# GAINN website

Landing page for **GAINN — Graduate Advancement in Neuromodulation & Neurotech** (CRANIA NeuroModulation Institute, University of Toronto).

Single static page, no build step. `gainn-site/index.html` is the live site.

## Folder structure

```
gainn-site/
├── index.html                  ← the live site (all CSS + JS inline)
├── LICENSE
├── assets/
│   ├── fonts/                  ← D-DIN (self-hosted, used for all headings)
│   └── images/
│       ├── brand/              ← GAINN + U of T / CRANIA logos
│       ├── team/               ← Core team headshots
│       └── partners/           ← Partner logos shown in the footer
└── design-reference/           ← not part of the live site
    ├── concept.html            ← alternate design concept
    ├── mobile.html             ← early mobile comp
    └── tokens.css              ← colours / type / spacing as CSS variables
```

### Brand logos (`assets/images/brand/`)

| File | Where it's used |
|---|---|
| `gainn-logo-white-navy.png` | Hero section |
| `gainn-logo-all-white.png` | Footer (Connect row) |
| `uoft-crania-logo-white.png` | Hero section, next to the GAINN logo |
| `gainn-logo-black-navy.png` | Not used — version for light backgrounds |
| `gainn-logo-white-lightblue.png` | Not used — alternate dark version |
| `gainn-logo-white-lightblue-small.png` | Not used — small copy of the above |

## Adding content

### Add a team member
1. Crop the headshot to a **4:5 portrait** (e.g. 560 × 700), save as JPG.
2. Name it `firstname-lastname.jpg` and put it in `assets/images/team/`.
3. In `index.html`, find `const FAC = [` and add an entry:
   ```js
   {"n": "Full Name", "r": "Short role", "a": "Affiliation line",
    "img": "assets/images/team/firstname-lastname.jpg",
    "t": ["Tag 1", "Tag 2", "Tag 3"],
    "bio": ["Paragraph one.", "Paragraph two."]}
   ```
   The card and its bio pop-up are generated from this list — no HTML to copy.

### Add a partner
1. Save the logo as a transparent PNG, trimmed, ~160 px tall.
2. Name it after the organisation (e.g. `hospital-name.png`) and put it in `assets/images/partners/`.
3. In `index.html`, search for `class="pl"` in the footer and copy one of the `<a class="pl">` lines.
   Change the link, the `src`, the `alt`, and `--h` (the display height — tune it so the logo looks the same size as the others).

### Naming rules
- lowercase, words separated by hyphens, no spaces (`jose-zariffa.jpg`, not `Jose Z.jpg`)
- photos → `.jpg`, logos → `.png` with a transparent background

## Deploy
Cloudflare Pages — framework preset **None**, no build command, output directory **`gainn-site`** (or the repo root if `index.html` is moved there).

---

## Client notes (original)


So for the design that you give me the zip file , 

for the brain thing - either make it a brain - this fake ball looking brian is bad
also under program requirements - on the side there is this tihng that says list item ist item..

can you get rid of that - its making the thing look bad

and before he even tell us - increase the font size for the section headers to much larger- and use the UofT blue - that would look sexy ..
so your third color would be UofT
