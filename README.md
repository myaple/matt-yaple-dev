# matt.yaple.dev

Personal site for Matt Yaple — single-page static site, hand-written HTML/CSS, no build step.

- **Hosting:** Cloudflare Workers (static assets), custom domain `matt.yaple.dev`
- **Deploy:** push to `main` → GitHub Actions → `wrangler deploy` (`.github/workflows/deploy.yml`)
- **Config:** `wrangler.toml` (assets-only, `workers_dev = false`, 404 via `404.html`)

## Local preview

```sh
cd site && python3 -m http.server 8080
# open http://localhost:8080
```

Edit `site/index.html` / `site/assets/styles.css`, commit, push — the site redeploys automatically.
