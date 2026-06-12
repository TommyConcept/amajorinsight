# A Major Insight — Website

## Two Versions Included

1. **`index_standalone.html`** — a single self-contained file with all CSS, JavaScript, and images embedded inline. Open this directly in any browser, or use it for the Claude artifact preview — it works with zero external dependencies. This is the easiest way to preview the site immediately.

2. **`index.html` + `styles.css` + `script.js` + `images/`** — the production-ready multi-file version. Use this for actual deployment (upload the whole folder to your host). This version is easier to edit and maintain going forward.

Both versions have identical design and content — `index_standalone.html` is simply the multi-file version with everything inlined for portability.

## File Structure
```
a-major-insight/
├── index_standalone.html  (single-file preview version — open directly in browser)
├── index.html              (production HTML — links to styles.css/script.js/images)
├── styles.css               (design system + all styling)
├── script.js                 (nav, scroll reveals, contact form)
└── images/
    ├── hero.jpg              (hero background — Image 1, colorful blazer)
    ├── about.jpg             (About Ashley section — laptop photo)
    ├── speaking.jpg          (Speaking section — yellow garden, close crop)
    ├── reading.jpg           (Becoming HER Mastermind — full-body yellow garden photo)
    ├── casual.jpg            (Podcast section cover — car selfie)
    ├── book-paid.jpg          ("Get to Know Your Self in 30 Days, God's Way")
    ├── free1.jpg              (Navigating Life After Divorce & Separation)
    ├── free2.jpg              (Forgive to Flourish workbook)
    ├── free3.jpg              (Stormproof devotional)
    ├── free4.jpg              (The Path to Becoming scripture guide)
    ├── logo.png               (AMI logo, original — lavender/gold/black, for light backgrounds)
    ├── logo-light.png         (AMI logo, light-text variant used in nav + footer on dark plum)
    ├── favicon.ico / favicon.png  (site favicon, generated from logo)
```

All 4 of Ashley's personal photos are now used:
- Hero background (colorful blazer, full body)
- About Ashley section (green outfit with laptop/book)
- Becoming HER Mastermind (yellow outfit, full body, garden)
- Podcast cover (car selfie)

The AMI logo (`logo-light.png`) now appears in the navigation and footer.

## What's Built
- Full single-page site with smooth-scroll nav (desktop + mobile hamburger)
- Cinematic centered hero with dark plum overlay over Ashley's photo
- Credibility strip, "Right Place If" emotional section, "From Healing Into Becoming"
- "I RISE to Become" signature framework (6-step visual journey)
- Becoming HER Mastermind section incl. HER breakdown (Healed / Elevated / Reborn)
- About Ashley, "Where Faith Meets Transformation" pillars
- Free Resources grid (4 real covers from your assets)
- Paid Book feature section
- Podcast section with 3 placeholder episodes
- Speaking/topics section
- Testimonials (all 4 provided, staggered layout)
- Final CTA + Contact/Speaking inquiry form (front-end only, shows success message)
- Footer with nav, social, copyright

## Things to Replace Before Launch

1. **Amazon link** — `<a href="#" class="btn btn-primary">Buy on Amazon</a>` in the book section. Add the real Amazon URL.
2. **Free resource download links** — each "DOWNLOAD" button in the Free Resources section currently points to `#`. Replace with real download URLs (e.g. from Beacons).
3. **Podcast links** — "Listen to the Podcast" button and episode titles are placeholders. Replace with real episode titles/descriptions and a link to your podcast host (Spotify/Apple/etc).
4. **Social icons** — Instagram/Facebook/YouTube icons in the footer link to `#`. Add real profile URLs.
5. **Email address** — `hello@amajorinsight.com` in the Contact section is a placeholder; update if different.
6. **Contact form** — currently front-end only (shows a success message on submit, no backend). To make it functional, connect `#contact-form` in `script.js` to your form service of choice (e.g. Formspree, GoHighLevel, Mailchimp).
7. **Hero image swap** — to use a different photo of Ashley as the hero background, replace `images/hero.jpg` with a same-aspect-ratio image (portrait orientation works best with the centered overlay treatment).
8. **Editing after this point** — make changes to `index.html` / `styles.css` / `script.js` (the multi-file version). `index_standalone.html` is a separate generated snapshot for preview only and won't reflect future edits unless regenerated.

## Notes
- Favicon is generated from the AMI logo.
- All copy is final, premium copy (no lorem ipsum) — review for tone/accuracy before publishing.
- Fully responsive: desktop, tablet, and mobile (hamburger nav under ~1380px).
- The AMI logo and all 4 of Ashley's personal photos are used across the site (hero, About, Becoming HER, Podcast).

## Deploying the Site

I can't push this to a live server directly, but here are the fastest ways to get it online — all free or near-free:

**Easiest — Netlify Drop**
1. Go to https://app.netlify.com/drop
2. Drag the whole `a-major-insight` folder (the one containing `index.html`, `styles.css`, `script.js`, and `images/`) onto the page.
3. Netlify gives you a live URL instantly. You can rename the site and later connect a custom domain (e.g. amajorinsight.com) in Netlify's site settings.

**Also easy — Vercel**
1. Go to https://vercel.com/new and choose "Deploy without Git" / drag-and-drop the folder.
2. You'll get a live URL, with custom domain support in project settings.

**GitHub Pages (if you use GitHub)**
1. Create a new repo, upload the contents of this folder (not the folder itself — `index.html` should be at the repo root).
2. In repo Settings → Pages, set the source to the main branch root.
3. Your site will be live at `https://<username>.github.io/<repo-name>/`.

**Existing host (cPanel / FTP)**
Upload the contents of this folder to your site's `public_html` (or equivalent root) directory via FTP or your host's file manager — `index.html` should sit at the root so it loads at your domain automatically.

In all cases, upload the **multi-file version** (`index.html`, `styles.css`, `script.js`, `images/`), not `index_standalone.html` — the standalone file is just for quick local preview.
