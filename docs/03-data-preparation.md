# Week 3 Data Preparation

## CRS

The analysis was reprojected to **EPSG:32737, WGS 84 / UTM zone 37S**, because the analysis involves distance and other spatial measurements that are more appropriate in a projected coordinate system using metres.

## Data Reprojected

The following datasets were reprojected to EPSG:32737:

* GRID3 settlement layer
* Nairobi County boundary
* OSM rivers
* OSM streams
* Nairobi DEM

## Data Clipped

The datasets were prepared for the **Nairobi County study area**.

The vector datasets processed for the study area were:

* GRID3 settlements
* OSM rivers
* OSM streams

The DEM was clipped to the Nairobi County study area for use in the elevation and low-lying area analysis.

## Quality Checks

### 1. CRS Check

All prepared datasets were checked and confirmed to use **EPSG:32737, WGS 84 / UTM zone 37S**.

### 2. Study Area Extent Check

The prepared datasets were checked against the Nairobi County study area. The settlement data and DEM were within the study area. Some river and stream features extended beyond the Nairobi County boundary because the processing retained features that intersected the study area rather than cutting the features exactly at the boundary.

### 3. Geometry Validity Check

The vector datasets were checked for geometry validity. All geometries were valid, and no geometry errors were found.

### 4. Attribute/Data Completeness Check

The datasets were checked for the required attributes and data completeness. The required data was present, with no significant missing or incomplete data identified.

### 5. Duplicate/Overlap Check

The prepared datasets were checked for duplicate features and unexpected overlaps. No significant duplicate features were identified.

## Problems Found

Some OSM river and stream features extended beyond the Nairobi County boundary after the spatial processing. This was identified as an extent/clipping issue rather than a geometry validity problem.

## Fixes / Flags

The issue was flagged for the next processing step. The river and stream layers can be clipped using the Nairobi County boundary so that only the portions falling within the study area are retained.

## Analysis-ready Data

The analysis-ready vector and raster data is stored in:

geodev-lab-project/`Datasets/processed/`
