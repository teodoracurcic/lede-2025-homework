# Homework 10: Mapping Power Plants with GeoPandas

This assignment was completed as part of homework for the [Lede Program at Columbia Journalism School](https://ledeprogram.com).  
The goal was to practice spatial analysis and cartographic design using GeoPandas in Python by recreating and expanding on this [Washington Post map of U.S. power plants](https://www.washingtonpost.com/graphics/national/power-plants/).

All work was done in Jupyter Notebook using open-source tools, with final maps can be exported as static images.



## Notebook

**File**: `geopandas homework.ipynb`  
This notebook includes the full workflow: data loading, filtering, CRS transformation, map design, spatial joins, and aggregation.


## Datasets Used

- `powerplants.csv` — Dataset with 8,600+ U.S. power plants including coordinates, energy type (`PrimSource`), and output (`Total_MW`)  
- `cb_2016_us_state_20m` — Shapefile of U.S. state boundaries (used for choropleths and spatial joins)


## Maps Produced

1. **Dot Map**  
   One dot per plant showing overall distribution.

2. **Bubble Map**  
   Bubble size reflects total megawatt output (`Total_MW`).

3. **Colored Dot Map**  
   Plants colored by primary energy source (`PrimSource`).

4. **Colored Bubble Map**  
   Combines bubble size and color to represent both output and source.

5. **Coal Only**  
   Shows only coal plants as bubbles, filtered by `PrimSource == 'coal'`.

6. **Solar Only (Dot Map)**  
   Shows only solar plants as equal-sized dots.

7. **Solar Choropleth**  
   Number of solar plants per state (using spatial join + groupby).

8. **Coal Choropleth**  
   Number of coal plants per state.

9. **Total Output Choropleth + Overlay**  
   Choropleth of total output (`Total_MW`) per state, with all plant locations overlaid as black dots.



## Tools & Techniques

- `GeoPandas` — spatial joins, projections (EPSG:5070), plotting
- `pandas` — data cleaning, filtering, grouping, merging
- `matplotlib` — map design
- Spatial operations: `.within()`, `.groupby()`, `gpd.sjoin()`
- Visual design: categorical and sequential color palettes, map layering, alpha transparency