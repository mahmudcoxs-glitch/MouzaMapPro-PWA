# MouzaMap Pro — updated web/PWA prototype

This update is based on the supplied `MouzaMapPro-iPhone-WebApp` source archive. It preserves the existing lightweight Leaflet PWA structure and adds/removes features described below.

## Changes in this update
- Removed the Point and Pentagram drawing buttons/workflows.
- Renamed the line tool to **Ruler / Line**; it reports segment length and total length.
- Added an **Auto Polygon** action. It guides the user to trace the center of the visible plot boundary and creates a closed polygon when finished. It is a trace-assistance workflow, not computer-vision detection from an image.
- Added numerical image-overlay width/height controls in feet, inches, meters, centimeters, and millimeters, plus opacity, visual rotation, and a lock/unlock control.
- Project backup/save data now includes the imported image as a data URL when available, overlay bounds and overlay style settings, so an overlay can be restored with a project.
- Updated project schema and service-worker cache version.

## Run locally / host
1. Extract this folder.
2. Host it over HTTPS (for example GitHub Pages or another static host).
3. Open the HTTPS URL in Safari on iPhone and use Share → Add to Home Screen.
4. Internet access is needed for the map tiles and Leaflet library.

## Important limitations / not yet implemented
- **Google Maps is not yet the active basemap.** This project still uses Esri satellite imagery and OpenStreetMap street tiles through Leaflet. A proper Google Maps Platform integration requires an API key, billing/configuration, and a compatible map-layer implementation. It must not be emulated by scraping Google tile URLs.
- Auto Polygon currently means a guided manual trace; it does not automatically detect parcel edges from scanned imagery.
- Image width/height are interpreted as approximate ground dimensions around the overlay center. They are not the physical print dimensions of the scanned paper and do not independently georeference the image.
- The overlay still uses rectangular SW/NE geographic bounds. It is not a full draggable-corner, affine, or rubber-sheet georeferencing editor. Visual rotation can vary with map redraws.
- Undo/redo is not yet a complete history system for every edit. Geometry vertices are not yet draggable after finishing; delete and rename are available.
- Phone GPS is not survey-grade. RTK GNSS integration, coordinate-system transformations, control-point residual reports, and legally defensible cadastral survey workflows are not implemented.
- Local browser storage is not cloud backup. Export JSON backups regularly. Large embedded images can exceed browser local-storage quotas.
- Katha/bigha conversions vary regionally; configure and verify the correct local convention before use.

## Intended use
Planning and preliminary mapping only. For land demarcation, verify the Mouza map scale, projection, survey records, and control points with a qualified surveyor. This app does not certify cadastral boundaries.
