# bimsarapathiraja.github.io

Plain static site: one `index.html`, images in `assets/img/`, the CV in `cv/`. No Jekyll, no build step.

## Deploy (recommended: a user site at the root URL)

1. On GitHub, create a **public** repository named exactly `bimsarapathiraja.github.io`.
2. Copy everything in this folder (including the hidden `.nojekyll` file) to the repository root and push to `main`.
3. Repository **Settings → Pages → Build and deployment**: Source "Deploy from a branch", branch `main`, folder `/ (root)`.
4. The site goes live at <https://bimsarapathiraja.github.io/> within a minute or two.
5. Optional: in the old `minimal-portfolio` repository, replace `index.md` with `redirect/index.html` (rename it to `index.html`) so old links forward to the new site. Delete the `redirect` folder from the new repository.

### If you would rather keep the old URL

Replace the contents of the `minimal-portfolio` repository with this folder instead. Then change the site URL in two places:

- `index.html`: the `canonical`, `og:url`, `og:image` and JSON-LD `url`/`image` values (search for `bimsarapathiraja.github.io/`).
- The CV: `\newcommand{\website}` and `\newcommand{\websitetext}` near the top of `Bimsara_Pathiraja_CV.tex`.

## Editing

- **News item:** add an `<li>` at the top of the `<ul class="news">` list.
- **Publication:** copy one `<li class="paper">…</li>` block. For a paper without a figure, keep the empty `<div class="fig" aria-hidden="true"></div>` so the text stays aligned. Mark yourself with `<span class="me">Bimsara Pathiraja</span>`.
- **Figures:** put a 3:2-ish image in `assets/img/pubs/` and point the `<img src>` at it. It is shown at 200 x 130 px, scaled to fit.
- **CV:** replace `cv/Bimsara_Pathiraja_CV.pdf` with the newly compiled *public* copy (same file name, so every link keeps working).
- **Colours and font:** the `:root` block at the top of the `<style>` tag.
