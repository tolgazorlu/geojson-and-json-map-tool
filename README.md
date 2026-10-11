# GeoJSON and JSON Map Tool

A single-page browser tool that merges statistics data (e.g. TUIK/IBB style JSON) into a base GeoJSON file by a matching key, for use in map visualizations.

## About
Takes a base GeoJSON (feature geometries, e.g. Turkish province/district boundaries) and a separate JSON data file (an array of records under `veriler`), matches records to features by a configurable key (`duzeyKodu`), and produces a merged GeoJSON ready to paste into tools like Mapbox Datasets. Built 2025-11.

## Features
- Load a base `.geojson` file and a data `.json` file from the browser, no backend
- Case-insensitive key matching between the two files
- Appends yearly data columns (`data_<year>`) derived from the data file's `tarihler` array
- Preview merged output and download it as `.geojson`

## Tech stack
- Plain HTML/JavaScript, Tailwind CSS via CDN
- No build step, no dependencies

## Architecture
Single `index.html` file containing markup, styling and merge logic (`mergeDataIntoGeoJSON`).

## Getting started
Open `index.html` directly in a browser, or serve it statically:
```
python3 -m http.server
```

## Status
Learning/utility project, not actively maintained.
