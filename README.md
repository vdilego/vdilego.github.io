# vdilego.github.io

Personal academic website of **Vanessa Di Lego**, Professor of Demography at Cedeplar/FACE/UFMG.

Live site: <https://vdilego.github.io>

---

## Tech stack

This site is built with [Quarto](https://quarto.org/), version ≥ 1.4.  
It replaces the previous `distill` site. Output goes to `docs/` for GitHub Pages.

---

## Setup (first time)

1. Install [R](https://cran.r-project.org/) and [Quarto](https://quarto.org/docs/get-started/).
2. Clone the repository:
   ```bash
   git clone https://github.com/vdilego/vdilego.github.io.git
   cd vdilego.github.io
   ```
3. Preview locally:
   ```bash
   quarto preview
   ```
4. Build to `docs/`:
   ```bash
   quarto render
   ```

---

## File map — where to edit things

| What you want to change | File |
|---|---|
| Your name / affiliation / links | `index.qmd` and `about.qmd` |
| Bio text | `about.qmd` |
| Publications | `publications.qmd` |
| Research areas | `research.qmd` |
| Teaching | `teaching.qmd` |
| Talks | `talks.qmd` |
| CV link / PDF | `cv.qmd` + replace `cv.pdf` in root |
| Blog post | Add a new `.qmd` file in `blog/posts/` |
| Navigation / footer | `_quarto.yml` |
| Fonts / colours | `custom.scss` |
| Your photo | Replace `photo_me.jpg` in root |

---

## Adding a blog post

Create a new file `blog/posts/my-post-title.qmd` with this YAML header:

```yaml
---
title: "My Post Title"
date: 2025-06-01
categories: [R, methods]
description: "One sentence summary shown in the listing."
---
```

Then write in Markdown below. Run `quarto render` or `quarto preview` to see it.

---

## Deploying

GitHub Pages is configured to serve from the `docs/` folder on the `main` branch.

After editing:
```bash
quarto render          # builds to docs/
git add -A
git commit -m "update: brief description"
git push
```

The site updates automatically within a minute.

---

## GitHub Pages setting

In your repository settings → Pages → Source:  
**Branch:** `main` | **Folder:** `/docs`

---

## Updating your photo

Replace `photo_me.jpg` in the repository root with your photo file (keep the same filename, or update the reference in `index.qmd` and `about.qmd`).
