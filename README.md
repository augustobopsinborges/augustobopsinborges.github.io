# augustobopsinborges.github.io

Personal and professional website of Augusto Bopsin Borges, built with
[Quarto](https://quarto.org).

## Layout

| Path | Content |
|---|---|
| `_quarto.yml` | site configuration: navigation, footer, theme files |
| `index.qmd` | home page: hero, research interests, latest posts, publications, software |
| `research.qmd`, `publications.qmd`, `software.qmd`, `about.qmd` | the research pages |
| `blog/index.qmd` | blog listing (also publishes the RSS feed `blog/index.xml`) |
| `blog/posts/<date>-<slug>/index.qmd` | one folder per post |
| `_theme/` | design tokens and styles (`base.scss` shared, `light.scss`, `dark.scss`), fonts (`head.html`) |
| `files/` | downloadable files (BibTeX, PDFs) |
| `images/` | favicon and portrait |
| `.github/workflows/publish.yml` | renders on every push to `main` and publishes to the `gh-pages` branch |

## Writing

Preview locally (needs [Quarto](https://quarto.org/docs/get-started/)):

```bash
quarto preview
```

New post: copy `blog/posts/2026-11-08-hello/` to `blog/posts/<yyyy-mm-dd>-<slug>/`,
edit the front matter (`title`, `description`, `date`, `categories`) and write.
Mathematics is written in LaTeX between `$…$` or `$$…$$`; code chunks in Python or
Julia are executed at render time and cached by `freeze: auto`.

## Publishing

1. Push to `main`; the workflow renders the site and commits it to `gh-pages`.
2. In the repository settings, point GitHub Pages to the `gh-pages` branch (root).

The site is served at the address in `site-url` (`_quarto.yml`). A GitHub *user*
page is only served at `<username>.github.io`; for any other name a custom
domain (`CNAME`) is needed.
