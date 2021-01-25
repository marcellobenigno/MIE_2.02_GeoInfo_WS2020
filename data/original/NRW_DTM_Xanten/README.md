# Digital Terrain Model of the Municipality of Xanten

Because of the data size we decided not to distribute the DTM based on Airborne Laser Scanning (ALS) via Git. 

The ALS data is organized in tiles which are bundled in zip archives for each municipality (in our case "Xanten"). The original file format of each tile is a formatted text file with three columns for the x-y-z coordinates denoted as XYZ file format. Each row represents one grid point in space.

In fact all points of a single tile form a regular grid of 2000 x 2000 points with 1m distance between points in x- and y-direction leading to a text file with 4'000'000 rows!

**Download the DTM zip archive of the municipality of Xanten (approx. 500 MB packed and 4 GB unpacked):**
**https://www.opengeodata.nrw.de/produkte/geobasis/dgm/dgm1/dgm1_05170052_Xanten_EPSG4647_XYZ.zip**

Unzip the zip archive in the currect directory such that the subfolder `dgm1_05170052_Xanten_EPSG4647_XYZ` containing all xyz files is created.
 
