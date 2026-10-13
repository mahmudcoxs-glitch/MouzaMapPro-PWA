# MouzaMap Pro — iPhone Web App

This is a functional browser-based prototype for iPhone and desktop. It is not yet a native App Store app or a professional cadastral survey tool.

## Install on iPhone
1. Host the contents of this folder on an HTTPS web host (GitHub Pages, Netlify, or your own domain).
2. Open the HTTPS URL in Safari on your iPhone.
3. Tap Share → Add to Home Screen → Add.
4. Internet is needed for the Leaflet library and map tiles. Cached app shell can load offline, but offline base-map tiles are not included.

## Features
- Satellite imagery and street-map switch
- Current phone location and reported accuracy
- Point, line, polygon, circle, and pentagram drawing
- Length and area conversions with configurable decimal precision
- Import scanned map image and overlay it using supplied SW/NE GPS bounds
- Local project save/reload, GeoJSON/KML/CSV export, JSON backup/restore, print/PDF report
- Configurable katha/bigha conversions

## Important limitations
- The image overlay uses a rectangular geographic extent; it is not a full affine/rubber-sheet georeferencing engine.
- Phone GPS is not survey-grade. External RTK GNSS, correction service integration, coordinate-system transformations, and legally defensible survey workflows are not implemented.
- Map tile usage is subject to provider terms; attribution is displayed in the map controls.
- Katha/bigha conversions vary regionally; configure and verify before use.
- Local browser storage is not cloud backup. Export JSON backups.
