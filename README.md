# Garden 33 – 3D garden model

A three.js model of the back garden, built from photos, for planning changes (first up: a pergola over the terrace).

- `index.html` is the whole app: open it through any static server, e.g. `python3 -m http.server`, then go to http://localhost:8000.
- `garden.glb` is the same model exported for Blender (File → Import → glTF 2.0).
  To re-export after editing, open the page locally and click **Download .glb for Blender**.

## What's modelled

House with rear extension, tiled terrace (60 × 60 cm), clinker path to the back gate, lawn, planting bed with the
hedge on the mesh fence, wooden fences, spots where containers stand today, covered furniture, and the surroundings
(neighbours, sheds behind, field trees) for realistic shadows.

## Sun & shade

The sun is computed for the central Netherlands (52.1° N) on the chosen date and Dutch clock time.
The garden's orientation ("Back fence faces") defaults to **south**, based on the shadows in the photos; change it if that's wrong.

## Measurements

Coordinates are in metres, with the origin at ground level at the field-side corner of the extension's back wall:
**X** runs along the house toward the neighbour, **Z** runs from the house toward the back fence.

Measured with a tape (in the `LAYOUT` block at the top of the script in `index.html`):

| Extension back wall, left → right | cm |
|---|---|
| Corner → grey door | 216 |
| Grey door (incl. frame) | 104 |
| Door → glass doors (39 wall + 8 downpipe + 114 wall) | 161 |
| Glass doors (181.5 fixed + 94.5 + 94.5) | 370 |
| Glass doors → corner at neighbour fence | 97 |

- Terrace: 12 × 5 tiles of 60 × 60 cm = 720 × 300 cm, laid one tile to the right of the glass doors and eleven to the left.
- Pebble strip between the wall/doors and the tiles: 8 cm.
- Planting border between the terrace and the neighbour fence: 40 cm.
- Path: starts 22 cm in from the terrace's field-side corner and runs straight to the gate.
- Mesh fence + hedge on the field side: 23 cm outside the house corner.

Still estimated from photos (shown with ≈ in the model): garden depth, lawn, path width (≈1.10 m), the extension height,
the house volume, and where furniture and pots stand. Positions that follow from the wall (terrace, path, container
spots, herb planter) are computed from the measured values, so correcting a number there moves them along.
