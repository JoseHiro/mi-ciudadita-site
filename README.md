# Mi Ciudadita — Static Landing Site

Simple 3-page static site:

- `/` — Marketing landing (index.html)
- `/privacy` — Privacy Policy (bilingual EN/ES)
- `/terms` — Terms of Use (bilingual EN/ES)

No build step, no framework. Pure HTML + CSS.

---

## Deployment options

### Option A: Cloudflare Pages (recommended, free)

1. Push this repo to GitHub (already there)
2. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages** → **Create → Pages** → **Connect to Git**
3. Select the `gdl-weather` repo
4. Build settings:
   - **Framework preset**: None
   - **Build command**: (leave empty)
   - **Build output directory**: `site`
5. Deploy. Cloudflare gives you a `*.pages.dev` URL immediately.
6. Add custom domain `miciudadita.app` in the Pages settings once you own it.

### Option B: GitHub Pages

1. Settings → Pages → **Deploy from a branch**
2. Branch: `master`, Folder: `/site`
3. URL: `https://josehiro.github.io/gdl-weather/`
4. Custom domain (miciudadita.app) can be added later.

### Option C: Vercel / Netlify

Import the repo, set output dir to `site/`, done. Both are free for personal use.

---

## URLs to use in App Store Connect

Once deployed, plug these into App Store Connect:

- **Privacy Policy URL**: `https://miciudadita.app/privacy` (or the temporary `*.pages.dev` URL)
- **Marketing URL**: `https://miciudadita.app`
- **Support URL**: `https://miciudadita.app` (or a mailto: link)
- **Terms of Use**: linked from Paywall description (`https://miciudadita.app/terms`)

---

## Update `support@miciudadita.app`

Search-and-replace across `site/**/*.html` if your support email is different. The address only shows on:

- Privacy Policy contact section
- Terms of Use contact section
- Landing page footer

## Ownership of `miciudadita.app` domain

Not yet registered — recommended registrars: Cloudflare Registrar (at-cost), Porkbun, Namecheap. Once registered, add to Cloudflare Pages custom domain config for free HTTPS.
