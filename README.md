# AIA-Studio_BikeMapper

About the project:  <a href="https://www.iaacblog.com/programs/bikemapper/">BikeMapper Blog</a>  <br>
Website:            <a href="http://aia22.iaac.net:8080/g1">BikeMapper Website</a>  <br>
Deployment:         <a href="http://aia22.iaac.net:8080/g1/map">BikeMapper Map</a>  <br>

**All the required files are in the BikeMapper_MachineLearning folder** <br>

1. **Get data about lighting and road type conditions with OSMNX** <br>
Use compiling_02.ipynb <br>
Output: street characteristics including street lighting and road type <br>

2. **Get data about paving type** <br>
First downloaded images from mapillary (use ViennaMapillaryScraping.ipynb) <br>
Run images through semantic segmentation script (use RoadSurfaceSegmentation.ipynb) <br>
Correlate location of mapillary images to streets (coordstoEdges) <br>
Supplement semantic segmentation with data from osmnx (use compiling_02.ipynb) <br>

3. **Get data about veg type** <br>
First download images from mapillary (use ViennaMapillaryScraping.ipynb) <br>
Run images through semantic segmentation script (use RoadSurfaceSegmentation.ipynb) <br>
Correlate location of mapillary images to streets (coordstoEdges) <br>
Supplement semantic segmentation with data from osmnx (use compiling_02.ipynb) <br>

4. **Get data about wind speeds** <br>
Download roads and buildings in Vienna as geojson files 
(use <a href="https://drive.google.com/file/d/1-Lo4ighf97Rwxag09GhExjnTt18Xo5iD/view?usp=sharing">streets_proj.geojson</a> and <a href="https://drive.google.com/file/d/1-4Zu93BIYUDB79zqHrRRGqm9GutjH5Xd/view?usp=sharing">buildings_proj.geojson</a>) <br>
Geojson files can be read in grasshopper (use ViennaBuildingStreets.ipynb) <br>
Run infrared in grasshopper (use Infrared.gh) <br>

5. **Score streets by category** <br>
Use compiling_02.ipynb <br>
Data from step 1-5 gets combined together to develop into a single csv file called ‘finalScoredEdges.csv’ <br>

6. **Calculate routes** <br>
Inputs: ‘finalScoredEdges.csv’ + user preferences <br>
Output: geojson of route <br>
(See interactive_route folder) <br>



