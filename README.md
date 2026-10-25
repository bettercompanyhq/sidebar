# Sidebar — Homepage & Pre-order Page

Static site for Sidebar by Better Company HQ. Plain HTML, CSS and JavaScript — no build step, no dependencies.

## Files

```
index.html          Homepage (packages version)
preorder.html       Pre-order page (Team Kit / Deck Only)
assets/
  sidebar-logo.png  Logo (used as a mask so it can take any colour)
  andrea.jpg        Headshot
  melissa.jpg       Headshot
```

Fonts load from Google Fonts (Playfair Display, Poppins, Baloo 2).

## Run locally

Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

then visit http://localhost:8000.

## Publish with GitHub Pages

1. Create a repo and upload these files (keep the `assets` folder).
2. Repo **Settings → Pages → Deploy from a branch → main / (root)**.
3. Your site will be live at `https://<username>.github.io/<repo>/`.

The same folder also deploys as-is to Vercel, Netlify or Webflow (custom code).

## What works

- **Scenario card (homepage):** switch between Belonging, Judgment and Resilience, and flip to see approaches.
- **FAQ:** expand/collapse, no JavaScript needed.
- **Pre-order page:** choose a package, change quantity, live total in CAD.
  `preorder.html#deck` opens with Deck Only selected (used by the "Pre-order the deck" button).
- **Form validation:** name and a valid email are required.

## Before going live

1. **Connect the pre-order form.** Right now it shows the confirmation but doesn't send anything.
   In `preorder.html`, find `var FORM_ENDPOINT = '';` and paste a form endpoint, e.g. from
   [Formspree](https://formspree.io) (`https://formspree.io/f/xxxxxxx`).
   Submissions include: name, email, company, role, package, quantity, total_cad.
   If you'd rather take payment up front, replace the form with a Stripe Payment Link per package.
2. **Replace the placeholder** `[Payment, shipping and expected ship date details]` under the
   pre-order button.
3. **Update the year** in the footers if needed.
4. Optional: add an Open Graph image and Google Analytics tag in each page's `<head>`.

Questions: info@bettercompanyhq.com
