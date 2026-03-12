# BWM Homepage — Build Handoff

## Build: v4-full-build-2026-03-12

### Deployed
- **Production:** https://buildwisemedia.com (Cloudflare Pages)
- **Staging:** https://8c884471.buildwise-media.pages.dev
- **Repo:** https://github.com/buildwisemedia/bwm-homepage
- **Tag:** `v4-full-build-2026-03-12`

### What Was Built
Full rebuild from base spec + Patch v2 overrides. 3 pages:

| Page | File | URL |
|------|------|-----|
| Landing Page | `index.html` | `/` |
| Booking Page | `book.html` | `/book` |
| Confirmation | `booked.html` | `/booked` |

### Section Order (16 sections on landing page)
1. Hero (scroll notice, no geometric shapes)
2. Trust Bar (4 stats: $20M+ / 3-5× / 18+ / 90 Days)
3. Problem/Pain (The Poor Four)
4. Solution Bridge (Revenue Engine intro)
5. How It Works (3 steps)
6. What's Inside (Offer Stack, 10 items)
7. Comparison Table (9 rows)
8. Results/Proof (RutherfordMade + ROI math)
9. AI Acceleration Curve (NEW — SVG with stroke animation)
10. Compounding Slider (NEW — interactive, 4 metric cards)
11. Dot Grid / AI Future (NEW — 2,500 dots, wave animation)
12. Testimonials (carousel, 3 cards, auto-advance)
13. Why Buildwise
14. FAQ (10 questions, accordion)
15. Final CTA
16. Footer (no phone, 160px logo, Tucker GA)

### Design System
- **Palette:** v2 Production (Copper #BF9469, Ember #C75B2A)
- **Typography:** Playfair Display (display) + DM Sans (body)
- **Dark/Light:** prefers-color-scheme detection, cookie override, default dark
- **Texture:** Film grain overlay (dark mode), glass-effect cards, radial glow

### Tracking
- GA4: G-V5LSP69E41
- GTM: GTM-P5JSD86L
- Meta Pixel: 2728397250833051

### Locked Decisions Enforced
- No Robert on site
- No pricing visible (JSON-LD + llms.txt only)
- No revenue qualifiers
- No phone number anywhere
- CTA = "Book Your Strategy Call" everywhere
- No decorative geometric shapes

### QA Results
- 25 PASS / 2 FAIL (false positives) / 2 WARN
- False positive 1: `<title>` tag — present, grep -P fails on macOS
- False positive 2: book.buildwisemedia.com href — CTAs link to /book (architecture-correct)
- Warnings: no HSTS on staging (expected), no phone (locked decision)

### Known Items
- `og:image` meta tag points to `/og-image.png` — need to create and upload this asset
- Privacy Policy and Terms of Service pages not yet built (links go to `#`)
- Sitemap.xml not yet generated
- Microsoft Clarity project ID empty in config — add when ready
