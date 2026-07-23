# chatt-site

Landing page for the ChatT messenger app — plain static HTML/CSS, no build step.

Served by GitHub Pages from the `main` branch root. `.nojekyll` disables Jekyll processing.

## Structure

- `index.html` — the whole site
- `styles.css` — all styling (mobile-first, dark)
- `assets/appicon.svg` — app icon (copied from the app repo)
- `assets/fonts/Inter-Variable.woff2` — Inter variable font (copied from the app repo)
- `CNAME` — custom domain (`chatty.pk`) for GitHub Pages
- `.well-known/apple-app-site-association` — iOS universal links (app ID `A468T66XSK.com.computism.chatt`)
- `.well-known/assetlinks.json` — Android app links (`com.computism.chatt`)

The `.well-known` files were moved here from the VM (`/var/www/chatty.pk`, served by
`big-chat/infra/nginx/pk/*.conf.template`) so chatty.pk can point at this site instead.

## Local preview

```sh
python3 -m http.server 8471
# open http://localhost:8471
```

## TODO

- [ ] `og:image` (raster) for link previews
- [ ] Custom domain: `CNAME` file added; still need to set it in repo settings
      (Pages → Custom domain, enable HTTPS) and point chatty.pk DNS at GitHub Pages
- [ ] After the DNS switch, verify `https://chatty.pk/.well-known/apple-app-site-association`
      and `assetlinks.json` still resolve, then drop the `.well-known` locations from
      the nginx configs in big-chat
