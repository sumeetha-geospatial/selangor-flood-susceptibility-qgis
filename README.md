# Flood Susceptibility Assessment in Selangor

## Project Overview

This project demonstrates a basic GIS flood susceptibility assessment workflow using DEM slope analysis and river proximity analysis in QGIS.

## Objectives

* Identify low-lying flood-prone zones
* Analyze proximity to waterways
* Produce flood susceptibility polygons and hotspot locations

## Data Sources

**USGS EarthExplorer** - SRTM DEM 30m
**OpenStreetMap via QuickOSM** - Waterways/river network
**GADM** - Administrative boundary of Selangor

## GIS Workflow

1. Downloaded and merged SRTM DEM tiles
2. Clipped DEM to Selangor boundary
3. Reprojected DEM to EPSG:32647
4. Generated slope raster
5. Extracted low slope areas (0–3°)
6. Created 500m river buffer
7. Rasterized river buffer
8. Performed raster overlay analysis
9. Converted raster to polygons
10. Generated centroids and coordinates
11. Joined flood polygons with river attributes

## Tools Used

* QGIS 3.40.6
* GDAL
* QuickOSM

## Key Outputs

* Flood susceptibility map
* Flood risk polygons
* River-linked hotspot identification
* Coordinate extraction

## Results

The analysis identified high flood susceptibility zones concentrated in the low-lying western part of Selangor, particularly areas within 500m of major waterways and near the coastline. The final map and outputs provide spatial location of potential flood hotspots for further validation and planning.

![Flood Susceptibility Map for Selangor](Selangor_Flood_Susceptibility_Map.PNG.png)
*Fig 1: Flood risk zones in western Selangor within 500m of waterways*

## Project Limitation

This is a simplified flood susceptibility assessment based primarily on slope and river proximity analysis. Additional variables such as rainfall, land use, and historical flood records were not incorporated due to data availability constraints.

**Future Improvement:**
The accuracy of this model would improve significantly by integrating historical flood hotspot data from NADMA or DID. Including rainfall intensity, land-use, and soil type would allow for a more robust hydrological risk assessment.
