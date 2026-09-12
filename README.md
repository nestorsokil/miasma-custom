# Miasma Custom

Miasma's woods-inspired palette with the minimalistic syntax highlighting from GitHub Dimmed Custom.

## What changed from real Miasma

- **Default code is greyish white (`#c2c2b0`)** instead of Miasma's tan/rust default text.
- **Less token highlighting** — method calls, functions, types, classes, parameters, punctuation and operators all use the neutral foreground. Only a few things are colored:
  - Keywords, storage, modifiers → Miasma green (`#5f875f`)
  - Strings, numbers, character/boolean literals → Miasma rust (`#bb7744`)
  - Comments → Miasma grey (`#666666`)
  - Named constants / enum members → foreground, bold italic

## Palette

Backgrounds `#222222` / `#1c1c1c` / `#2a2a2a`, borders warm olive-grey, accents green `#5f875f`, moss `#78834b`, gold `#d7c483` / `#c9a554`, rust `#bb7744` / `#b36d43`. Blue/purple/cyan from the source theme are folded into the Miasma greens and golds.

### Java

- Gold annotations, moss javadoc
- No `var` highlight (the Java extension infers the real type instead of defaulting to `keyword`)

### Go

Mirrors the Java treatment as closely as the Go grammar allows:

- Functions, builtins (`len`, `make`, `append`), type names, builtin types, package/import names, variables and parameters share the neutral foreground (Go functions take a subtle gold)
- Struct fields are bold italic, matching Java fields
- Operators (`:=`, `<-`, `&&`, `...`) stay neutral
- Strings, raw strings, runes and numeric literals share the Miasma literal color
- `nil`/`iota` follow the `null` color; `true`/`false` follow the boolean color
- Applied through both TextMate scopes and `gopls` semantic tokens, so highlighting is identical whether or not the language server is running

## Credits

- Palette: [Miasma](https://github.com/xero/miasma.nvim) by xero (CC0-1.0)
- Syntax overrides: adapted from the sibling GitHub Dimmed Custom theme
