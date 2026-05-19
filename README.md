# Imperial Street Auto Repair — Website

Landing page for **Imperial Street Auto Repair**, a full-service auto shop at 5186 Imperial St, Burnaby, BC V5J 1E3. Phone: (604) 434-1120.

---

## Project overview

Single-page static website (`index.html`). No framework, no build step. All CSS is inline in a `<style>` block. All JS is inline before `</body>`. Deployed on Vercel via CLI.

**Live site:** deployed via `vercel --prod` from the main branch.

**GitHub repo:** `BuildOrbitGit/ImperialStreetAuto`

---

## Design system

### Colors (CSS custom properties)
```css
--copper:    #b76935   /* primary accent — buttons, borders, kickers, avatars */
--blue:      #0066cc   /* secondary links */
--navy:      #0a1929   /* dark section backgrounds */
--warm-grey: #f5f3f0   /* light section backgrounds */
--text:      #1a1a1a   /* body text */
--muted:     #666      /* secondary text */
```

### Typography
- **Headers:** Lora (Google Fonts, serif) — gives the shop a trustworthy, non-template feel
- **Body / UI:** Outfit (Google Fonts, sans-serif) — clean and modern
- Base size: 16px, line-height 1.6

### Visual motifs
- **Glassmorphism:** hero card uses `backdrop-filter: blur(18px)`, `rgba` backgrounds, `border: 1px solid rgba(255,255,255,.18)`
- **Copper accents:** copper left-border on nav brand, copper buttons, copper section kickers
- **Scroll reveals:** `.reveal` class + IntersectionObserver triggers fade-up on scroll

---

## Page sections (top to bottom)

| Section | ID | Notes |
|---|---|---|
| Nav | — | Brand name (Lora serif + copper border), phone CTA |
| Hours bar | `.hours-bar` | Live open/closed dot via JS, checks real shop hours |
| Hero | `#hero` | Glass card over shop background image |
| Cred strip | `.cred-bar` | Est. 1997 · 47+ Reviews · Same-day · Honest quotes |
| Quick cards | `.quick-cards` | 4 value props (no appointment, diagnostics, warranty, local) |
| Services sphere | `#services` | 3D rotating tag cloud, hover updates side panel with category info |
| Gallery | `#gallery` | 2-col × 2-row grid, hero image spans 2 rows |
| Why choose us | `#why` | Feature list cards |
| Reviews | `#reviews` | 3 Google review cards (all 5-star), "Trusted by our Burnaby community ★★★★★" |
| FAQ | `#faq` | 5 questions, JS accordion |
| Contact | `#contact` | Hours, address, Google Maps iframe |
| Footer | — | Copyright, address |

---

## What services are offered (and NOT offered)

**Offered:**
- Engine diagnostics, electrical, battery
- Brakes, tires, wheel alignment
- Oil changes, scheduled maintenance
- Transmission, exhaust, cooling
- Pre-purchase inspections, safety checks
- A/C, heating, climate control

**NOT offered (removed from all copy):**
- Auto detailing (no longer a service)
- Body work / paint

---

## Business details

- **Hours:** Mon–Fri 8am–6pm, Saturday walk-in welcome (not by appointment)
- **Location:** 5186 Imperial St, Burnaby BC V5J 1E3 (near Royal Oak SkyTrain)
- **Google rating:** 3.8 stars, 47+ reviews
- **Established:** 1997

---

## Deployment workflow

```bash
# Make changes to index.html (or other files)
git add index.html
git commit -m "Short description of change"
git push origin main
vercel --prod
```

Always work on `main` branch directly. No PR workflow needed for this project.

To roll back, use the Vercel dashboard → Deployments → promote a previous deployment to production.

---

## Improvement ideas & revamp notes

These are areas identified for future improvement:

### Design
- [ ] Add a real hero photo of the shop exterior (replace the current background image)
- [ ] Add more team/shop photos to the gallery — ideally 4–6 images showing the workspace and staff
- [ ] Consider a dark-mode variant using `prefers-color-scheme`
- [ ] Mobile nav: hamburger menu for smaller screens (currently just stacks)
- [ ] Typography scale could be tightened on mobile — some headings feel oversized at 320px

### Content
- [ ] Add real customer names/photos if any customers consent to a testimonial
- [ ] Embed actual Google Reviews widget if API key is obtained
- [ ] Add a "Brands we service" or "Makes we work on" section (Toyota, Honda, Ford, etc.)
- [ ] Consider adding a simple price list for common services (oil change, brake pad, etc.)

### Features
- [ ] Contact form (name, phone, describe problem) — currently only shows phone number
- [ ] Click-to-call tracking (Google Analytics event)
- [ ] Service booking link if shop adopts an online booking system
- [ ] Google Analytics / Plausible for traffic tracking

### Performance
- [ ] Compress and serve images as WebP (currently PNG/JPG)
- [ ] Lazy-load the Google Maps iframe (add `loading="lazy"` — done for img tags, confirm for iframe)
- [ ] Subset Google Fonts to only used character sets

### SEO
- [ ] Add Google Business Profile link in footer
- [ ] Add structured data for business hours (currently only has LocalBusiness schema)
- [ ] Expand meta description with more keywords

---

## File structure

```
/
├── index.html          # entire website — HTML, CSS, JS all inline
├── vercel.json         # cache headers config for Vercel
├── README.md           # this file
├── imperial-shop-clean.png   # shop exterior photo (hero background)
├── imperial-lift.png         # car on lift photo (gallery)
├── team-photo.jpg            # team photo (gallery)
└── .claude/
    └── launch.json     # preview server config (python3 -m http.server 3456)
```

---

## Local preview

```bash
cd /path/to/ImperialStreetAuto
python3 -m http.server 3456
# open http://localhost:3456
```
