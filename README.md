# Philips Akinbami — Portfolio

Static portfolio site. Plain HTML + Tailwind (via CDN, so there is no build step). Just edit the files and push.

## Files

```
index.html            → landing page
projects/mawi.html    → Network Traffic Measurement & Analysis writeup
projects/uav.html     → UAV Communications writeup
assets/resume.pdf     → downloadable résumé (linked from every page)
.nojekyll             → tells GitHub Pages to serve files as-is
```

## Deploy to GitHub Pages (free github.io URL)

1. Create a GitHub account and pick a professional username, e.g. `philips-akinbami` or `philipsakinbami`.
2. Create a new **public** repository named exactly `<username>.github.io` (this is what gives you the clean root URL).
3. Put every file in this folder at the **root** of that repo (`index.html` must be at the top level, not inside a subfolder).
4. Commit and push to the `main` branch.
5. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
6. Wait about a minute. Your site is live at `https://<username>.github.io`.

Git commands:

```bash
git init
git add .
git commit -m "portfolio: initial site"
git branch -M main
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```

## After it's live — two edits

- In `index.html`, replace both `https://github.com/USERNAME` links with your real profile URL.
- Add the live URL (`<username>.github.io`) to the header of your résumé.

## Add a new project later

1. Copy `projects/mawi.html` to `projects/your-project.html` and edit the title, meta, numbers, and writeup.
2. On `index.html`, duplicate one of the two project `<a>` cards in the Projects section and point it at your new page.
3. Drop screenshots into `assets/` and swap them into the dashed "artifact" placeholders.

## Notes

- The Tailwind config and custom styles are inlined in each page's `<head>`, so every page stands alone.
- Fonts: Sora (display), IBM Plex Sans (body), IBM Plex Mono (labels/data), loaded from Google Fonts.
- Motion respects `prefers-reduced-motion`.
