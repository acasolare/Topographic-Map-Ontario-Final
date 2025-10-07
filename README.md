# Topographic-Map-Ontario-Final
Final topographic mapping project for MAP 671
# Topographic Map of Ontario (Final Project)

**Author:** Amanda Casolare  
**GitHub Username:** acasolare  
**Course:** MAP 671 — Introduction to GIS  
**Date:** October 6 2025  

## Project Overview
This project presents a topographic map of Ontario, focused on the Brockville region.  
The goal was to integrate elevation and hydrographic datasets to produce a clear, visually compelling map that highlights terrain and hydrology relationships.  
All data preparation, analysis, and design were completed in **QGIS 3.40.10 “Bratislava.”**

## Data Sources
- **Digital Elevation Model (DEM):** Copernicus GLO-30 (GeoTIFF format)  
  - [Copernicus DEM GLO-30 Download Portal](https://spacedata.copernicus.eu/collections/copernicus-digital-elevation-model)
- **Hydrography (Rivers and Lakes):** [Natural Earth Dataset (10m scale)](https://www.naturalearthdata.com/)
- **Populated Places and Boundaries:** [Natural Earth Dataset (10m scale)](https://www.naturalearthdata.com/)

## Methods
1. Imported DEM and Natural Earth vector data into QGIS.  
2. Reprojected all vector layers from **EPSG:4326 (WGS 84)** to **EPSG:3857 (WGS 84 / Pseudo-Mercator)** to match the DEM.  
3. Used *Extract Layer Extent* to create a bounding polygon for the DEM.  
4. Clipped all vector layers (rivers, lakes, populated places, and country boundaries) to the DEM extent using the **Clip** tool.  
5. Styled the DEM using a terrain color ramp for elevation, with blue symbology for rivers and lakes.  
6. Added populated place labels and a subtle gray country boundary.  
7. Inserted a legend, scale bar, north arrow, and map title in QGIS Print Layout.  
8. Exported the final map at two resolutions:  
   - **Web version:** 1200 px width  
   - **High-resolution:** 8000 px width  

## Projection Information
- **Original Data CRS:** EPSG:4326 (WGS 84)  
- **Final Map CRS:** EPSG:3857 (WGS 84 / Pseudo-Mercator)  

## View the Map
- [View Web Map on GitHub Pages](https://acasolare.github.io/Topographic-Map-Ontario-Final/)  
- [Download High-Resolution Map (8000 px PNG)](Topographic_map_final_highres.png)

## Software
- QGIS 3.40.10 “Bratislava”  
- GDAL 3.11.3  
- PROJ 9.6.2  

## Reflection
This project strengthened my understanding of coordinate systems, raster and vector integration, and effective map composition in QGIS.  
If I created a future version, I would explore symbolizing population density or land cover to add further context to the terrain visualization.
