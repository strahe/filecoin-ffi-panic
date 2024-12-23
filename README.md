# filecoin-ffi-panic

A lightweight substitute for filecoin-ffi designed to minimize build complexity and binary size.
This library provides the same interface as filecoin-ffi but throws "not implemented" panics for all methods,
making it ideal for projects that have filecoin-ffi as a transitive dependency but don't actually use its functionality.

## Usage

Just replace `github.com/filecoin-project/filecoin-ffi` with `github.com/strahe/filecoin-ffi-panic` in your go.mod file.

```shell
# Use main branch or replace with a specific version

go mod edit -replace=github.com/filecoin-project/filecoin-ffi=\
github.com/strahe/filecoin-ffi-panic@main

go mod tidy
```
