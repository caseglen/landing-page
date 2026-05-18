# Caseglen — Landing Page

Static HTML + CSS. No build step. Two pages:

- `index.html` — landing (hero, how it works, who it's for, CTAs to contact)
- `contact.html` — dedicated contact page (email mailto + LinkedIn link)
- `styles.css` — shared styles

Open `index.html` in a browser to preview.

## Preview locally

```bash
cd /Users/rajneesh/Desktop/Exp/landing
python3 -m http.server 8080
# then open http://localhost:8080
```

Or just double-click `index.html`.

## Things to do before sharing the URL

1. **Brand locked: Caseglen.** Domain `caseglen.com` verified available — buy it before doing outreach. Cheapest registrars: Cloudflare (~$10.44/yr), Porkbun (~$11/yr), Namecheap (~$13/yr).
2. **Check the meta description** in `<head>` — currently optimized for "tax resolution intake" search intent.

## Known temporary issue: LinkedIn URL slug

The LinkedIn company page displays the name "Caseglen" but the URL slug is currently `casebook-labs` (legacy page; LinkedIn locks slug changes for 30 days after a rename). The landing page contact-card shows clean text ("Caseglen on LinkedIn") so prospects don't see the mismatch unless they hover the link.

**Reminder for ~30 days from 2026-05-18 (i.e. ~2026-06-17):**
- Rename the LinkedIn company URL slug to `caseglen` in LinkedIn admin → Page info → Public URL
- Update the `href` in `landing/index.html` from `linkedin.com/company/casebook-labs` to `linkedin.com/company/caseglen`
- Add a 301 redirect from `caseglen.com/linkedin` to the LinkedIn page (cleaner link for outreach emails)

## Deploy options (pick one)

| Host | Cost | Setup |
|---|---|---|
| **Netlify Drop** | Free | Drag the `landing/` folder onto netlify.com/drop. Get a `*.netlify.app` URL in 30 seconds. |
| **Vercel** | Free | `npx vercel` in the `landing/` folder. |
| **GitHub Pages** | Free | Push to a public repo, enable Pages on the main branch. |
| **Cloudflare Pages** | Free | Connect a Git repo or upload the folder. |

For early outreach the auto-generated `*.netlify.app` subdomain is fine. Buy a real domain (e.g. `form433.ai`) only after 2-3 prospects ask "do you have a real URL?"

## What's intentionally NOT on the page

- ❌ **Pricing.** Don't anchor before discovery calls reveal what people will pay.
- ❌ **Demo video / product screenshots.** You don't have a product yet. Faking screenshots loses more trust than not having them.
- ❌ **Testimonials.** You have none. Don't fabricate.
- ❌ **Email capture form.** A `mailto:` is higher-friction but signals research mode, not lead-magnet mode. Switch to a form (Formspree / Tally) once you start running paid traffic.
- ❌ **Tracking / analytics.** Add later if needed. For 30 cold-emails worth of traffic, you'll learn more from replies than from analytics.

## Iteration plan

After the first 5-10 discovery calls, update the page with:
- 1-2 verbatim pain quotes from practitioners (with permission)
- Tighter headline based on what actually resonated on calls
- Real pricing once validated
- Email capture form once you're ready to handle inbound at scale
