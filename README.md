# Franck Migone — personal website

Source files for [fajzmigone.github.io](https://fajzmigone.github.io), built with
[Quarto](https://quarto.org/) and published from the `docs/` directory.

## Local preview

```powershell
quarto preview
```

## Build

```powershell
quarto render
```

## Publishing

`quarto render` writes the site to `docs/`, which GitHub Pages serves directly.
Commit both the sources and the regenerated `docs/` — there is no CI workflow, so
a change that is not rendered will not go live.

## Layout

- `index.qmd`, `research/`, `Useful_Ressources/`, `cv/`, `404.qmd` — the pages,
  listed explicitly under `project: render:` in `_quarto.yml`
- `html/styles.scss` — the only custom stylesheet, layered on the `pulse` theme
- `html/head.html` — favicons and the JSON-LD `Person` block, injected into every page
- `img/` — only the assets actually served: profile photo and favicons

## Maintenance

The footer copyright year is hardcoded in `_quarto.yml` (`page-footer: left:`) —
bump it each January.
