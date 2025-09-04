# Snailkarts – Engineered to Drift
Marketing site for Snailkarts: S-kart-Go (gas) and Es-kart-Go (electric, coming soon).  
Live site: https://snailkarts.com

## Contents
- `index.html` – single-page app with hash routing (`#home`, `#karts`, `#gallery`, `#build`, `#contact`)
- `style.css` – neon theme, responsive layout, background video sections
- Favicons: `favicon.ico`, `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png`, `site.webmanifest`

## Features
- Fullscreen background video on **Karts**, **Gallery**, **Build**
- Image masonry Gallery
- Build Sheet Form (Formspree) → sends spec + contact info
- Contact Form (Formspree)
- Social links: Instagram, YouTube, TikTok
- Testimonials section
- Mobile nav + auto-pausing videos on hidden tabs

## Edit & Run
This is a static site—no build step required.
- Edit HTML/CSS directly on GitHub or locally and push.
- Open `index.html` in a browser to preview locally (videos require files to be reachable via HTTPS if using remote URLs).

## Deploy (GitHub Pages)
1. Repo **Settings → Pages**  
   - Source: `main` (or `master`) branch → `/root`
2. If using a custom domain:
   - Set **Custom domain**: `snailkarts.com` (and optional `www.snailkarts.com`)
   - In Namecheap DNS:
     - Apex `@` → A records for GitHub Pages: `185.199.108.153`, `...109.153`, `...110.153`, `...111.153`
     - `www` → CNAME → `snailkarts.github.io`
   - Wait for DNS to propagate, then enable **Enforce HTTPS**.

## Forms (Formspree)
- Endpoint: `https://formspree.io/f/xandlqzb`
- Add allowed domains in Formspree: `snailkarts.com`, `www.snailkarts.com`
- Test by submitting the **Contact** or **Build** forms on the live site.

## Payments (future)
- Recommended: Stripe **Payment Links** or **Buy Button** (no backend).  
- Connect Stripe → QuickBooks via the QuickBooks Stripe app or a connector (Synder/A2X/Bookkeep).

## Updating Media
- Background videos:
  - Home: `assets.codepen.io/.../469ec902-...mp4`
  - Karts: `.../bbfbad66-...mp4`
  - Gallery: `.../72ba602c-...mp4`
  - Build: `.../VideoAug30...mov`
- Swap sources in the corresponding `<video>` elements in `index.html`.

## Cache Busting (optional)
If an update doesn’t show right away, append a version query string to CSS:
```html
<link rel="stylesheet" href="style.css?v=2">
