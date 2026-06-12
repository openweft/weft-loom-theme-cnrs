# weft-loom-theme-cnrs

`cnrs` brand theme for weft-loom compile tooling.

**Signature** : CNRS — institutional blue #1D50A2 + cyan #00AFCA accent.

## Usage (Marp slides)

```yaml
---
marp: true
theme: cnrs
---

# Slide title
```

The theme is published as an OCI artifact at
`ghcr.io/openweft/weft-loom-theme-cnrs:<tag>` and consumed by
the tool images via a multi-stage `COPY --from=` :

```dockerfile
COPY --from=ghcr.io/openweft/weft-loom-theme-cnrsatest /marp/ /opt/marp/themes/
```

## Layout

| Path                  | Contents                                  |
| --------------------- | ----------------------------------------- |
| `marp/cnrs.css`   | Marp slide stylesheet                     |
| `pandoc/cnrs.tex` | pandoc XeLaTeX template (V0.2)            |
| `latex/cnrs.sty`  | raw LaTeX style package (V0.2)            |

## Brand integrity

The CSS commits to the institution's published visual identity
guide. Re-brand drift → open a PR with the citation. Logos +
wordmarks remain the property of their owners and are referenced
only by colour + typography, never bundled as image assets.

## License

BSD-3-Clause (openweft).
