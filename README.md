# GoLox

GoLox is an implementation of the Lox language from *Crafting Interpreters*.

## Requirements

- Go 1.27.1 or later
- No third-party Go packages are required.

Install Go from the official instructions:

https://go.dev/doc/install

After installation, verify Go is available:

```text
go version
```

This project was built on a Windows 11, version 25H2 machine. Instructions may differ slightly for Mac or Linux but the core principle is the same. For questions, consult the Go documentation.

## Run the Project

Open PowerShell or Command Prompt (or Terminal) and change to the GoLox project directory:

```text
cd "C:\Users\{Path to Your Project}\golox"
```

Start the interactive prompt:

```text
go run .
```

At the `>` prompt, enter Lox source code. Press `Ctrl+C` to stop the program.

To scan a source file, provide its path as the first argument. The repository includes `test_src_code.lox`:

```text
go run . test_src_code.lox
```

You can also provide an absolute or relative path to another `.lox` source file:

```text
go run . path\to\your\source.lox
```

The scanner prints each token it recognizes, including the final `EOF` token.

## Run the Tests

Run all tests for this GoLox module from the project directory:

```text
go test
```

A successful test run ends with output similar to:

```text
PASS
ok      golox
```

To see each scanner test while it runs:

```text
go test -v
```

To run only scanner tests:

```text
go test -run TestScanner -v
```

## Project Files

- `golox.go` - Program entry point and command-line handling.
- `scanner.go` - Token definitions, lexical scanner, REPL, and file execution.
- `scanner_test.go` - Built-in Go tests for scanner behavior.
- `test_src_code.lox` - Example Lox source file.
- `go.mod` - Go module definition.
