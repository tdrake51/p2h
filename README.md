# P2H website

Static HTML site — no build step, no dependencies. Works on GitHub Pages as-is.

## Deploy

1. Copy everything in this folder to the root of the `tdrake51/p2h` repository (or push the folder and set Pages to serve from it).
2. Repo → Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Add a `CNAME` file containing your domain if you're using one.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | Home |
| `levels-of-care.html` | ASAM levels for P2H Recovery + P2H Wellness |
| `locations.html` | Easton, Baltimore, Pennsylvania + program status table |
| `resources.html` | Article index |
| `book.html` | Assessment request form |
| `css/modernist.css` | Design-system tokens and components — edit tokens here to reskin |
| `css/p2h.css` | Site layer (layout, placeholders, brand colors) |
| `.nojekyll` | Stops GitHub Pages running Jekyll |

## Before launch

- **Phone number** — every page uses (410) 555-0142 / `tel:14105550142`. Find-and-replace both.
- **Addresses** — Easton and Baltimore street addresses are marked "to add" in `locations.html`.
- **Photos** — each placeholder is a `<div class="grayscale ph">` with an HTML comment showing the `<img>` tag to drop in its place. Put files in `site/img/`.
- **Joint Commission Gold Seal** — footer placeholder; use the official file from your accreditation portal (usage is licensed, don't redraw it).
- **Form endpoint** — `book.html`'s `<form action="#">` needs a real handler (Formspree, Netlify Forms, or your intake CRM). Static hosting cannot accept posts. Given PHI, confirm the handler is HIPAA-capable with a BAA.
- **Legal pages** — Privacy, Notice of Privacy Practices, and Non-discrimination link to `#`.
- **Licensure claims** — copy currently says Easton is accredited, Baltimore cleared Part 1 of the two-part early survey, PA is in licensure. Update as each step clears.
