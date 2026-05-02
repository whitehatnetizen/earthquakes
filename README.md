# Earthquakes — interactive replay & heatmap

Live: https://whitehatnetizen.github.io/earthquakes/

Self-contained interactive visualisation of every M4.5+ earthquake recorded in the [USGS ANSS Comprehensive Catalog](https://earthquake.usgs.gov/fdsnws/event/1/) since 1960 — about 300,000 events.

## Modes

- **Replay** — time-scrubber animation; each quake fades in at its epicentre with size scaled by magnitude.
- **Heatmap** — kernel-density of seismic energy across the full catalog.
- **Live** — refreshes every 60 s with the USGS real-time M2.5+ feed for the past hour.

## Major historical events

Seventeen significant earthquakes are pinned to the timeline as clickable dots — Valdivia 1960, Alaska 1964, Tangshan 1976, Mexico City 1985, Kobe 1995, Sumatra 2004, Tōhoku 2011, Maule 2010, Kamchatka 2025, and others. Click any to:

- Pause the replay and jump to the exact event time
- Pan the map to the epicentre (current zoom preserved)
- Show a sidebar with date, magnitude, depth, location, and a curated note
- Link straight to the USGS event page

The ring stays put until another marker is clicked or the replay is resumed.

## Data sources

- Historical: USGS ANSS ComCat via FDSN
- Real-time: USGS earthquakes feed
- Basemap: [OpenFreeMap](https://openfreemap.org)

## Tech

deck.gl 9.x for rendering · MapLibre GL JS 4.x for the basemap · all libs inlined in `index.html`, no build needed at deploy time. The full source (Python build pipeline + raw parquet ingest) lives in a separate repo.
