# climateScience
## Dataset Description:

URL: http://noaa-ghcn-pds.s3.amazonaws.com/  
Data Owner: NOAA (scientific agency that focuses on the weather conditions, atmosphere, oceans, etc). It collects real-time data from satellites, weather stations, etc.  
Format: .csv (one file per year, will need scraping)  
Data: Each row represents one station-day  
Time period: 175 years (~1763 - present)  
Interesting columns:   
PRCP = Precipitation (tenths of mm)  
SNOW = Snowfall (mm)
SNWD = Snow depth (mm)
TMAX = Maximum temperature (tenths of degrees C)
TMIN = Minimum temperature (tenths of degrees C)
TAVG = Average temperature (tenths of degrees C)
TSUN = Daily total sunshine (minutes)
AWND = Average daily wind speed (tenths of meters per second)
WT** = Weather Type
Any missing values: possible blanks
Location: Europe (determined through the least missing values : Austria, Spain, England)
Needs for data transformations: 
AWND = Average daily wind speed (tenths of meters per second)
Classify on the Beaufort scale (0-12)
TAVG = Average temperature (tenths of degrees C)
Calculate difference in average from previous year
(maybe also for other columns)
PRCP = Precipitation (tenths of mm)
Classify whether rain day or not (0, 1)
SNOW = Snowfall (mm)
Classify whether snow day or not (0, 1)
WT** = Weather Type 
Pick specific weather types to explore, transform those into columns (0, 1)
