# San Jose Redlining Map

Source for [sanjoseredlining.org](https://sanjoseredlining.org), an interactive map that
compares the 1930s HOLC redlining grades in San Jose with present-day data on transit,
broadband access, street trees, demographics, and air quality.

The HOLC boundaries are from the University of Richmond's
[Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) project. Other layers
come from the American Community Survey, City of San Jose open data, and OpenStreetMap,
plus 2025 seasonal averages of NO₂, ozone, and formaldehyde. Most of the analysis was
done in QGIS. The site is where the results are shared.

I worked on this independently from 2024 to 2025, with advice from a few professors
along the way.

## Running locally

The site is a single `index.html` using MapLibre GL JS. Vector layers are hosted on
MapTiler, and the GeoTIFF rasters are in this repo.

```
python3 -m http.server 8000
```

Then open http://localhost:8000. The MapTiler key is restricted to the live domain, so
some layers may not load locally.
