# chatt-site

Landing page for the ChatT messenger app — plain static HTML/CSS, no build step.

Served by GitHub Pages from the `main` branch root. `.nojekyll` disables Jekyll processing.

## Structure

- `index.html` — the whole site
- `styles.css` — all styling (mobile-first, dark)
- `assets/appicon.svg` — app icon (copied from the app repo)
- `assets/fonts/Inter-Variable.woff2` — Inter variable font (copied from the app repo)

## Local preview

```sh
python3 -m http.server 8471
# open http://localhost:8471
```

## TODO

- [ ] Android testers Google Group URL (search `TODO` in `index.html`), then enable the
      step-1 link and swap the disabled button for a real "Join the Android beta" CTA
- [ ] `og:image` (raster) for link previews
- [ ] Custom domain: add `CNAME` file + configure in repo settings
