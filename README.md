# J World Creations Website

A lightweight, multi-page static website for **jworldcreations.com**.

This site acts as the umbrella landing page for independent projects by J World Creations, including:
- EV Revival
- Darts Master
- Overrun

## Site structure

- `index.html` — main landing page with hero, featured projects, about summary, and CTA.
- `projects.html` — expanded list of all current projects.
- `about.html` — background and purpose of J World Creations.
- `contact.html` — simple contact page and support expectations note.
- `privacy.html` — umbrella privacy information for the website itself.
- `terms.html` — umbrella terms for website use.
- `style.css` — shared styles for all pages.
- `script.js` — lightweight JavaScript for mobile navigation, year in footer, and back-to-top button.
- `assets/favicon.svg` — placeholder favicon/logo.

## Deploying to GitHub Pages

1. Push this repository to GitHub.
2. In GitHub, open **Settings → Pages**.
3. Under **Build and deployment**, set:
   - **Source**: Deploy from a branch
   - **Branch**: `main` (or your default branch), folder `/ (root)`
4. Save and wait for GitHub Pages to publish.
5. Confirm the published URL loads correctly.

## Custom domain (GoDaddy later)

When ready to point your domain from GoDaddy:

1. In GitHub Pages settings, add a custom domain:
   - Suggested primary host: `www.jworldcreations.com`
2. In GoDaddy DNS:
   - Add/confirm a `CNAME` record for `www` pointing to `<your-github-username>.github.io`.
   - For root (`jworldcreations.com`), use a redirect/forwarding approach to `https://www.jworldcreations.com` (or use A/ALIAS setup if preferred).
3. Enable HTTPS in GitHub Pages once DNS has propagated.

## Notes

- This is intentionally framework-free (plain HTML/CSS/JS) for speed, simplicity, and GitHub Pages compatibility.
- The structure is easy to expand with future project pages and additional sections.
