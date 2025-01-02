<h1 align="center">-☄️ Markview.nvim</h1>

<p align="center">
    A <b>Markdown</b>, <b>HTML</b>, <b>LaTeX</b>, <b>Typst</b> & <b>YAML</b> previewer for Neovim.
</p>

<!-- Video Demo here! -->

<div align="center">
    <a href="">📚 Wiki</a> | <a href="">🧩 Extras</a> | <a href="">📦 Presets</a>
</div>

<!-- Screenshots here -->

## 📖 Table of contents

- [🧭 Configuration]()
- [🎇 Commands]()
- [📞 Autocmds]()
- [🎨 Highlight groups]()

## 🧭 Configuration

Check the [wiki]() for the entire configuration table. A simplified version is given below.

<details>
    <summary>Click for config jump-scare</summary><!-- --+ -->

```lua
--- Configuration table for `markview.nvim`.
---@class mkv.config
---
---@field experimental config.experimental | fun(): config.experimental
---@field highlight_groups { [string]: config.hl } | fun(): { [string]: config.hl }
---@field html config.html | fun(): config.html
---@field latex config.latex | fun(): config.latex
---@field markdown config.markdown | fun(): config.markdown
---@field markdown_inline config.markdown_inline | fun(): config.markdown_inline
---@field preview config.preview | fun(): config.preview
---@field renderers config.renderer[] | fun(): config.renderer[]
---@field typst config.typst | fun(): config.typst
---@field yaml config.yaml | fun(): config.yaml
mkv.config = {
    experimental = {
        date_formats = {},
        date_time_formats = {},

        text_filetypes = {},
        read_chunk_size = 1000,
        link_open_alerts = false,
        file_open_command = "tabnew",

        list_empty_line_tolerance = 3
    },
    highlight_groups = {},
    preview = {
        enable = true,
        filetypes = { "md", "rmd", "quarto" },
        ignore_buftypes = { "nofile" },
        ignore_previews = {},

        modes = { "n", "no", "c" },
        hybrid_modes = {},
        debounce = 50,
        draw_range = { vim.o.lines, vim.o.lines },
        edit_range = { 1, 0 },

        callbacks = {},

        splitview_winopts = { split = "left" }
    },
    renderers = {},

    html = {
        enable = true,

        container_elements = {},
        headings = {},
        void_elements = {},
    },
    latex = {
        enable = true,

        blocks = {},
        commands = {},
        escapes = {},
        fonts = {},
        inlines = {},
        parenthesis = {},
        subscripts = {},
        superscripts = {},
        symbols = {},
        texts = {}
    },
    markdown = {
        enable = true,

        block_quotes = {},
        code_blocks = {},
        headings = {},
        horizontal_rules = {},
        list_items = {},
        metadata_plus = {},
        metadata_minus = {},
        tables = {}
    },
    markdown_inline = {
        enable = true,

        block_references = {},
        checkboxes = {},
        emails = {},
        embed_files = {},
        entities = {},
        escapes = {},
        footnotes = {},
        highlights = {},
        hyperlinks = {},
        images = {},
        inline_codes = {},
        internal_links = {},
        uri_autolinks = {}
    },
    typst = {
        enable = true,

        codes = {},
        escapes = {},
        headings = {},
        labels = {},
        list_items = {},
        math_blocks = {},
        math_spans = {},
        raw_blocks = {},
        raw_spans = {},
        reference_links = {},
        subscripts = {},
        superscript = {},
        symbols = {},
        terms = {},
        url_links = {}
    },
    yaml = {
        enable = true,

        properties = {}
    }
}
```
<!-- --_ -->
</details>

## 🎇 Commands

This plugin follows the *sub-commands* approach for creating commands. There is only a single `:Markview` command.

It comes with the following sub-commands,

>[!NOTE]
> When no sub-command name is provided(or an invalid sub-command is used) `:Markview` will run `:Markview Toggle`.


| Sub-command  | Arguments           | Description                              |
|--------------|---------------------|------------------------------------------|
| `attach`     | **buffer**, integer | Attaches to **buffer**.                  |
| `detach`     | **buffer**, integer | Detaches from **buffer**.                |
|              |                     | ———————————————————————————————————————— |
| `Enable`     | none                | Enables preview *globally*.              |
| `Disable`    | none                | Disables preview *globally*.             |
| `Toggle`     | none                | Toggles preview *globally*.              |
|              |                     | ———————————————————————————————————————— |
| `enable`     | **buffer**, integer | Enables preview for **buffer**.          |
| `disable`    | **buffer**, integer | Disables preview for **buffer**.         |
| `toggle`     | **buffer**, integer | Toggles preview for **buffer**.          |
|              |                     | ———————————————————————————————————————— |
| `splitOpen`  | **buffer**, integer | Opens *splitview* for **buffer**.        |
| `splitClose` | none                | Closes any open *splitview*.             |
| `splitToggle`| none                | Toggles *splitview*.                     |
| `splitRedraw`| none                | Updates *splitview* contents.            |
|              |                     | ———————————————————————————————————————— |
| `Render`     | none                | Updates preview of all *active* buffers. |
| `Clear`      | none                | Clears preview of all **active** buffer. |
|              |                     | ———————————————————————————————————————— |
| `render`     | **buffer**, integer | Renders preview for **buffer**.          |
| `clear`      | **buffer**, integer | Clears preview for **buffer**.           |
|              |                     | ———————————————————————————————————————— |
| `toggleAll`  | none                | **Deprecated** version of `Toggle`.      |
| `enableAll`  | none                | **Deprecated** version of `Enable`.      |
| `disableAll` | none                | **Deprecated** version of `Disable`.     |

>[!TIP]
> **buffer** defaults to the current buffer. So, you can run commands on the current buffer without providing the buffer.
> ```vim
> :Markview toggle "Toggles preview of the current buffer.
> ```

## 📞 Autocmds

`markview.nvim` emits various *autocmd events* during different parts of the rendering allowing users to extend the plugin's functionality.

>[!NOTE]
> Autocmds are executed **after** callbacks!

Currently emitted autocmds are,

- **MarkviewAttach**
  Called when attaching to a buffer.

  Arguments,

  + `buffer`, integer
    The buffer that's being attached to.

  + `windows`, integer[]
    List of windows attached to `buffer`.

- **MarkviewDetach**
  Called when detaching from a buffer.

  Arguments,

  + `buffer`, integer
    The buffer that's being detached from.

  + `windows`, integer[]
    List of windows attached to `buffer`.

- **MarkviewDisable**
  Called when disabling previews in a buffer.

  Arguments,

  + `buffer`, integer
    The buffer whose the preview was disabled.

  + `windows`, integer[]
    List of windows attached to `buffer`.

- **MarkviewEnable**
  Called when enabling previews in a buffer.

  Arguments,

  + `buffer`, integer
    The buffer whose the preview was enabled.

  + `windows`, integer[]
    List of windows attached to `buffer`.

- **MarkviewSplitviewClose**
  Called when the splitview window is closed. Called *before* splitview is closed.

  Arguments,

  + `source`, integer
    The buffer whose contents are being shown.

  + `preview_buffer`, integer
    The buffer that's showing the preview.

  + `preview_window`, integer
    The window where the `preview_buffer` is being shown.

- **MarkviewSplitviewOpen**
  Called when the splitview window is opened.

  Arguments,

  + `source`, integer
    The buffer whose contents are being shown.

  + `preview_buffer`, integer
    The buffer that's showing the preview.

  + `preview_window`, integer
    The window where the `preview_buffer` is being shown.

## 🎨 Highlight groups

`markview.nvim` creates a number of *primary highlight groups* that are used by most of the decorations.

>[!IMPORTANT]
> These groups are all **generated** during runtime and as such their colors may look different.

If you want to create your own *dynamic* highlight groups or modify existing ones, see the [custom highlight groups](placeholder) section


| Highlight group      | Generated from                          | Default                     |
|----------------------|-----------------------------------------|-----------------------------|
| MarkviewPalette0     | Normal(bg) + Comment(fg)                | fg: `#9399b2` bg: `#35374a` |
| MarkviewPalette0Fg   | Comment(fg)                             | fg: `#9399b2`               |
| MarkviewPalette0Bg   | Normal(bg) + Comment(fg)                | bg: `#35374a`               |
| MarkviewPalette0Sign | Normal(bg) + Comment(fg), LineNr(bg)    | fg: `#9399b2`               |
| ———————————————————— | ——————————————————————————————————————— | ——————————————————————————— |
| MarkviewPalette1     | Normal(bg) + markdownH1(fg)             | fg: `#f38ba8` bg: `#4d3649` |
| MarkviewPalette1Fg   | markdownH1(fg)                          | fg: `#f38ba8`               |
| MarkviewPalette1Bg   | Normal(bg) + markdownH1(fg)             | bg: `#4d3649`               |
| MarkviewPalette1Sign | Normal(bg) + markdownH1(fg), LineNr(bg) | fg: `#f38ba8`               |
| ———————————————————— | ——————————————————————————————————————— | ——————————————————————————— |
| MarkviewPalette2     | Normal(bg) + markdownH2(fg)             | fg: `#f9b387` bg: `#4d3d43` |
| MarkviewPalette2Fg   | markdownH2(fg)                          | fg: `#f9b387`               |
| MarkviewPalette2Bg   | Normal(bg) + markdownH2(fg)             | bg: `#4d3d43`               |
| MarkviewPalette2Sign | Normal(bg) + markdownH2(fg), LineNr(bg) | fg: `#f9b387`               |
| ———————————————————— | ——————————————————————————————————————— | ——————————————————————————— |
| MarkviewPalette3     | Normal(bg) + markdownH3(fg)             | fg: `#f9e2af` bg: `#4c474b` |
| MarkviewPalette3Fg   | markdownH3(fg)                          | fg: `#f9e2af`               |
| MarkviewPalette3Bg   | Normal(bg) + markdownH3(fg)             | bg: `#4c474b`               |
| MarkviewPalette3Sign | Normal(bg) + markdownH3(fg), LineNr(bg) | fg: `#f9e2af`               |
| ———————————————————— | ——————————————————————————————————————— | ——————————————————————————— |
| MarkviewPalette4     | Normal(bg) + markdownH4(fg)             | fg: `#a6e3a1` bg: `#3c4948` |
| MarkviewPalette4Fg   | markdownH4(fg)                          | fg: `#a6e3a1`               |
| MarkviewPalette4Bg   | Normal(bg) + markdownH4(fg)             | bg: `#3c4948`               |
| MarkviewPalette4Sign | Normal(bg) + markdownH4(fg), LineNr(bg) | fg: `#a6e3a1`               |
| ———————————————————— | ——————————————————————————————————————— | ——————————————————————————— |
| MarkviewPalette5     | Normal(bg) + markdownH5(fg)             | fg: `#74c7ec` bg: `#314358` |
| MarkviewPalette5Fg   | markdownH5(fg)                          | fg: `#74c7ec`               |
| MarkviewPalette5Bg   | Normal(bg) + markdownH5(fg)             | bg: `#314358`               |
| MarkviewPalette5Sign | Normal(bg) + markdownH5(fg), LineNr(bg) | fg: `#74c7ec`               |
| ———————————————————— | ——————————————————————————————————————— | ——————————————————————————— |
| MarkviewPalette6     | Normal(bg) + markdownH6(fg)             | fg: `#b4befe` bg: `#3c405b` |
| MarkviewPalette6Fg   | markdownH6(fg)                          | fg: `#b4befe`               |
| MarkviewPalette6Bg   | Normal(bg) + markdownH6(fg)             | bg: `#3c405b`               |
| MarkviewPalette6Sign | Normal(bg) + markdownH6(fg), LineNr(bg) | fg: `#b4befe`               |


> The source highlight group's values are turned into `Lab` color-space and then mixed to reduce unwanted results.

These groups are then used as links by other groups responsible for various preview elements,

>[!NOTE]
> These groups exist for the sake of *backwards compatibility* and *ease of use*.
>
> You will see something like `fg: Normal`, it means the *fg* of Normal was used as the *fg* of that group.


| Highlight group           | value                                      |
|---------------------------|--------------------------------------------|
| MarkviewBlockQuoteDefault | link: `MarkviewPalette0Fg`                 |
| MarkviewBlockQuoteError   | link: `MarkviewPalette1Fg`                 |
| MarkviewBlockQuoteNote    | link: `MarkviewPalette5Fg`                 |
| MarkviewBlockQuoteOk      | link: `MarkviewPalette4Fg`                 |
| MarkviewBlockQuoteSpecial | link: `MarkviewPalette3Fg`                 |
| MarkviewBlockQuoteWarn    | link: `MarkviewPalette2Fg`                 |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewCheckboxCancelled | link: `MarkviewPalette0Fg`                 |
| MarkviewCheckboxChecked   | link: `MarkviewPalette4Fg`                 |
| MarkviewCheckboxPending   | link: `MarkviewPalette2Fg`                 |
| MarkviewCheckboxProgress  | link: `MarkviewPalette6Fg`                 |
| MarkviewCheckboxUncheked  | link: `MarkviewPalette1Fg`                 |
| MarkviewCheckboxStriked   | link\*: `MarkviewPalette0Fg`               |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewCode              | bg\*\*: `normal` ± 5%(L)                   |
| MarkviewCodeInfo          | bg\*\*: `normal` ± 5%(L), fg: `comment`    |
| MarkviewCodeFg            | fg\*\*: `normal` ± 5%(L)                   |
| MarkviewInlineCode        | fg\*\*: `normal` ± 10%(L)                  |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewIcon0             | link\*\*\*: `MarkviewPalette0Fg`           |
| MarkviewIcon1             | link\*\*\*: `MarkviewPalette1Fg`           |
| MarkviewIcon2             | link\*\*\*: `MarkviewPalette5Fg`           |
| MarkviewIcon3             | link\*\*\*: `MarkviewPalette4Fg`           |
| MarkviewIcon4             | link\*\*\*: `MarkviewPalette3Fg`           |
| MarkviewIcon5             | link\*\*\*: `MarkviewPalette2Fg`           |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewGradient0         | fg: `Normal`                               |
| MarkviewGradient1         | fg\*\*\*\*: `lerp(Normal, Title, 1/9)`     |
| MarkviewGradient2         | fg\*\*\*\*: `lerp(Normal, Title, 2/9)`     |
| MarkviewGradient3         | fg\*\*\*\*: `lerp(Normal, Title, 3/9)`     |
| MarkviewGradient4         | fg\*\*\*\*: `lerp(Normal, Title, 4/9)`     |
| MarkviewGradient5         | fg\*\*\*\*: `lerp(Normal, Title, 5/9)`     |
| MarkviewGradient6         | fg\*\*\*\*: `lerp(Normal, Title, 6/9)`     |
| MarkviewGradient7         | fg\*\*\*\*: `lerp(Normal, Title, 7/9)`     |
| MarkviewGradient8         | fg\*\*\*\*: `lerp(Normal, Title, 8/9)`     |
| MarkviewGradient9         | fg: `Title`                                |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewHeading1          | link: `MarkviewPalette1`                   |
| MarkviewHeading2          | link: `MarkviewPalette2`                   |
| MarkviewHeading3          | link: `MarkviewPalette3`                   |
| MarkviewHeading4          | link: `MarkviewPalette4`                   |
| MarkviewHeading5          | link: `MarkviewPalette5`                   |
| MarkviewHeading6          | link: `MarkviewPalette6`                   |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewEmail             | link: `@markup.link.url.markdown_inline`   |
| MarkviewHyperlink         | link: `@markup.link.label.markdown_inline` |
| MarkviewImage             | link: `@markup.link.label.markdown_inline` |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewSubscript         | link: `MarkviewPalette3Fg`                 |
| MarkviewSuperscript       | link: `MarkviewPalette6Fg`                 |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewListItemMinus     | link: `MarkviewPalette2Fg`                 |
| MarkviewListItemPlus      | link: `MarkviewPalette4Fg`                 |
| MarkviewListItemStar      | link: `MarkviewPalette6Fg`                 |
| ————————————————————————— | —————————————————————————————————————————— |
| MarkviewTableHeader       | link: `@markup.heading.markdown`           |
| MarkviewTableBorder       | link: `MarkviewPalette5Fg`                 |
| MarkviewTableAlignCenter  | link: `MarkviewPalette5Fg`                 |
| MarkviewTableAlignLeft    | link: `MarkviewPalette5Fg`                 |
| MarkviewTableAlignRight   | link: `MarkviewPalette5Fg`                 |


> \* = Only the foreground color is used. Strikeout is added.
> \*\* = The color is converted to HSL and it's luminosity(L) is increased/decreased by the specified amount.
> \*\*\* = The background color of `MarkviewCode` is added to the groups.
> \*\*\*\* = Linearly interpolated value between 2 highlight groups `fg`.

---

The options and the highlight groups they use are given below,

| Option name               | Group(s)                                                             |
|---------------------------|----------------------------------------------------------------------|
| block_quotes              | `MarkviewBlockQuote*`                                                |
| code_blocks               | `MarkviewCode*`, `MarkviewIcon*`(icon), `MarkviewPalette[n]Fg`(sign) |
| headings                  | `MarkviewHeading[n]`, `MarkviewPalette[n]Sign`(sign)                 |
| horizontal_rules          | `MarkviewGradient[n]`                                                |
| list_items                | `MarkviewListItem*`                                                  |
| metadata_minus            | `MarkviewCode`, `MarkviewCodeFg`                                     |
| metadata_plus             | `MarkviewCode`, `MarkviewCodeFg`                                     |
| reference_definitions     | `MarkviewPalette4Fg`                                                 |
| tables                    | `MarkviewTable*`                                                     |
| ————————————————————————— | ———————————————————————————————————————————————————————————————————— |
| block_references          | `Comment`                                                            |
| checkboxes                | `MarkviewCheckbox*`                                                  |
| emails                    | `MarkviewEmail`                                                      |
| embed_files               | `MarkviewPalette2Fg`                                                 |
| entities                  | `Special`                                                            |
| escapes                   | None                                                                 |
| footnotes                 | `MarkviewHyperlink`                                                  |
| highlights                | `MarkviewPalette1`                                                   |
| hyperlinks                | `MarkviewHyperlink`                                                  |
| images                    | `MarkviewImage`                                                      |
| inline_codes              | `MarkviewInlineCode`                                                 |
| internal_links            | `MarkviewHyperlink`                                                  |
| uri_autolinks             | `MarkviewEmail`                                                      |
| ————————————————————————— | ———————————————————————————————————————————————————————————————————— |
| container_elements        | None                                                                 |
| headings                  | `MarkviewHeading[n]`, `MarkviewPalette[n]Sign`(sign)                 |
| void_elements             | None                                                                 |
| ————————————————————————— | ———————————————————————————————————————————————————————————————————— |
| blocks                    | `MarkviewCode*`                                                      |
| commands                  | `@punctuation.bracket`, `@keyword.function`                          |
| escapes                   | None                                                                 |
| fonts                     | None                                                                 |
| inlines                   | `MarkviewInlineCode`                                                 |
| parenthesis               | `@punctuation.bracket`                                               |
| subscripts                | `MarkviewSubscript`                                                  |
| superscripts              | `MarkviewSuperscript`                                                |
| symbols                   | `Comment`                                                            |
| texts                     | None                                                                 |
| ————————————————————————— | ———————————————————————————————————————————————————————————————————— |
| codes                     | `MarkviewCode`                                                       |
| escapes                   | None                                                                 |
| headings                  | `MarkviewHeading[n]`, `MarkviewPalette[n]Sign`(sign)                 |
| labels                    | `MarkviewInlineCode`                                                 |
| list_items                | `MarkviewListItemMinus`, `MarkviewListItemPlus`                      |
| math_blocks               | `MarkviewCode*`                                                      |
| math_spans                | `MarkviewInlineCode*`                                                |
| raw_blocks                | `MarkviewCode`                                                       |
| raw_spans                 | `MarkviewInlineCode`                                                 |
| reference_links           | `MarkviewHyperlink`                                                  |
| subscripts                | `MarkviewSubscript`                                                  |
| superscripts              | `MarkviewSuperscript`                                                |
| symbols                   | `Special`                                                            |
| terms                     | `MarkviewPalette6Fg`                                                 |
| url_links                 | `MarkviewEmail`                                                      |
| ————————————————————————— | ———————————————————————————————————————————————————————————————————— |
| properties                | None                                                                 |

