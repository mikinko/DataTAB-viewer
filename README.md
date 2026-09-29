<p align="center"><img src="assets/banner.jpg" alt="DataTab — Total Commander plugin" width="100%"></p>

# DataTab

## News

**2026-09-29 — DataTab 1.4**

- **32-bit version.** DataTab now runs in 32-bit Total Commander as well as
  64-bit (`datatab.wlx` next to `datatab.wlx64`, one package).
- **More file types:** YAML (`.yaml`, `.yml`, `.clang-format`,
  `.clang-tidy`), TOML, INI (`.ini`, `.editorconfig`), Java `.properties`
  and `.env` files. They open in the same outline as JSON, and edits keep
  their comments and layout.
- **Rename keys** in the outline, and **Copy node as YAML** from any format.
- **Wildcards** (`*`, `?`) in the filter boxes.
- A file too large for the available memory now gives a clear message
  instead of taking Total Commander down.

---

**DataTab** is a Lister (WLX) plugin for [Total Commander](https://www.ghisler.com/)
that turns CSV/TSV, JSON, XML, YAML, TOML, INI, `.properties` and `.env` files
into an interactive, editable table instead of raw text. Press <kbd>F3</kbd>
on a file to get a spreadsheet-like grid or a structured outline, right
inside Lister.

It replaces three older single-format plugins (csvtab, jsontab and xmltab)
with one shared engine, so every format gets the same filtering, sorting,
editing, theming and font handling.

## What it does

- **Grid view** for CSV/TSV: sortable columns with a filter box on each,
  decimal-aligned numbers, natural sort, and a status bar showing row counts,
  delimiter and encoding.
- **Outline view** for JSON, XML, YAML, TOML, INI, `.properties` and
  `.env`. Every node (object, array, element, attribute, key) is a
  Name/Value row that can be expanded and collapsed. A value pane below the
  grid shows long values wrapped.
- **Record table:** when a document contains a repeated list (an array of
  similar objects, an element repeated as siblings, or a TOML array of
  tables), DataTab can show just that list as a normal sortable, filterable
  table. The status bar tells you when one is available; <kbd>Ctrl+T</kbd>
  switches to it.
- **Filtering:** "contains", `=` exact, `!` not, `<` / `>` comparisons, and
  `*` / `?` wildcards. Filters either hide non-matching rows or jump to the
  next match.
- **Editing:** cells are edited in place, and saving is lossless. Only the
  values you changed are rewritten; the rest of the file stays byte for byte
  the same, so comments and layout in config files survive. Keys can be
  renamed too, in every format except XML.
- **Source tab:** the raw file with syntax highlighting for every supported
  format, line numbers, and *Locate in source*, which jumps from a row or
  node to its position in the text.
- **Copy node as** JSON, XML, YAML, or JSON Path/XPath from any outline
  node, so converting a piece of one format into another is one copy.
- **Themes:** nine built-in presets. The light ones are Light, Paper, Frost
  and Solarized Light; the dark ones are Dark, Midnight, Solarized Dark,
  Nord and Monokai. Any individual color can be overridden.
- **Fonts:** a standard Windows font picker for both the grid and the source
  view, remembered between sessions.
- **Large files:** loading runs in the background, and filtering stays
  responsive well past a million rows.

## Supported files

- **Tables:** CSV, TSV, TAB.
- **JSON:** JSON, JSONL/NDJSON, GeoJSON, HAR, JSONC, JSON5.
- **XML** and the formats that are really XML underneath: SVG, XSD, XSL/XSLT,
  RSS, ATOM, GPX, KML, OSM, `.config`, `.manifest`, `.nuspec`, `.resx`,
  `.xaml`, `.csproj`/`.vbproj`/`.vcxproj`, `.props`, `.targets`, WSDL, PLIST,
  DGML, XLF/XLIFF, `.runsettings`.
- **YAML:** YAML/YML, `.clang-format`, `.clang-tidy`. Anchors, merge keys,
  complex keys and multi-document files are supported.
- **Config files:** TOML, INI, `.editorconfig`, Java `.properties`, `.env`
  (including `.env.local` and similar).

Files with an unrecognized extension still open if their content looks like
JSON, XML or YAML.

## Screenshots

Themed Lister views, opened directly from Total Commander:

| CSV grid | JSON outline |
|---|---|
| ![CSV grid view](scrshot/csv.png) | ![JSON outline view](scrshot/JSON.png) |

| XML outline (dark theme) | JSONL, "copy node as" |
|---|---|
| ![XML outline view](scrshot/xml.png) | ![JSONL outline view](scrshot/jsonl.png) |

## Requirements

Total Commander, 64-bit or 32-bit. DataTab ships as `datatab.wlx64` and
`datatab.wlx` in one package; Total Commander's plugin installer picks the
one it needs. The 32-bit version opens files up to 256 MiB by default,
because it has at most 2 GB of memory to work with (`max-file-size` in the
ini changes the limit).
