# Avi Andargie — portfolio

A single static page. No build step, no dependencies, no framework.

```
index.html      the whole page (HTML + CSS + a few lines of JS)
img/            every screenshot the page uses
```

## Publish it on GitHub Pages

1. Create a new public repository, e.g. `avi` (the site will live at `https://<user>.github.io/avi/`).
   Name it `<user>.github.io` instead if you want it at the root domain.
2. Upload `index.html` and the `img/` folder to the repository root.
3. Repository → **Settings** → **Pages** → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → **Save**.
4. Wait about a minute, then open the URL GitHub shows on that page.

From a terminal instead:

```bash
git init
git add .
git commit -m "portfolio"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

## Edit it

Everything is in `index.html`.

- Colors live in the `:root` block at the top, once for light and once for dark.
- Fonts load from Google Fonts in the `<link>` at the top.
- Each project is one `<article class="case">`. Copy one, change the text and the image paths, and you have a seventh project.
- Images are plain `<img src="img/...">`. Drop a new file in `img/` and point at it.

## Custom domain

Settings → Pages → Custom domain. Add a `CNAME` file containing the domain, and point the domain's DNS at GitHub Pages.
