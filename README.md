# Journal (.jnl) Syntax

Lightweight language support for Journal `.jnl` files in Visual Studio Code. The extension provides syntax highlighting and folding for journal entries.

## Features

- Highlights entry dates, mood labels, optional themes, separators, and note text.
- Supports both `:` and `|` between a date and mood, and `|` before an optional theme.
- Treats lines between `---` markers as foldable entry sections.
- Associates `.jnl` files with the **Journal** language mode automatically.

The exact highlight colors depend on your selected VS Code theme.

## Journal format

An entry header starts with a date in `YYYY-MM-DD` form, followed by `:` or `|`, then a mood label. Add an optional theme after another `|`. Lines that do not match a header are treated as notes; notes can span multiple lines.

```jnl
---
2026-11-18|tired|work
Some notes here which
can even be multiline
---
2026-11-17: ok | health
---
```

## Usage

Install the extension and open a `.jnl` file. If VS Code does not select **Journal** automatically, use the language-mode selector in the status bar and choose **Journal**.

## Development

To run the extension from this repository, open the folder in VS Code and press `F5` to launch an Extension Development Host. The included [`example.jnl`](./example.jnl) demonstrates the supported syntax.

To package the extension as a VSIX, run:

```sh
npm run package
```

## Requirements

Visual Studio Code 1.80.0 or later.

## Extension settings

This extension does not contribute any settings.
