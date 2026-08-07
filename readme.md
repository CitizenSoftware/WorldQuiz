# 🌍 Country Trainer – PWA

A Progressive Web App for learning countries using interactive SVG maps and ISO codes.

## Features

- **Quiz Mode**: Identify highlighted countries on the map.
- **Edit Mode**: Assign countries to custom regions.
- **Drag & Drop**: Load KML, GeoJSON, and SVG files.
- **Offline Support**: Works without an internet connection (once loaded).
- **Persistent Storage**: Countries and SVG data are saved in IndexedDB.

## Installation

1. **Download the ZIP** and extract it to a folder.
2. **Serve the app** using any static file server:
   - Use `npx serve` or `python -m http.server`
   - Or deploy to any web host (Netlify, Vercel, GitHub Pages)
3. **Open the app** in a browser. On first visit, the service worker will install and cache assets for offline use.

## Adding Icons

Replace the placeholder icons in the `/icons` folder with your own logo files. Use the included `generate-icons.js` script or an online generator to create the required sizes.

## Development

- The app is a single `index.html` file with embedded CSS and JavaScript.
- All data (countries, regions, assignments) is stored locally in IndexedDB and LocalStorage.
- Leaflet is used for map rendering (tiles loaded from OpenStreetMap).

## Offline Usage

The service worker caches all core assets and Leaflet libraries. Map tiles are fetched on‑demand and cached for offline use. Loaded country files are stored in IndexedDB and remain available offline.

## License

MIT