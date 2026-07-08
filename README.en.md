**English** · [Русский](README.md)

# Ría Olabeaga · Tides

A small PWA for viewing the water level and tides in the Ría de Olabeaga, Bilbao.

Open the app: https://aerotsunami.github.io/olabeaga_waves/

## What it shows

- the current water level in metres;
- the direction of the water: rising, falling, or turning;
- the rate of level change in centimetres per hour;
- dynamics over the last 1, 3 and 6 hours;
- a level chart for the coming days;
- the upcoming high and low tides.

## Language

The interface is available in Russian and English. Use the language button (EN / RU) in the top-right corner to switch; your choice is remembered.

## Data

The app uses the Open-Meteo Marine API and requests the `sea_level_height_msl` parameter for the Olabeaga coordinates.

Data is shown in Bilbao local time. It refreshes roughly every 30 minutes.

## How it works

This is a static site with no build step and no backend:

- `index.html` — the interface, chart and calculation logic;
- `manifest.json` — PWA settings;
- `sw.js` — the service worker for caching the app shell;
- `icon-*.png` — the app icons.

## Running locally

Just open `index.html` in a browser. To fully test the PWA and service worker, it's better to serve the folder as a local static server, for example:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.
