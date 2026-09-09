# Personal academic homepage

A single-file academic homepage, laid out like the Hugo Blox "academic resume" theme
(profile card on the left, biography and sections on the right).
No build step, no dependencies — GitHub Pages serves `index.html` directly.

## Publish on GitHub Pages

1. Create a public repository named **`USERNAME.github.io`** (replace `USERNAME`
   with your GitHub username — the repo name must match exactly).
2. Upload `index.html`, `avatar.jpg`, and `Jihyung_Kim_CV.pdf` to the repository root.
3. Go to **Settings → Pages**, set *Source* to **Deploy from a branch**,
   branch **main**, folder **/ (root)**, and save.
4. The site appears at `https://USERNAME.github.io` within a couple of minutes.

To use a repo with a different name, the site will live at
`https://USERNAME.github.io/REPO-NAME/` instead.

## Before publishing — fill these in

Search `index.html` for `USERNAME` and replace it in two links:

| Line | What to change |
|---|---|
| GitHub icon | `https://github.com/USERNAME` |
| LinkedIn icon | `https://www.linkedin.com/in/USERNAME/` |

Other things to check:

- **Photo.** `avatar.jpg` is already in place (800×800, cropped and set on a white
  background). To swap it, replace that file with another square image — the page
  clips it to a circle, so keep the face near the centre.
- **CV.** The document icon links to `Jihyung_Kim_CV.pdf` in the repo root.
  Re-upload that file whenever the CV changes.
- **Scholar / X.** No links were added, since there is no profile yet. To add one,
  copy an existing `<a>` block inside `<div class="icons">` and swap the URL.

## Editing the content

Everything is in `index.html` — the CSS is in the `<style>` block at the top, the
content is plain HTML below it.

- **News** — add a `<li>` at the top of the `#news` list; newest first.
- **Research** — each entry is a `.item` block. The `<span class="tag">In progress</span>`
  marker is optional; drop it once a paper is submitted, or change the text to
  the venue. When you have publications, an author line and an
  `<a href="...">Arxiv</a>` link go in the `.meta` paragraph.
- **Colors** — the accent color is the `--accent` variable at the top of the
  `<style>` block (currently the teal used in the CV). Dark-mode values are in the
  `html[data-theme="dark"]` block below it.

The page always opens in light mode; the moon button switches to dark. The choice
is not remembered between visits (browser storage is deliberately not used).
