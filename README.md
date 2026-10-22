# plan-my-trip stop snapshot

Public transport stops and the lines that call at them, for
[plan-my-trip](https://github.com/tigerasks/plan-my-trip). Built by that repository's
`tools/refresh-stops.py` from OpenStreetMap extracts.

- built: 2026-10-23
- regions: europe, asia, north-america, south-america, africa, australia-oceania, central-america
- stops: 4495039
- tiles: 8985, one per 1 degree of latitude and longitude

## Licence

This is a derived database of OpenStreetMap data.

© OpenStreetMap contributors, available under the
[Open Database Licence](https://opendatacommons.org/licenses/odbl/).

See https://www.openstreetmap.org/copyright.

## Layout

`manifest.json` lists the tiles that exist. Each `tiles/<lat>_<lng>.json` holds the stops
whose position floors to that whole degree, as columns: `o` the tile origin at 1e5 fixed
point, `y` and `x` delta-encoded positions from it, `n` the names newline-joined, `k` the
kind (0 bus, 1 rail, 2 tram, 3 other), `L` the line labels, and `l` each stop's labels as
indices into `L`.
