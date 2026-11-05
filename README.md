# Daniel Himmans — v10 publication preparation

This is a **modular static website** based on the approved v9 design and narrative engine. It is **not yet ready to publish** until the checklist below is completed.

## Preview

Run `python -m http.server 8000` from this directory and open `http://localhost:8000`. You can also open `index.html` directly in most browsers.

## Files and safe editing

- `index.html`: website sections and layout.
- `assets/styles.css`: visual styling.
- `assets/favicon.svg`: provisional monogram favicon.
- `content/library.js`: competency definitions, presets, narrative evidence scenes and scene order. **Most content updates happen here.**
- `engine/composer.js`: selection, narrative composition, deduplication, share links and print behaviour. Avoid editing this for routine copy changes.

### Add or improve a career story

1. Find the corresponding `scenes` entry in `content/library.js` and edit its `paras` text. Keep factual details verified.
2. To add a new distinct scene, give it a unique `id`, a `covers` array containing the appropriate competency IDs, a `heading`, a `paras` array, and `visual: null` (or a supported figure type). Add its ID to `sceneOrder`.
3. Check it appears only once for each relevant selection and that selected interests remain substantively covered.
4. To change a role preset, edit `presets`; use 1–4 valid competency IDs.
5. To add a fully curated role-specific narrative in future, introduce an explicit override map in the content layer and a small hook in the composer. **This override mechanism is planned, not yet implemented.**

## Contact and messaging privacy

The published contact section links to the supplied email and LinkedIn profile. Do not add personal WhatsApp numbers or private Messenger accounts to public HTML; hiding links visually does not protect the underlying details. If messaging is added later, use a dedicated professional number/account or a service with appropriate privacy controls.

## Before public launch

- Contact links have been added: dhimmans@gmail.com and the supplied LinkedIn profile. Confirm both work as intended before launch.
- Review and approve all public claims, especially revenue growth measurement and approximate metrics.
- Homepage intentionally uses a typographic executive presentation without a portrait.
- Test keyboard use, mobile/tablet layout, share URLs, and printing across browsers.
- Verify that generated views are readable and not repetitive across all presets and representative combinations.
- Decide domain and hosting, then add canonical URL, social preview image, robots/sitemap, and analytics only if appropriate.
- Review UK privacy/cookie requirements before enabling analytics or a contact form. Current site uses neither.

## Deployment

Upload the contents of this directory to a static host (e.g. Cloudflare Pages, Netlify or GitHub Pages). No server-side runtime is needed. Do not upload the standalone preview in place of this modular project if you want maintainable updates.
