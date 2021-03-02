# vector_tile_pbf_test
Attempting to work with tippecanoe vector tiles - data obtained via https://github.com/mapbox/tippecanoe#discontinuous-polygon-features-buildings-of-rhode-island-visible-at-all-zoom-levels


### Commands
In the `tippecanoe_testing/rhode_island` directory run

```
tippecanoe -zg -o RhodeIslandDC.mbtiles --drop-densest-as-needed --extend-zooms-if-still-dropping --no-tile-compression RhodeIsland.geojson
```

Then run 

```
mb-util RhodeIslandDC.mbtiles pbf_tiles/RhodesIslandDC --image_format=pbf
```

to generate static protobuf files that are decompressed (DC stands for decompressed).
