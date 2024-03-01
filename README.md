# Weather over the years

This repository contains a weather analysis, comparing European countries over the span of over 250 years, dating back as far as 1763.
The analysis can be found in the [Weather_Report.ipynb](https://github.com/LeliaE/climateScience/blob/main/Weather_Report.ipynb), including a thorough description of the steps taken in order to achieve the results.

## Collaborators

- [Lelia](https://github.com/LeliaE)
- [Andreea](https://github.com/andreeastroia)
- [Hritika](https://github.com/hritikakathuria136)
- [Amelie](https://github.com/amelie106)

## Instructions

You can view the notebook directly here on GitHub.
However, if you want to run and modify the notebook yourself, you will need to install Git on your computer. Refer to [this page](https://github.com/git-guides/install-git) for instructions.

Additionally, you will need Python (version 3.8 or higher) preinstalled. If you are using MacOS or Linux, this should already be the case. If you are on Windows, please refer to [this page](https://www.tomshardware.com/how-to/install-python-on-windows-10-and-11) for instructions.


### 0. Clone and enter repository
Open a terminal and run the following commands in order to clone the repository and enter its root directory:

```
git clone git@github.com:LeliaE/climateScience.git
cd climateScience
```


### 1. Create environment
Create an environment in the root directory like this:

```
python -m venv env
```


### 2. Activate environment
If you are using MacOS or Linux, run the following command to activate your environment:

```
source env/bin/activate
```

If you are using Windows, run this instead:

```
env\Scripts\activate
```


### 3. Install dependencies
Finally, install the requirements for this project by running the following command:

```
python -m pip install -r requirements.txt
```


## Running the notebook

In order to open the notebook, run the following command:

```
jupyter notebook Weather_Report.ipynb
```

## Data Ownership and Description:   
URL: http://noaa-ghcn-pds.s3.amazonaws.com/  
Data Owner: NOAA’s National Centers for Environmental Information (NCEI), a scientific agency that focuses on the weather conditions, atmosphere, oceans, and more. It collects real-time data from satellites, weather stations, etc.  
Format: .csv (one file per year and one file per station)    

## Information Contained:  
Data: Each row represents one station-day  
Time period: 260 years (~1763 - 2022)  


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

## License:  
See the [LICENSE](https://github.com/LeliaE/climateScience/blob/main/LICENSE.md) file for license rights and limitations (MIT).
