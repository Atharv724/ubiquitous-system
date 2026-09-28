# WORLD WEATHER

A Vite + React + TypeScript Earth intelligence foundation with a Cesium 3D globe, live Open-Meteo conditions, Nominatim search/reverse geocoding, Overpass nearby context, USGS seismic events, a simulation clock, and an immersive Earth Mode.

## Run locally

```bash
npm install
npm run dev
```

Build production assets with `npm run build`, then serve `dist/` from any static host. Copy `.env.example` to `.env.local` only to override optional API endpoints or product branding.

## Data sources and attribution

- **Open-Meteo** supplies forecast and current atmospheric observations.
- **OpenStreetMap / Nominatim** powers place search and reverse geocoding; requests are debounced and cached.
- **Overpass API** provides nearby OSM features and is cached per selected area.
- **USGS** provides the public all-day earthquake GeoJSON feed.
- **SpaceX** is isolated behind `spaceXService` for use in subsequent space panels.

Public adapters use request timeouts, one retry with backoff, and browser caching. Failed optional sources leave the rest of the experience available.
