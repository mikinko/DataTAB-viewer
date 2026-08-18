<p align="center"><img src="assets/banner.jpg" alt="DataTab — Total Commander plugin" width="100%"></p>

# DataTab

**DataTab** is a Lister (WLX) plugin for [Total Commander](https://www.ghisler.com/)
that turns CSV/TSV, JSON and XML files into an interactive, editable table
instead of raw text — press <kbd>F3</kbd> on a file and get a spreadsheet-like
grid or a structured outline, right inside Lister.

It replaces three older single-format plugins (csvtab / jsontab / xmltab)
with one shared engine, so all three formats get the same filtering,
sorting, editing, theming and font handling.

## What it does

- **Grid view** for CSV/TSV — sortable, filterable columns with per-column
  filter boxes, decimal-aligned numeric columns, natural sort, and a status
  bar showing row counts, delimiter and encoding.
- **Outline view** for JSON and XML — every node (object, array, element,
  attribute) as a Name/Value row, expand/collapse, with values wrapped for
  reading in a value pane below the grid.
- **Record table** — when a document contains a repeated list (an array of
  similar objects, or an element repeated as siblings), DataTab can project
  just that list as a normal sortable/filterable table instead of the full
  tree — the status bar tells you when one is available (<kbd>Ctrl+T</kbd>
  to switch).
- **Editing** — cells are editable in place; saves are lossless: untouched
  parts of the file are copied byte-for-byte, only the cells you changed are
  rewritten. Works for CSV rows, JSON values and XML element/attribute text.
- **Source tab** — the raw file with syntax highlighting (CSV/JSON/XML),
  line numbers and "Locate in source" to jump from a row/node straight to
  its position in the text.
- **Copy node as** JSON, XML or JSON Path/XPath from any outline node.
- **Themes** — five built-in presets (Light, Paper, Dark, Midnight,
  Solarized Dark), or override any individual color.
- **Fonts** — a standard Windows font picker for both the grid and the
  source view, remembered between sessions.
- **Large files** — spans into the decoded file instead of per-cell copies,
  background indexing with progressive display, and filtering that stays
  responsive well past a million rows.

## Supported files

CSV, TSV, TAB · JSON, JSONL/NDJSON, GeoJSON, JSONC, JSON5 · XML and the
XML-family formats that are really XML underneath — SVG, XSD, XSLT, RSS,
GPX, KML, OSM, `.config`/`.manifest`/`.resx`/`.csproj`/`.props` and similar
project/config files, WSDL, PLIST, ATOM, and a few more. Unrecognized
extensions are still opened if the content itself looks like JSON or XML.

## Screenshots

Themed Lister views, opened directly from Total Commander:

| CSV grid | JSON outline |
|---|---|
| ![CSV grid view](scrshot/csv.png) | ![JSON outline view](scrshot/JSON.png) |

| XML outline (dark theme) | JSONL, "copy node as" |
|---|---|
| ![XML outline view](scrshot/xml.png) | ![JSONL outline view](scrshot/jsonl.png) |

## Requirements

Total Commander, x64. DataTab ships as a single `datatab.wlx64` Lister
plugin.
