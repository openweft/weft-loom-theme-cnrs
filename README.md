<p align="center"><img src="https://raw.githubusercontent.com/openweft/brand/main/social/weft-loom-theme-cnrs.png" alt="weft-loom-theme-cnrs" width="720"></p>

# weft-loom-theme-cnrs

`cnrs` brand theme for weft-loom compile tooling.

**Signature** : `#0660FF` — the electric Marianne-leaning blue used
across the current CNRS web identity. The earlier draft used a
muted `#1D50A2` which doesn't match the institution's actual brand
saturation.

## Source

Colour frequency-counted across the CNRS theme stylesheet
(`www.cnrs.fr/sites/default/files/css/css_V-i0aKYHu__c4i3nBxPe3-VsyQv_IPSIoWkCY6Q4KL0.css`,
2026-06 audit) :

| Token              | Hex       | Occurrences in CSS |
| ------------------ | --------- | ------------------ |
| Primary blue       | `#0660FF` | 196                |
| Body text          | `#151723` | 78                 |
| Muted text         | `#535460` | 73                 |
| Soft paper surface | `#F1F2FA` | 32                 |
| Secondary blue     | `#0094F0` | 10                 |

## Typography

Brand-prescribed Google Fonts found in the site stylesheet :

- **Chivo** — headlines + emphasis (the dominant brand display
  face).
- **Libre Franklin** — body.
- **Rubik** — UI / labels.

All three are free on Google Fonts and embedded by the slide
renderer automatically.

## Wordmark

The institution wording is "Centre national de la recherche
scientifique (CNRS)" in long form ; CNRS in short form. The CSS
prints the short form in the upper-right of every slide.

## Usage (Marp slides)

```yaml
---
marp: true
theme: cnrs
---

# Slide title
```

## Distribution

Published as an OCI artifact at
`ghcr.io/openweft/weft-loom-theme-cnrs:<tag>`. Tool images consume
it via multi-stage `COPY --from=` :

```dockerfile
COPY --from=ghcr.io/openweft/weft-loom-theme-cnrs:latest /marp/cnrs.css /opt/marp/themes/cnrs.css
```

## License

BSD-3-Clause (openweft). The CNRS name, logo, and trademark remain
the property of the CNRS ; this repo references the institution
only by colour and typography, never bundled as image assets.

## Cover slide / logo

The theme renders a brand-typography wordmark on `section.lead`
slides ; no institutional logo file is bundled (trademarks remain
the institution's property and aren't redistributable under
BSD-3-Clause).

If you have the right to use the official logotype in your deck,
supply your own image via the `--cnrs-logo` CSS variable :

```markdown
<!-- _class: lead -->
<!-- _style: "--cnrs-logo: url(/path/to/your/logo.svg)" -->

# Title here
## Subtitle here
```

Official logo source : https://www.cnrs.fr — Presse / CNRS Images.
