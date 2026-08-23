# sean-xr.github.io

Personal academic website — plain HTML and CSS, no build step, no dependencies.

## Files

| Path | What it is |
|---|---|
| `index.html` | The entire page. All content lives here. |
| `style.css` | All styling. The colour palette is in the `:root` blocks at the top. |
| `assets/images/profile.jpg` | Your photo. Square works best (600×600 or larger). |
| `assets/images/favicon.svg` | Browser tab icon. |
| `assets/thumbs/*.png` | Paper teaser images, ~600×340. |
| `assets/cv.pdf` | Your CV. |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is instead of running Jekyll. |

## Editing

**Preview locally** — open `index.html` in a browser, or:

```
python3 -m http.server 8000
```

then visit http://localhost:8000.

**Add a news item** — copy a line in the `<ul class="news-list">` block. Newest goes on top.

**Add a paper** — copy an `<article class="pub">` block in the publications section and edit it.
Drop the teaser in `assets/thumbs/`. Wrap your own name in `<span class="me">Rui Xiao</span>`
so it renders bold. Add `<span class="badge">Oral</span>` after the venue for highlights.

**Replace an image** — overwrite the file, keep the same filename, and the HTML needs no change.

**Change colours** — edit the `--accent`, `--bg`, `--text` variables in the two `:root` blocks
at the top of `style.css`. The first block is light mode, the others are dark mode.

## Deploying

The site is static, so GitHub Pages serves it directly:

1. Push this repo to GitHub as **`sean-xr.github.io`** (the repo name must match the username
   exactly for the site to live at the root domain).
2. Repo → Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)`.
3. It goes live at https://sean-xr.github.io within a minute or two.
