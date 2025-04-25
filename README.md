# Tubular: A Custom Language Compiler

Welcome! Tubular is full compiler for a custom programming language, written in modern C++. It features a hand-crafted lexer, parser, AST, symbol table, and a code generator that emits WebAssembly Text (WAT). This project is a playground for experimenting with language design, parsing techniques, and low-level code generation.

## Features

- **Handwritten Lexer and Parser**: Built from scratch for full control and learning.
- **AST Construction**: Modular node classes for all language constructs.
- **Type Checking**: Static type analysis with support for custom types.
- **WebAssembly Code Generation**: Outputs WAT for execution in modern runtimes/browsers.
- **Recursive Functions**: Full support for recursion (extra credit feature).
- **String Type Casting**: Seamless casting between integers and strings (extra credit feature).
- **String Comparison**: Native support for string equality checks.
- **Robust Testing**: Extensive suite of both standard and error-handling tests.

## Directory Structure

```
├── Project4.cpp         # Main compiler entrypoint
├── lexer.hpp/.emplex    # Lexer implementation and DFA definition
├── ASTNode.hpp          # AST node hierarchy
├── Control.hpp          # Code generation and control utilities
├── SymbolTable.hpp      # Symbol management and type info
├── TokenQueue.hpp       # Token stream abstraction
├── Type.hpp             # Type system
├── tools.hpp            # Utility functions
├── tests/               # Test cases, runners, and HTML/JS test harnesses
├── Makefile             # Build and test automation
├── LICENSE
└── README.md
```

## Getting Started

### Build

Requires a modern C++20 compiler (tested with g++/clang++):

```sh
make
```

### Usage

Compile a `.tube` source file to WebAssembly Text:

```sh
./Project4 <source.tube> > output.wat
```

### Run Tests

To run the full test suite:

```sh
make tests
```

Or run individual tests in the `tests/` directory. The test harness supports both CLI and browser-based testing (see `wasm-tester.html`).

## Extra Credit & Extensions

- **Recursive Functions**: Fully implemented and tested (see `test-21`, `test-24`).
- **String Type Casting**: `:string` works on integers (see `test-22`).
- **String Comparison**: Equality checks with `==` (see `test-23`).
- **New Tests**: Added tests for all new features.

## Author

Aditya Chaudhari

