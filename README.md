# It's All Good Productions — Website

## Files in this project

```
iag-website/
├── index.html       ← The full website
├── sitemap.xml      ← For Google indexing
├── robots.txt       ← Tells search engines what to crawl
├── netlify.toml     ← Netlify config (redirects, headers, caching)
└── README.md        ← You're reading it
```

---

## STEP 1 — Set your contact email

Before deploying, set where form submissions go:

1. Open `netlify.toml`
2. Note the comment about `YOUR_EMAIL_HERE`
3. You can set this in the Netlify dashboard after deploy:
   - Go to **Forms** → **contact** → **Form notifications** → **Add notification** → **Email notification**
   - Enter the email where you want project inquiries delivered

---

## STEP 2 — Deploy to Netlify (2 options)

### Option A — Drag & Drop (fastest, no account needed to start)
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag this entire `iag-website` folder onto the page
3. You'll get a live URL instantly (e.g. `amazing-curie-abc123.netlify.app`)
4. Create a free Netlify account to claim it and connect your domain

### Option B — GitHub + Netlify (recommended for ongoing updates)
1. Create a free GitHub account if you don't have one
2. Create a new repository called `iag-website`
3. Upload these files to the repo
4. Go to [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import from GitHub**
5. Select the repo — Netlify auto-detects everything from `netlify.toml`
6. Hit **Deploy** — done

---

## STEP 3 — Connect your domain

1. In Netlify dashboard → **Domain management** → **Add custom domain**
2. Type: `itsallgoodproductions.com`
3. Netlify will show you nameservers to update
4. Go to wherever your domain is registered (GoDaddy, Namecheap, Google Domains, etc.)
5. Update the nameservers to Netlify's
6. Wait up to 24 hours (usually under an hour)
7. Netlify auto-provisions a free SSL certificate

---

## STEP 4 — Cancel Wix

Only do this AFTER confirming the site is live at your domain.

---

## STEP 5 — Submit to Google Search Console

1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Add property → enter `https://www.itsallgoodproductions.com`
3. Verify via Netlify (add the meta tag Netlify tells you to use in the `<head>`)
4. Submit your sitemap: `https://www.itsallgoodproductions.com/sitemap.xml`
5. Google will start indexing within a few days

---

## STEP 6 — Things to update over time

- **`og-image.jpg`** — Add a 1200×630px image to the root folder for social sharing previews. A screenshot of the hero section works great.
- **`favicon.png`** — Add a 32×32px favicon (your logo mark works)
- **`apple-touch-icon.png`** — 180×180px version for iOS home screen bookmarks
- **Logo images** — Currently pulling from Wix CDN. After canceling Wix, download your logo file and host it in this folder, then update the `src` in `index.html`

---

## Claude Code prompt (if you want to enhance it further)

Copy and paste this into Claude Code after navigating to this folder:

```
I have a production-ready static website in this folder for It's All Good Productions, a video production company in Los Angeles. The site is built in plain HTML/CSS/JS with Netlify Forms already wired up.

Here's what I'd like you to do:
1. Add a hamburger menu for mobile (the nav links are hidden on small screens right now)
2. Add lazy loading and a blur-up placeholder effect for images so the page feels fast
3. Add smooth scroll-triggered fade-in animations for each section as the user scrolls down
4. Check the Lighthouse score and fix any accessibility issues (aria labels, contrast, etc.)
5. Make sure all external image URLs are loading — if any 404, replace with a neutral placeholder
6. Add a Google Analytics script placeholder in the <head> with a comment showing where to put the GA4 measurement ID

Keep all the existing design, copy, and functionality exactly as-is.
```

---

## SEO already built in

- ✅ Title tag optimized for "video production Los Angeles"
- ✅ Meta description under 160 characters
- ✅ Open Graph tags for Facebook/LinkedIn sharing
- ✅ Twitter Card tags
- ✅ JSON-LD structured data (VideoProductionCompany schema)
- ✅ Canonical URL set
- ✅ All images have descriptive alt text
- ✅ Lazy loading on below-fold images
- ✅ Semantic HTML (h1, h2, main, nav, footer, section)
- ✅ sitemap.xml submitted-ready
- ✅ robots.txt configured
- ✅ Security headers via netlify.toml
- ✅ Static asset caching headers

---

*Built with Claude · June 2026*
