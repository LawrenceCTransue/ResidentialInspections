# Residential Inspections Pro

Marketing website for **Residential Inspections Pro** — a residential home inspection company serving the Lehigh Valley, PA and western NJ (Warren & Hunterdon Counties).

Live site: [residentialinspections.pro](https://residentialinspections.pro)

## About this repo

This is a single static page (`index.html`) with no build step, no framework, and no dependencies beyond a Google Fonts link. It's hosted on **GitHub Pages** and served directly from this repository.

- `index.html` — the entire site (structure, styles, and content in one file)
- `CNAME` — tells GitHub Pages to serve the site at the custom domain `residentialinspections.pro`

## Hosting / Deployment

This repo is deployed via **GitHub Pages**:

1. Settings → Pages → Source is set to deploy from the `main` branch, root folder.
2. The custom domain is configured in Settings → Pages → Custom domain, which creates/updates the `CNAME` file in this repo.
3. Any push to `main` updates the live site — no build step required.

## Making updates

Since everything lives in one file, most edits are a direct find-and-replace in `index.html`:

| To change... | Look for... |
|---|---|
| Phone number | `6104170722` (tel links) and `(610) 417-0722` (display text) |
| Contact form fields | The `<form class="contact-form">` block near the bottom |
| Service area / towns list | The `#areas` section, and the `areaServed` list in the JSON-LD schema near the top of `<head>` |
| Photos | `<img src="...">` tags inside the "In the Field" gallery section — currently using free-license Unsplash placeholder images |
| Colors / theme | CSS custom properties at the top of the `<style>` block (`:root { --navy: ...; --amber: ...; }`) |

## Form submissions

The quote request form submits to [Formspree](https://formspree.io) (`https://formspree.io/f/xnpqnykr`). Submissions are emailed directly — no backend or database is involved. To change where submissions go, update the Formspree dashboard, not this repo.

## Analytics

Google Analytics (gtag.js) is wired up in `<head>` under measurement ID `G-389XHQNKD2`.

## License

See [LICENSE.md](./LICENSE.md). Site content and branding are proprietary to Residential Inspections Pro — this repo is public for hosting purposes only, not for reuse.
