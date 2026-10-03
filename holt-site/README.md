# Holt Town Redevelopment

A 3D web map of a regeneration scheme for Holt Town in east Manchester, set in the city's real street network. Made for a University of Manchester planning studio (2025).

**Proposed / Today toggle:** *Proposed* shows the scheme's buildings by land use, the Medlock Green Way and the canal-side promenade. *Today* shows the buildings that stand on the site now, from OpenStreetMap.

## Data
- `data/buildings.geojson`: 336 proposed buildings with `use`, `base` and `height` in metres. They were converted from the 3D multipatch layer in the original ArcGIS Pro project (`Hilt Town.gdb`).
- `data/public_realm.geojson`: the Medlock Green Way, a riverside corridor about 30 m either side of the River Medlock, and the Ashton Canal promenade. Both were redrawn from OpenStreetMap river and canal lines because the original ArcGIS Online layers no longer exist.
- `data/water.geojson`: the River Medlock and Ashton Canal centrelines (OpenStreetMap, © OpenStreetMap contributors, ODbL).
- `data/site_boundary.geojson`: the study area boundary.
- Basemap, street network and existing buildings: [OpenFreeMap](https://openfreemap.org) (OpenMapTiles schema, © OpenStreetMap contributors), loaded live.

## Hosting
Push this folder to a GitHub repository, then go to Settings → Pages → Deploy from branch → `main` / root.
