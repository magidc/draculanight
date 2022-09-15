# A fork of [Dracula.nvim](https://github.com/Mofiqul/dracula.nvim) as base to port VSCode theme [Dracula at night](https://github.com/bceskavich/dracula-at-night)

<h1 align="center" >🧛‍♂️ draculanight</h1>

<p align="center"><a href="https://draculatheme.com/">Dracula</a> colorscheme for <a href="https://neovim.io/">NEOVIM</a> written in Lua</p>

![Rust and NeoTree](./assets/1.png)

![Lua](./assets/2.png)

## ✔️ Requirements

- Neovim >= 0.7.0
- Treesitter (optional)

## #️ Supported Plugins

- [LSP](https://github.com/neovim/nvim-lspconfig)
- [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [nvim-compe](https://github.com/hrsh7th/nvim-compe)
- [nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [Telescope](https://github.com/nvim-telescope/telescope.nvim)
- [NvimTree](https://github.com/kyazdani42/nvim-tree.lua)
- [BufferLine](https://github.com/akinsho/nvim-bufferline.lua)
- [Git Signs](https://github.com/lewis6991/gitsigns.nvim)
- [Lualine](https://github.com/hoob3rt/lualine.nvim)
- [LSPSaga](https://github.com/glepnir/lspsaga.nvim)
- [indent-blankline](https://github.com/lukas-reineke/indent-blankline.nvim)
- [nvim-ts-rainbow](https://github.com/p00f/nvim-ts-rainbow)

## ⬇️ Installation

Install via package manager

```lua
-- Using Packer:
use 'magidc/draculanight'
```

```vim
" Using Vim-Plug:
Plug 'magidc/draculanight'
```

## 🚀 Usage

```lua
-- Lua:
vim.cmd[[colorscheme draculanight]]
```

```vim
" Vim-Script:
colorscheme draculanight
```

If you are using [`lualine`](https://github.com/hoob3rt/lualine.nvim), you can also enable the provided theme:

> Make sure to set theme as 'draculanight' as dracula already exists in lualine built in themes

```lua
require('lualine').setup {
  options = {
    -- ...
    theme = 'draculanight'
    -- ...
  }
}
```

## 🔧 Configuration

The configuration must be run before `colorscheme` command to take effect.

If you're using lua

```lua
local dracula = require("draculanight")
dracula.setup({
  -- customize dracula color palette
  colors = {
    bg = "#0E1419",
    fg = "#F8F8F2",
    selection = "#292E38",
    comment = "#A6C2F9",
    red = "#FF5555",
    orange = "#FFB86C",
    yellow = "#F1FA8C",
    green = "#50fa7b",
    purple = "#BD93F9",
    cyan = "#8BE9FD",
    pink = "#FF79C6",
    bright_red = "#FF6E6E",
    bright_green = "#69FF94",
    bright_yellow = "#FFFFA5",
    bright_blue = "#D6ACFF",
    bright_magenta = "#FF92DF",
    bright_cyan = "#A4FFFF",
    bright_white = "#FFFFFF",
    menu = "#21222C",
    visual = "#3E4452",
    gutter_fg = "#4B5263",
    nontext = "#3B4048",
    white = "#FFFFFF",
    black = "#191A21",
  },
  -- show the '~' characters after the end of buffers
  show_end_of_buffer = true, -- default false
  -- use transparent background
  transparent_bg = true, -- default false
  -- set custom lualine background color
  lualine_bg_color = "#44475a", -- default nil
  -- set italic comment
  italic_comment = true, -- default false
  -- overrides the default highlights see `:h synIDattr`
  overrides = {
    -- Examples
    -- NonText = { fg = dracula.colors().white }, -- set NonText fg to white
    -- NvimTreeIndentMarker = { link = "NonText" }, -- link to NonText highlight
    -- Nothing = {} -- clear highlight of Nothing
  },
})
```

The same works in viml

```vim
lua << EOF
local dracula = require("draculanight")
dracula.setup({
  -- customize dracula color palette
  colors = {
    bg = "#0E1419",
   fg = "#F8F8F2",
   selection = "#292E38",
   comment = "#A6C2F9",
   red = "#FF5555",
   orange = "#FFB86C",
   yellow = "#F1FA8C",
   green = "#50fa7b",
   purple = "#BD93F9",
   cyan = "#8BE9FD",
   pink = "#FF79C6",
   bright_red = "#FF6E6E",
   bright_green = "#69FF94",
   bright_yellow = "#FFFFA5",
   bright_blue = "#D6ACFF",
   bright_magenta = "#FF92DF",
   bright_cyan = "#A4FFFF",
   bright_white = "#FFFFFF",
   menu = "#21222C",
   visual = "#3E4452",
   gutter_fg = "#4B5263",
   nontext = "#3B4048",
   white = "#FFFFFF",
   black = "#191A21",
  },
  -- show the '~' characters after the end of buffers
  show_end_of_buffer = true, -- default false
  -- use transparent background
  transparent_bg = true, -- default false
  -- set custom lualine background color
  lualine_bg_color = "#44475a", -- default nil
  -- set italic comment
  italic_comment = true, -- default false
  -- overrides the default highlights see `:h synIDattr`
  overrides = {
    -- Examples
    -- NonText = { fg = draculanight.colors().white }, -- set NonText fg to white
    -- NvimTreeIndentMarker = { link = "NonText" }, -- link to NonText highlight
    -- Nothing = {} -- clear highlight of Nothing
  },
})
EOF
```

## 🎨 Importing colors for other usage

```lua
local colors = require('draculanight').colors()
```

This will return the folowing table

![colors](./assets/colors.png)
