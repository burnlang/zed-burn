# Burn for Zed

Language support for [Burn](https://github.com/burnlang/burn) in [Zed](https://zed.dev): tree-sitter highlighting,
outline, indentation and brackets, plus the Burn language server (`burn lsp`) for diagnostics, completion, hover,
signature help, inlay hints, go to definition (also into the standard library and built-ins), references, rename and
formatting. A run button appears next to `fun main`.

## Install

```sh
git clone https://github.com/burnlang/zed-burn
```

Then run **zed: install dev extension** in Zed and choose the cloned folder. Zed needs Rust installed through rustup
to build it, and fetches the grammar from [tree-sitter-burn](https://github.com/burnlang/tree-sitter-burn). The extension starts `burn` from your `PATH`,
`$BURN_HOME/bin` or `~/.burn/bin`. To use another one, set the path in
Zed's settings:

```json
{
  "lsp": {
    "burn": {
      "binary": { "path": "/path/to/burn", "arguments": ["lsp"] }
    }
  }
}
```

## Updating the grammar

`extension.toml` pins the grammar to a commit of tree-sitter-burn. After a grammar change, set `rev` to the new
commit; CI checks that the commit exists.

## License

GPL-3.0-only
