# Accounting Analytics with Python — Quarto Book Project

## Folder contents
- `_quarto.yml` — book configuration (title, chapter order, HTML + PDF output formats)
- `index.qmd` — preface
- `01-...qmd` through `16-...qmd` — one file per chapter (currently just a heading; add content as you write)
- `references.qmd` / `references.bib` — bibliography

## One-time setup
1. Install [Quarto](https://quarto.org/docs/get-started/).
2. Install Python + Jupyter (e.g., via `pip install jupyter pandas numpy matplotlib`) so Quarto can execute Python code chunks.
3. For PDF output, install TinyTeX (Quarto can do this for you):
   ```
   quarto install tinytex
   ```

## Rendering the book
From inside this folder:

```bash
quarto render
```

This produces both HTML and PDF versions in a `_book/` folder (per `output-dir` in `_quarto.yml`):
- `_book/index.html` — browsable HTML site you can post online or share as a folder
- `_book/Accounting-Analytics-with-Python.pdf` — single PDF file

To preview live while editing:
```bash
quarto preview
```

## Adding a new chapter
1. Create a new `.qmd` file (e.g., `17-new-topic.qmd`) with a top-level `# Heading`.
2. Add its filename to the `chapters:` list in `_quarto.yml` in the position you want it to appear.

## Notes
- Chapter numbering in the book is automatic based on order in `_quarto.yml`, not the filenames — the numeric prefixes on filenames are just for your own organization.
- `execute: freeze: auto` in `_quarto.yml` means code chunks only re-run when a chapter's content changes, which keeps renders fast once you have many chapters with code.
