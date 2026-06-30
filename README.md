# Vim Leader Keymaps

Keymaps for [VSCodeVim extension](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim).

## Installation

This extension can be installed locally from a VSIX package.

Package the extension:

  ```bash
  npx @vscode/vsce package
  ```

Install the generated `.vsix` file:

  ```bash
  code --install-extension vscodevim-keymaps-0.0.1.vsix --force
  ```

Extension identifier: `hq3009.vscodevim-keymaps`

## Configuration defaults

The default leader key is `Space`. For some special modes, the local leader key is `,`.

## Usage

The mapping configuration uses the nvim name shortcuts as:

- `<C>` - `Ctrl`
- `<S>` - `Shift`
- `<A>` - `Alt`
- `<leader>` - `Space`

Only representative keymaps are shown below. Full mappings are defined in `package.json` under `contributes.configurationDefaults` and `contributes.keybindings`.

### Typical Leader Mappings (Normal Mode)

| Key                | Description             |
| ------------------ | ----------------------- |
| `<leader><leader>` | Show command palette    |
| `<leader>ss`       | Find in current file    |
| `<leader>sp`       | Find in files           |
| `<leader>rr`       | Replace in current file |
| `<leader>bb`       | Show all open editors   |
| `<leader>k`        | Close current editor    |
| `<leader>fs`       | Save file               |
| `<leader>fe`       | Focus explorer view     |

### Window and Tab Navigation

| Key          | Description              |
| ------------ | ------------------------ |
| `<leader>wh` | Focus left editor group  |
| `<leader>wj` | Focus group below        |
| `<leader>wk` | Focus group above        |
| `<leader>wl` | Focus right editor group |
| `<leader>ws` | Split editor down        |
| `<leader>wv` | Split editor right       |
| `<leader>wo` | Single editor layout     |
| `<leader>th` | Previous tab/editor      |
| `<leader>tl` | Next tab/editor          |

### Insert Mode Examples

| Key         | Description               |
| ----------- | ------------------------- |
| `kj` / `jk` | Exit insert mode          |
| `<C-a>`     | Move cursor to line start |
| `<C-e>`     | Move cursor to line end   |
| `<C-d>`     | Delete right              |
| `<C-j>`     | Insert newline            |

### Suggestions and Quick Input

| Key      | Description                     |
| -------- | ------------------------------- |
| `<C-n>`  | Next suggestion / list item     |
| `<C-p>`  | Previous suggestion / list item |
| `<A-/>`  | Trigger suggestions             |
| `<C-k>.` | Quick open                      |

### Notebook-Oriented Examples (Normal Mode)

| Key   | Description                   |
| ----- | ----------------------------- |
| `, ,` | Execute current notebook cell |
| `, a` | Insert code cell above        |
| `, b` | Insert code cell below        |
| `, m` | Change cell to markdown       |
| `, c` | Change cell to code           |

Notes:

- Some default VS Code shortcuts are intentionally unbound/reassigned (for example `Ctrl+,`, `Ctrl+N`, `Ctrl+P`) to better fit a Vim-like workflow.
- `Ctrl+N` / `Ctrl+P` are context-aware and are reused in lists, quick open, and suggestion widgets.
