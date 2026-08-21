# HFAF Repository Architecture

Human First, AI Forward uses a two-layer structure so research/source materials and the public website do not get mixed together.

## 1. Canonical source layer

These files are the editable source of truth for the project:

- `MANIFESTO.md` — foundational manifesto
- `01-framework/` — core HFAF models and principles
- `02-higher-education/` — higher-education implementation materials
- `03-workshop/` — workshop source materials
- `04-research/` — research agenda and bibliography
- `05-case-studies/` — implementation evidence as it develops
- `06-tools/` — reusable tools and canvases
- `07-essays/` — canonical essay source files
- `FACULTY-PACK.md` — faculty resource index
- `PUBLICATION-ROADMAP.md` — publication and release plan
- `CITATION.cff` — citation metadata

These Markdown files are designed for version control, collaboration, research transparency, and future releases.

## 2. Public website layer

GitHub Pages publishes **only** from `main` → `/docs`.

Everything inside `docs/` is public-facing website material:

- `docs/index.html` — homepage
- `docs/manifesto.html` — The Human Remains manifesto
- `docs/framework.html` — Human–AI Agency Loop
- `docs/spectrum.html` — Human–AI Use Spectrum
- `docs/faculty-guide.html` — higher-education faculty guide
- `docs/course-design-canvas.html` — course design canvas
- `docs/workshop.html` — faculty workshop
- `docs/research.html` — research questions and bibliography
- `docs/publication-roadmap.html` — public roadmap
- `docs/essay-the-human-remains.html` — Essay 01
- `docs/styles.css` — shared visual system
- `docs/404.html` — public-site fallback page
- `docs/.nojekyll` — serves the site as plain static files

## Rules for future updates

1. **Do not link public website visitors directly to Markdown files** unless the explicit purpose is to show source material on GitHub.
2. **Do not create another root `index.html`.** The website source is `/docs` only.
3. When a canonical Markdown document changes materially, update its corresponding HTML page in `/docs`.
4. Internal website links should use relative `.html` paths such as `framework.html`, not repository paths such as `01-framework/framework.md`.
5. GitHub/repository links are appropriate only when inviting visitors to inspect source, history, or contribute.
6. Research claims and HFAF conceptual propositions must remain clearly distinguishable.
7. Stable downloadable releases should eventually be versioned and archived separately from the living website.

## Deployment

GitHub Pages configuration:

- Branch: `main`
- Folder: `/docs`

Public site:

https://iamlegend-imani.github.io/HFAF-Human-First-AI-Forward/

This architecture intentionally separates **what we author and version** from **what a public reader experiences**.
