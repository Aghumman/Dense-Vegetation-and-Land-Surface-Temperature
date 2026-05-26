## Research Question: 
Does the area near to dense vegetation have lower land surface temperature?

## Methodology:
1) Download the red and nir bands from Sentinel-2 to calculate NDVI.
2) Download the Landsat thermal data to calculate the land surface temperature.
3) reproject_ndvi_to_temp function matches the crs, shape, and pixel size of NDVI to Landsat.
4) ndvi_map function crops the red and nir bands to a specific borough, calculates and creates the NDVI map.
5) temp function crops the thermal data to a specific borough and converts the raw data to degree celsius.
6) temp_distance_ndvi function calculates the average land surface temperature at different distances from dense vegetation.
7) vegetation_map function creates a visual overlay of dense vegetation and land surface temperature.
   
## Datasets:
1) Sentinel-2C L2A — S2C_MSIL2A_20250812T154951 — Aug 12, 2025 — B04 (Red) and B08 (NIR) at 10m — used for NDVI
2) Landsat 9 L2SP — LC09_L2SP_013032_20250822 — Aug 22, 2025 — B10 (Thermal) at 30m — used for LST
3) Landsat 9 L2SP — LC09_L2SP_013032_20250822 — Aug 22, 2025 — B4 (Red) and B5 (NIR) at 30m — used for Landsat NDVI comparison
4) NYC Borough Boundaries shapefile — geo_export_4028990d-538c-4c7b-8a10-4c82a933d409.shp
