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

1. In **Settings → Secrets and variables → Actions**, add repository secrets
   `JWORLD_OPERATOR_NAME` and `JWORLD_BUSINESS_ADDRESS`. Enter the approved legal
   name and the approved address on separate lines in the address secret,
   without the country line. The build appends United Kingdom.
2. With release approval, set **Settings → Pages → Build and deployment →
   Source** to **GitHub Actions**. Retain the existing custom domain and HTTPS.
3. Merge the approved release to `main`, or run **Deploy JWorldCreations Pages**
   from `main` in **Actions** if already merged. The workflow sets
   `JWORLD_PUBLISH_DISCLOSURE=1` and fails before upload if details are missing.
4. Verify the published Business Information page and privacy policy. Keep
   the disclosure out of screenshots, logs and issue or pull request text.

## Notes

- This is intentionally framework-free (plain HTML/CSS/JS) for speed, simplicity, and GitHub Pages compatibility.
- The structure is easy to expand with future project pages and additional sections.

### Business disclosure release

The public source contains the Business Information page, a central footer link,
and the business contact email. Keep the approved personal details out of Git.
To stage a release artifact after the owner approves the disclosure, supply
`JWORLD_OPERATOR_NAME`, `JWORLD_BUSINESS_ADDRESS` (multiline, without the
country line) and `JWORLD_PUBLISH_DISCLOSURE=1` through private build settings.
Run `node tools/build-public.mjs <empty-output-directory-outside-the-repo>`.
Names and addresses are rendered only in `business-information.html`. Without
the flag the review artifact omits personal details. The page is accessible
without an account, and its noindex directive cannot guarantee privacy.

Branch-based deployment does not run this build. Keep transactional disclosures
and release configuration out of public source history.
