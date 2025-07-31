# tree-sitter-toml

A [Tree-sitter](https://tree-sitter.github.io/tree-sitter/) grammar for the [TOML](https://toml.io/) configuration language.

## Features

- **Complete TOML Support**: Full support for the TOML v1.0 specification including tables, arrays, inline tables, and all data types
- **High Performance**: Fast and efficient parsing with Tree-sitter's incremental parsing capabilities
- **Robust Error Recovery**: Graceful handling of syntax errors with detailed error messages
- **Cross-Language Bindings**: Available for multiple programming languages through official bindings
- **Incremental Parsing**: Efficient re-parsing of modified documents without full re-analysis
- **Syntax Tree Queries**: Support for Tree-sitter's powerful query language for syntax analysis

## Usage

To use this grammar with Tree-sitter, you'll need to install the appropriate language binding and load the grammar.

### Basic Example

```javascript
const Parser = require('tree-sitter');
const TOML = require('tree-sitter-toml');

const parser = new Parser();
parser.setLanguage(TOML);

const sourceCode = `
[package]
name = "tree-sitter-toml"
version = "0.1.0"
authors = ["Tree-sitter Team"]

[dependencies]
tree-sitter = "0.20"
`;

const tree = parser.parse(sourceCode);
console.log(tree.rootNode.toString());
```

### Language Bindings

This grammar is available through official bindings for the following languages:

- **C**: Native C library with CMake support
- **Go**: Go module with native bindings
- **Node.js**: NPM package with TypeScript definitions
- **Python**: PyPI package with full Python API
- **Rust**: Cargo crate with Rust bindings
- **Swift**: Swift Package Manager support

Each binding provides idiomatic APIs for working with the TOML grammar in its respective language ecosystem.