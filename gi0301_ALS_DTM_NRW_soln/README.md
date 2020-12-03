# Digital Terrain Model

In this activity we cover the topic "Digital Terrain Models (DTM)" using the example of the official DTM provided by our federal state of Nordrhein-Westfalen (NRW). The DTM is derived from Airborne Laser Scanning.

Browse the data archive providing Airborne Laser Scan data of the Federal State of Nordrhein-Westfalen.

DO NOT DOWNLOAD THE DATA RANDOMLY DURING CLASS! IT IS TOO BIG!!! Just have a look!

Have a look at the SIZE of the following data sources, the description of which unfortunately being in German. It contains raw and processed data from aerial laser scanning (ALS).

Raw laser scanning data: https://www.opengeodata.nrw.de/produkte/geobasis/dgm/dgm1l/

Interpolated data on a regular 1m x 1m grid: https://www.opengeodata.nrw.de/produkte/geobasis/dgm/dgm1/

The ALS data is organized in tiles which are bundled in zip archives for each municipality (in our case "Xanten"). The original file format of each tile is a formatted text file with three columns for the x-y-z coordinates denoted as XYZ file format. Each row represents one grid point in space.

In fact all points of a single tile form a regular grid of 2000 x 2000 points with 1m distance between points in x- and y-direction leading to a text file with 4'000'000 rows!

Obviously the XYZ text files are not suitable for being processed in QGIS. Therefore we have to convert the XYZ format into a geoTiff format and use Python to perform the task.

Before we know which of the tiles have to be processed - i.e. are located in our region of interest (ROI) - we have to create a bounding box (georeferenced squared polygon) for all tiles (XYZ files) in the archive. These polygons are added to a shapefile which is used in QGIS later on to identify the interesting tiles in the ROI.

TO PREPARE FOR THIS ACTIVITY AT HOME PLEASE:

1) Set up a Python3 development environment. We recommend the Anaconda distribution from https://www.anaconda.com/distribution/

2) Install the Python package gdal, e.g. by calling "conda install gdal" 

3) Run Jupyter Notebook, create a new notebook and check, whether you can execute the following command: "from osgeo import osr, ogr, gdal"

4) Download the ALS DTM zip archive of the municipality of Xanten (approx. 500 MB packed and 4 GB unpacked): 
https://www.opengeodata.nrw.de/produkte/geobasis/dgm/dgm1/dgm1_05170052_Xanten_EPSG4647_XYZ.zip

ATTENTION! The Zip archive with Xanten ALS data is 517 MB large! Uncompressed the data needs approx. 4 GB!!!

LECTURE MATERIAL FOR LASER SCANNING
We are using a Powerpoint presentation by Petteri Packalén. It is available at slideplayer: https://slideplayer.com/slide/10386286/ 

The SPECTORS project partner Wageningen University and Research runs the Unmanned Aerial Remote Sensing Facility (UARSF). Among several very interesting instruments and flying platforms is the RICOPTER, an drone-borne laser scanner (LIDAR) by the company RIEGL.

Examples for ALS point clouds generated with the RICOPTER created by the WUR UARSF can be seen in a 3D online viewer:

Natural conservation area Dunea Wissel: http://common-test.services.geodesk.nl/storymaps/potree/dunea.html
Agricultural test site Hubselse Beek: http://common-test.services.geodesk.nl/storymaps/potree/hupsel.html