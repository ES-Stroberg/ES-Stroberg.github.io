# Simon Stroberg – static site (One.com export cleaned)

This repo contains a static export of the site originally made with One.com’s Web Editor.
The One.com-specific image-resizing URLs (`/____impro/...`) and root-absolute paths (`/onewebstatic/...`, `/onewebmedia/...`, `/index.html`, etc.)
have been rewritten to **portable relative paths** so the site can be hosted from any path (GitHub Pages, Netlify, S3, etc).

## Local preview
From the repo root:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

(Using a local server matters because some browsers block JS/CSS features when opening files via `file://`.)

## GitHub Pages
1. Push this repo to GitHub.
2. In **Settings → Pages**, choose:
   - Source: **Deploy from a branch**
   - Branch: `main` (or `master`) and `/ (root)`
3. Wait for Pages to publish.

If you use a custom domain, add a `CNAME` file with your domain name (and configure DNS per GitHub’s instructions).

## Notes
- `.nojekyll` is included so GitHub Pages serves files exactly as-is.
