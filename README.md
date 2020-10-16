# wisa
Who Is Still Alive: a broken link checker

# Building

Build:

```go build wisa.go```

Add wisa to your PATH or use it directly.

# Usage
type `wisa --help` for usage or:

```wisa -f [file]```

for verbose output (error logs)

```wisa -f [file] -v```

for ignoring certain URLs

```wisa -i [ignore file] -f [file]```

# Features

- Uses go routines to check for dead/broken links
- Uses `HEAD` requests for optimization
- `200-299` status codes are considered a `PASS`
- `403` emits a `WARN`
- All other codes are considered `DEAD`
- Uses flags for passing filename and for verbose output
- Coloured text using [gookit/color](https://github.com/gookit/color)
- Provide a second file to ignore certain urls