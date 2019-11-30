# gomodnogen

## depends on a module that has a test. This test imports generated code (`.gen`) that's not checked in. `go mod tidy` fails with `leading dot in path element`

```
$ go mod tidy
go: finding github.com/xytan0056/depwithoutgen latest
github.com/xytan0056/gomodnogen imports
	github.com/xytan0056/depwithoutgen tested by
	github.com/xytan0056/depwithoutgen.test imports
	github.com/xytan0056/depwithoutgen/.gen/client: malformed module path "github.com/xytan0056/depwithoutgen/.gen/client": leading dot in path element
```