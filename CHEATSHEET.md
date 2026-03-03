# Neovim Configuration Cheatsheet

## Structure

```
~/.config/nvim/
├── init.lua              # Entry point, sets up lazy.nvim
├── lua/
│   ├── vim-options.lua   # Core settings & basic keymaps
│   └── plugins/          # One file per plugin
```

## Key Bindings (Leader = Space)

### Navigation

| Keys | Action |
|------|--------|
| `Ctrl+h/j/k/l` | Move between windows (also works with tmux panes) |
| `Space h` | Clear search highlighting |

### Files

| Keys | Action |
|------|--------|
| `Ctrl+p` | Find files (Telescope) |
| `Space fg` | Live grep (search text in files) |
| `Space Space` | Recent files |
| `Ctrl+n` | Toggle file tree (Neo-tree) |
| `Space bf` | Buffer list in float window |
| `-` | Open Oil file browser |

### LSP

| Keys | Action |
|------|--------|
| `K` | Hover documentation |
| `Space gd` | Go to definition |
| `Space gr` | Find references |
| `Space ca` | Code actions |
| `Space gf` | Format file |

### Git

| Keys | Action |
|------|--------|
| `Space gp` | Preview git hunk |
| `Space gt` | Toggle line blame |

### Testing (runs in tmux via vimux)

| Keys | Action |
|------|--------|
| `Space t` | Run nearest test |
| `Space T` | Run current file tests |
| `Space a` | Run all tests |
| `Space l` | Re-run last test |
| `Space g` | Visit last test file |

### Tmux Integration

| Keys | Action |
|------|--------|
| `Ctrl+h/j/k/l` | Navigate between Neovim splits AND tmux panes seamlessly |

Your tests run in a tmux pane via vimux - when you press `Space t`, the test output appears in a tmux split, not inside Neovim.

### Completion

| Keys | Action |
|------|--------|
| `Ctrl+Space` | Trigger completion |
| `Enter` | Confirm selection |
| `Ctrl+e` | Cancel completion |
| `Ctrl+b/f` | Scroll docs up/down |

## Plugins

| Category | Plugins |
|----------|---------|
| LSP/Completion | nvim-lspconfig, mason, nvim-cmp, LuaSnip |
| Syntax | nvim-treesitter |
| Files | Telescope, Neo-tree, Oil |
| Git | vim-fugitive, gitsigns |
| Formatting | none-ls (Prettier, Stylua, Rubocop) |
| Testing | vim-test + vimux (runs in tmux) |
| Theme | Catppuccin Mocha (dark) |

## Editor Settings

- 2-space indentation with spaces (not tabs)
- No swap files
- Line numbers enabled

## Languages Supported

- TypeScript/JavaScript - ts_ls + Prettier
- Ruby - Solargraph + Rubocop
- Lua - lua_ls + Stylua
- HTML - HTML LSP
