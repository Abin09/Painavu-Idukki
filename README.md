# Painavu Land Listing — GitHub Pages Deploy

## Files
- `index.html` — the entire site, including all photos embedded directly in the file (no separate assets folder needed)

## Deploy in 5 minutes
1. Create a new repo on GitHub, e.g. `painavu-land-listing`
2. Upload `index.html` to the repo (that's the only file you need)
3. Go to **Settings → Pages**
4. Under "Build and deployment", set **Source: Deploy from a branch**
5. Branch: `main`, folder: `/ (root)` → Save
6. Wait ~1 minute, then your site is live at:
   `https://<your-username>.github.io/painavu-land-listing/`

## Editing later
Everything (text, price, phone number, links) lives in `index.html` as plain HTML — open it in any text editor and edit the text directly. No build tools needed.

Photos are embedded as base64 data directly in the file, which is why there's no `assets/` folder — this keeps the site working reliably as a single file everywhere (including previews), at the cost of a larger HTML file (~2.4MB). To swap a photo, you'd need to re-encode a new image to base64 and replace the corresponding `data:image/jpeg;base64,...` block — happy to do that for you if you have a replacement photo.

## Custom domain (optional)
If you buy a domain later, add a `CNAME` file to the repo root containing just the domain name, then point your domain's DNS to GitHub Pages (Settings → Pages will show you the exact records once you add the domain there).
