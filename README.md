# 仙女座星系 · Andromeda in Hubble's sharpest view

A narrated deep-zoom tour (in English) of the PHAT mosaic (ESA/Hubble heic1502a): one third of the Andromeda Galaxy, from the bulge across lanes of stars and dust to the outer disc, with the regions named, a light-year scale bar and a guided tour.

Live: https://youdata.github.io/andromeda/

Chinese version: https://youdata.github.io/andromeda-zh/ (it reads this site's tiles).

The image pyramid is a tile folder (`andromeda/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it. Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

Image: NASA, ESA, J. Dalcanton, B. F. Williams, L. C. Johnson (University of Washington), the PHAT team, and R. Gendler — CC BY 4.0.

## How it is made

From `infographic-examples/andromeda-hubble/build.mjs`, with rx (`~/rx-cli`):

```sh
rx export andromeda-hubble.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/andromeda --yes
```
