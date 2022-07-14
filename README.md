# AIA-Studio_BikeMapper
1. **Get data about lighting and road type conditions with OSMNX** <br>
Use compiling_02.ipynb
Output: street characteristics including street lighting and road type

2. **Get data about paving type**
First downloaded images from mapillary (use ViennaMapillaryScraping.ipynb)
Run images through semantic segmentation script (use RoadSurfaceSegmentation.ipynb)
Correlate location of mapillary images to streets (coordstoEdges)
Supplement semantic segmentation with data from osmnx (use compiling_02.ipynb)

3. **Get data about veg type**
First download images from mapillary (use ViennaMapillaryScraping.ipynb)
Run images through semantic segmentation script (use RoadSurfaceSegmentation.ipynb)
Correlate location of mapillary images to streets (coordstoEdges)
Supplement semantic segmentation with data from osmnx (use compiling_02.ipynb)

4. **Get data about wind speeds**
Download roads and buildings in Vienna as geojson files (use streets_proj.geojson and buildings_proj.geojson)
Geojson files can be read in grasshopper (use ViennaBuildingStreets.ipynb)
Run infrared in grasshopper (use Infrared.gh)

5. **Score streets by category**
Use compiling_02.ipynb
Data from step 1-5 gets combined together to develop into a single csv file called ‘finalScoredEdges.csv’

6. **Calculate routes**
Inputs: ‘finalScoredEdges.csv’ + user preferences
Output: geojson of route
(See interactive_route folder)



