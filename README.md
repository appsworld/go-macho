# go-macho [WIP] 🚧

[![Go](https://github.com/appsworld/go-macho/workflows/Go/badge.svg?branch=master)](https://github.com/appsworld/go-macho/actions) [![Go Reference](https://pkg.go.dev/badge/github.com/appsworld/go-macho.svg)](https://pkg.go.dev/github.com/appsworld/go-macho) [![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org)

> Package macho implements access to and creation of Mach-O object files.

---

## Why 🤔

This package goes beyond the Go's `debug/macho` to:

- Cover ALL load commands and architectures
- Provide nice summary string output
- Allow for creating custom macho

## Install

```bash
$ go get github.com/appsworld/go-macho
```

## Getting Started

```go
package main

import "github.com/appsworld/go-macho"

func main() {
    f, err := os.Open("/path/to/macho")
    if err != nil {
        panic(err)
    }

    m, err := macho.NewFile(f)
    if err != nil {
        panic(err)
    }

    fmt.Println(m.FileTOC.String())
}
```

## License

MIT Copyright (c) 2021 **appsworld**
