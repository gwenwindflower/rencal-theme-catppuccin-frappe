# Catppuccin Frappé for renCal

[Catppuccin Frappé](https://catppuccin.com/palette/) as a dark theme for [renCal](https://rencal.org). Assign it to the **dark** slot in **Settings → Themes**, or pick it in Single mode.

## Local install

Installing via the GUI adds the plugin to `plugins.toml`:

| Platform | Path |
| --- | --- |
| macOS | `~/Library/Application Support/rencal/plugins.toml` |
| Linux | `~/.config/rencal/plugins.toml` |

```toml
plugins = [
  "gwenwindflower/rencal-theme-catppuccin-frappe"
]
```

For local development with live reloading, clone the repo and add the path to your `plugins.toml`:

```toml
plugins = [
  ...
  "/path/to/catppuccin-frappe"
]
```

renCal links the checkout into its plugins directory and reloads `themes/frappe.css` as you save it, so edits show up in the running app while Catppuccin Frappé is selected.

## Palette mapping

| renCal role | Frappé colour |
| --- | --- |
| Background | Base `#303446` |
| Sidebar, popovers, toasts | Mantle `#292c3c` |
| Tooltips | Surface 0 `#414559` |
| Text | Text `#c6d0f5` |
| Muted text | Subtext 0 `#a5adce`; Subtext 1 `#b5bfe2` on accent, selection and tooltip surfaces |
| Primary actions, focus ring, brand | Mauve `#ca9ee6`, with Base text on fills |
| Selection | Mauve at 16% |
| Today | Pink `#f4b8e4`, with Base text on the marker |
| Success, warning, error | Green `#a6d189`, Yellow `#e5c890`, Red `#e78284` |

Hover, card, border and input surfaces use renCal's own derivation from the Text colour. Calendar and event colours, typography, sizing and layout stay as renCal draws them.

## Contrast

The checked theme-token pairings, modelled from renCal 0.9.3 surface rules, meet WCAG 2 contrast: at least 4.5:1 for normal text and 3:1 for the focus ring. The model covers renCal's derived tints, hover fills and selection stacked on weekend columns. The tightest pairs are:

| Pair | Ratio |
| --- | --- |
| Selected muted text on a selected weekend column | 4.52 |
| Red as text on Base | 4.65 |
| Base text on a Red fill | 4.65 |
| Accent muted text on Base | 4.70 |

Rendering in the app has not been visually checked yet. That check includes event text, which renCal derives from user-supplied calendar colours rather than from this theme.

## Credits and license

The colours are Catppuccin's Frappé flavour from the official [palette](https://github.com/catppuccin/palette), following the Catppuccin [style guide](https://github.com/catppuccin/catppuccin/blob/main/docs/style-guide.md). The palette is MIT licensed, Copyright (c) 2021 Catppuccin; its full license notice is in [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).
