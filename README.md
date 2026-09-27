# Neovim Config

A personal Neovim setup focused on everyday software development. It uses `lazy.nvim` for plugin management, Catppuccin Mocha for the theme, Telescope for search, Treesitter for parsing, Harpoon for quick file navigation, Git tooling, LSP support, completion, and Neo-tree.

## Requirements

- Neovim 0.11 or newer
- Git
- A terminal with true color support
- Language toolchains for the LSP servers you use

## Install

Clone or copy this directory to your Neovim config path:

```cmd
git clone https://github.com/AnalyticsWithJeff/nvim-config %LOCALAPPDATA%\nvim
```

On macOS or Linux:

```sh
git clone https://github.com/AnalyticsWithJeff/nvim-config ~/.config/nvim
```

Start Neovim:

```sh
nvim
```

`lazy.nvim` bootstraps itself on first launch and installs the configured plugins.

## Main features

- Catppuccin Mocha theme with lualine integration
- Telescope fuzzy finding
- Treesitter highlighting and indentation
- Harpoon file marks
- Gitsigns and Fugitive Git workflow
- Mason-managed LSP servers
- LSP keymaps for definitions, references, rename, code actions, hover, and type definitions
- `nvim-cmp` completion with snippets, path, buffer, and LSP sources
- Neo-tree file explorer

## Keymaps

Leader is `<Space>`.

| Key | Action |
| --- | --- |
| `<leader>w` | Save file |
| `<leader>q` | Quit window |
| `<leader>x` | Close buffer |
| `<Esc>` | Clear search highlight |
| `<C-h>` / `<C-j>` / `<C-k>` / `<C-l>` | Move between windows |
| `<leader>ff` | Find files |
| `<leader>fg` | Live grep |
| `<leader>fb` | List buffers |
| `<leader>fh` | Search help tags |
| `<leader>fr` | Recent files |
| `<leader>a` | Add current file to Harpoon |
| `<leader>h` | Open Harpoon menu |
| `<leader>1`..`<leader>4` | Jump to Harpoon file 1..4 |
| `<C-S-P>` / `<C-S-N>` | Previous / next Harpoon file |
| `<leader>e` | Toggle Neo-tree |
| `<leader>gg` | Git status |
| `<leader>gp` | Preview Git hunk |
| `<leader>gn` / `<leader>gN` | Next / previous Git hunk with preview |
| `<leader>gb` | Git blame current line |
| `<leader>gd` | Git diff current file |
| `<leader>gs` / `<leader>gr` | Stage / reset hunk |
| `<leader>gS` / `<leader>gR` | Stage / reset buffer |
| `gd` | LSP go to definition |
| `gr` | LSP references |
| `gI` | LSP implementation |
| `<leader>D` | LSP type definition |
| `<leader>rn` | LSP rename |
| `<leader>ca` | LSP code action |
| `K` | LSP hover docs |

## Managed LSP servers

Mason installs these servers by default:

- `lua_ls`
- `ts_ls`
- `pyright`
- `gopls`
- `rust_analyzer`

## Notes

Plugin versions are pinned in `lazy-lock.json`. Run `:Lazy` inside Neovim to inspect, update, or sync plugins.
