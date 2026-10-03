# Holt Town Redevelopment

A 3D web map of a regeneration scheme for Holt Town in east Manchester, set in the city's real street network. Made for a University of Manchester planning studio (2025).

**Proposed / Today toggle:** *Proposed* shows the scheme's buildings by land use, the Medlock Green Way and the canal-side promenade. *Today* shows the buildings that stand on the site now, from OpenStreetMap.

## Data
- `data/buildings.geojson`: 336 proposed buildings with `use`, `base` and `height` in metres. They were converted from the 3D multipatch layer in the original ArcGIS Pro project (`Hilt Town.gdb`).
- `data/public_realm.geojson`: the Medlock Green Way, a riverside corridor about 30 m either side of the River Medlock, and the Ashton Canal promenade. Both were redrawn from OpenStreetMap river and canal lines because the original ArcGIS Online layers no longer exist.
- `data/water.geojson`: the River Medlock and Ashton Canal centrelines (OpenStreetMap, © OpenStreetMap contributors, ODbL).
- `data/site_boundary.geojson`: the study area boundary. `data/site_wall.geojson` is the same boundary as a 5 m-wide strip, drawn as a low wall so it reads above the street map.
- `data/buildings_gm.pmtiles`: about 167,000 existing buildings across central Greater Manchester (Eccles to Ashton-under-Lyne, Middleton to Burnage) from OpenStreetMap (Geofabrik extract, October 2026), packed as vector tiles so the browser only downloads the area on screen. Heights come from OSM `height` or `building:levels` tags where mapped, otherwise typical heights by building type. Buildings that touch the site boundary are flagged (`s = 1`) and hidden in the Proposed view.
- Basemap and street network: [OpenFreeMap](https://openfreemap.org) (OpenMapTiles schema, © OpenStreetMap contributors), loaded live.

## Hosting
Push this folder to a GitHub repository, then go to Settings → Pages → Deploy from branch → `main` / root.
