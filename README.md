# WaypointMaps

Offline data for **Waypoint**, a UK driving app. This repo holds no code, only downloadable files,
published as GitHub Releases. The app fetches them from here so drivers can use them without signal.

## What's here

| Release | Files | What it is |
|---|---|---|
| `maps` | Great Britain `.obf` region files + region catalogue (JSON) | Offline routing and speed limits for England, Scotland, Wales and Northern Ireland |
| `cctv` | `cctv.json` + `cctv-manifest.json` | Mapped surveillance cameras (CCTV) in the UK, refreshed weekly |

Download links follow this pattern:

https://github.com/johnanders271/WaypointMaps/releases/download/<release>/<file>

The app checks each manifest at most once a day and only downloads a file again when it has changed.

## Where the data comes from

All data here comes from **OpenStreetMap**.

- **Maps**: OpenStreetMap road data in OsmAnd's `.obf` format.
- **CCTV**: every OpenStreetMap node tagged `man_made=surveillance` in the UK, excluding speed,
  red-light and ANPR cameras (Waypoint handles those separately). Each camera keeps its position,
  whether it is public or private, what it watches, camera type, mounting and facing direction when
  mapped.

Camera positions are what volunteers have mapped. Many cameras aren't mapped, and some mapped ones may
have been removed. Treat it as a guide, not a complete list.

## Licence

Map data © OpenStreetMap contributors, available under the
[Open Database License (ODbL)](https://www.openstreetmap.org/copyright).
The files in this repo are derived from OpenStreetMap and are shared under the same licence.
If you use them, credit "© OpenStreetMap contributors".

To correct a camera or a road, edit it on [openstreetmap.org](https://www.openstreetmap.org). Fixes
reach these files on the next weekly update.
