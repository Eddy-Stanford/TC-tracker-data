# TC-tracker-data
This directory contains files describing the tropical cyclones that occurred in each of the model simuations. The files were generated with the GFDL TSTORMS tropical cyclone tracker, publicly available here: https://www.gfdl.noaa.gov/tstorms/. Each subdirectory is named according to the corresponding simulation. For example, the directory "aqua_c192L33_45N" contains results from the simulation with SST maximum at 45 degrees north. Each of these directories contains five files: "trav_1979", "trav_1980", "trav_1981", "trav_1982", and "trav_1983", each containing results from the corresponding year of the five-year simulation. The exception is the simulation with SST maximum at 0 degrees north (the equator), which yielded so few tropical cyclones that the results from all five years were combined into the single file "trav_1979-1983".

Each file has a "start" line to indicate the start of a new tropical cyclone, followed by several rows of data describing that tropical cyclone at 6-hour time intervals, followed by another "start" line and block of data for another tropical cyclone, and so on. An example of a "start" line is as follows:

start    34  1979     1     5     6

The numbers after the word "start" are the number of lines of data (34) until the next start line (in other words, the duration of the tropical cyclone in 6-hour units), and the year (1979), month (1), day (5), and hour (6) of the start of the tropical cyclone. An example of a non-"start" line is as follows:

319.69   35.75   15.26  981.51   0.00030426  1979     1     5     6

The numbers in this line are the longitude (319.69) and latitude (35.75) of the tropical cyclone in degrees, the maximum 10-meter wind speed in meters per second (15.26), the minimum sea-level pressure in hectopascals (981.51), the maximum relative vorticity in s^{-1} (0.00030426), and the year (1979), month (1), day (5), and hour (6) at which this information is recorded. These two example lines are the first two lines of the file "aqua_c192L33_45N/trav_1979".
