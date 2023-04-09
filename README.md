# Applications-of-Machine-Learning-in-Drought-Monitoring-and-Forecasting-using-SPI
Libraries-
rasterio
pyproj
matplotlib
gdal
osr
fiona
numpy
re
statistics
pandas
scipy.stats
tensorflow
sklearn
tqdm
Order of Files for Execution:-

1) Preprocessing and Normal Distribution Monitoring-
Input- 
Cell 2- CHIRPS monthly precipitation dataset
Cell 4- CHIRPS monthly precipitation dataset
Cell 5- Line 2- ROI shapefile
	Line 5- CHIRPS monthly precipitation dataset
	Line 6- CHIRPS monthly precipitation dataset
(After cell 5, please move clipped Karnataka Dataset to different folder)
Cell 6- Location of Karnataka dataset, change name after -nomd based on name chosen by user
Cell 7- Location of Karnataka dataset
Cell 9- Location of Any 1 Raster
Cell 27- classification_1- Line 4-  Change value based on drought category

Output- 
Average of every month(12 rasters)
Standard Deviation of every month(12 raster)
Anomaly of each month (480 rasters)
Standardized anomaly of each month(480 rasters)
Percentage deviation from mean for each month (480 rasters)
Frequency, Mean, Max and min duration, Mean and max intensity, onset and cessation mode(8 rasters)

— Compute SPI distributions(Code not with me)


2) Area Stats and Shapiro Test-
Input-
Cell 2- Location of SPI for which area stats need to be found
Cell 3- Location of SPI for which area stats need to be found, change name after -nomd based on name chosen by user
Cell 6- Location of Raster based on which mask and other rasters will be made
Cell 18- Location and name to save area  stats
Cell 21- Line 2- Change the starting value of for loop based on distribution

Output-
CSV file with area stats,
Raster with shapiro test p values



— Conduct PCA(Code not with me)


3) Drought Monitoring -Standard Precipitation Index
Input-
Cell 2- Location of SPI rasters
Cell 3- Location of SPI rasters, change name after -nomd based on name chosen by user
Cell 5- Location of Raster based on which mask and other rasters will be made
Cell 10- Line 4- change value based on drought severity
Cell 14- Line 2- Change the starting value of for loop based on distribution
Cell 32- Line 2- Change the starting value of for loop based on distribution

Output- 
Frequency, Mean duration, Max duration, Mean and max intensity, Mean Severity, onset and cessation mode(8 rasters)
Top 10 Frequency, Mean and Max duration, Mean and Max Intensity and Mean severity(5 rasters)


4)Value Extraction for each Pixel
Input-
Cell 2- Location of SPI rasters
Cell 3- Location of SPI rasters, change name after -nomd based on name chosen by user
Cell 5- Location of Raster based on which mask and other rasters will be made
Cell 8- Line 3- Change starting value of loop based on SPI
	Line 9- Change location to store wherever needed
Output- Multiple CSV with value for each pixel


5)Random Forest Forecasting
Input-
Cell 6- Location of Chosen Pixel

Output-
Graph and errors for forecasting(Not saved anywhere)


— Make datasets manually using excel for LSTM(teleconnections and lag correction)

6) LSTM Forecasting
Input- 
Cell 2- Location of Chosen Pixel 
Output- Graph and Errors (Not saved)

Things to Remember-
In all the code files, you need to modify the loading and saving file locations
Change mask based on default value outside boundary
For Monitoring codes, remember to change the starting of the MONITORING process based on which SPI timescale is being used.
In Forecasting, modify attributes according to need
