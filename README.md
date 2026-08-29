# ComicLand website

A single static page (`index.html` + `assets/`) — no build step, no dependencies.

## Publish it free on GitHub Pages

1. Create a new **public** GitHub repo (e.g. `comicland-site`), or reuse an existing one.
2. Copy `index.html` and the `assets/` folder into the repo root and push:
   ```bash
   git init
   git add index.html assets
   git commit -m "ComicLand site"
   git branch -M main
   git remote add origin git@github.com:<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: repo → **Settings** → **Pages** → under "Build and deployment", set **Source** to "Deploy from a branch", branch **main**, folder **/ (root)** → **Save**.
4. GitHub gives you a URL like `https://<your-username>.github.io/<repo-name>/` within a minute or two.

### Custom domain (optional)
If you want `comiclandapp.com` (or similar) instead of the `github.io` URL: add a `CNAME` file to the repo root containing just your domain, and point your domain's DNS at GitHub Pages (an `A` record to GitHub's IPs, or a `CNAME` record to `<your-username>.github.io` for a subdomain) — GitHub's Pages docs walk through the exact DNS records.

## Editing

- All copy is plain HTML in `index.html` — no template system, just edit the text directly.
- The "ComicLand" and "Features" headings are pre-rendered images (`assets/img/wordmark.png`, `assets/img/features-title.png`) using the app's own Comix Loud font — regenerate them (via any tool that can render that font to an image) if you need to change the wording, since the text isn't live/editable there.
- Screenshots (`assets/img/screenshot-*.jpg`) are from the current build; swap in new ones the same way if the UI changes significantly.
- The "Download on the App Store" button is a plain styled link, not Apple's official badge — swap in Apple's actual SVG/PNG from their [marketing resources page](https://developer.apple.com/app-store/marketing/guidelines/) if you'd rather use that.
