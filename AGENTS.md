# AGENTS.md

## Cursor Cloud specific instructions

This is a **Quarto static website** (personal portfolio/blog). The only build tool required is the [Quarto CLI](https://quarto.org/).

### Key commands

| Task | Command |
|------|---------|
| Build site | `quarto render` |
| Dev preview (live-reload) | `quarto preview --port 4200 --no-browser` |
| Check Quarto version | `quarto --version` |

- Output goes to `docs/` (committed to repo, served via GitHub Pages).
- There are no linters, test frameworks, or package managers — Quarto is the single dependency.
- The `_quarto.yml` file configures the project; `.qmd` files are the source content.

### Gotchas

- `quarto preview` binds to all interfaces by default; use `--port` to pick a specific port and `--no-browser` in headless environments.
- One `.qmd` file (`blogs/DEL_Model/DEL_modelling.qmd`) triggers a non-fatal warning about `:::` fenced divs — this is harmless and does not block the build.
- No R or Python kernels are needed; the site is pure Quarto Markdown with LaTeX math.
