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

## Editing measurements

All sizes are estimates from the photos. Coordinates are in metres, with the origin at ground level at the field-side
corner of the extension's back wall: **X** runs along the house toward the neighbour, **Z** runs from the house toward the
back fence. Update the `LAYOUT` block at the top of the script in `index.html` with tape-measured values.
