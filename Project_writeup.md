

## Passenger movement on severe storm days NYC 2021

### Abstract:
The goal of this project was to to investigate patterns in passenger movement in severe weather events and advise the City on where to focus emergency services / infrastructure upgrade by looking for patterns in ridership due to heavy rainfall.
Data used included MTA turnstile data, NOOA daily precipitation data and hourly precipitation data to investigate correlations between passenger movement and precipitation and overall passenger numbers at stations on a severe storm day. A list of subway stations of interest are provided where the City of New York could focus its resources for emergency services and infrastructure upgrade. These are overlayed on NYC extreme stormwater maps to show their location with respect to high flood risk areas.

### Design: 

The analysis was conducted in a two part phase.

<i> 1. Correlations </i>

Investigated whether we can observe a relationship between precipitation and entries via a correlation calculation for daily precipitation vs overall daily entries/exits for 2021. 


<i> 2. Interday Movement </i> 

A deep dive into two storm days was conducted: 9/1/2021 when Hurricane Ida passed over NYC which had the highest daily precipitation (172.7mm), and 10/26/2021 which had the second highest daily precipitation (63mm). 

Both storm days were preceded by a day with no precipitation so the no precipitation day was used as a baseline for comparison. `

### Data:
The dataset included 2021 MTA turnstile [data](http://web.mta.info/developers/turnstile.html ) which was supplemented by NOOA daily precipitation [data](https://www.ncdc.noaa.gov/cdo-web/datasets#LCD) and hourly precipitation [data](https://meteostat.net/en/station/72503 ). 

NYC Stormwater floodmap [shapefiles](https://catalog.data.gov/dataset/nyc-stormwater-flood-map-extreme-flood) were used as a basemap for plotting subway stations of interest to view flood risk. Latitude/longitudes were sourced from NY state [data](https://data.ny.gov/widgets/i9wp-a4ja). 

### Algorithms:

As per the two part phase described above.

<i> 1. Correlations</i>

- The total entries/exits were grouped and summed for each day and a correlation was run against daily precipitation.

- Correlations were also calculated on a more granular station level by grouping entries/exits by station and day and then running a correlation against daily precipitation. 

<br>

<i> 2. Interday Movement </i>

- Total daily entry/exits were calculated per station and then difference between total daily entry/exits from one day to the next was calculated for each station.  

- The top 10 stations which were most impacted by passenger movement from the previous day were found. These stations were analysed further on an hourly basis by looking at the movement between the same time stamp from the previous day. e.g. the difference between 8/31 8pm and 9/1 8pm was calculated. 

- These movements were graphed on top of precipitation using Matplotlib and Seaborn as a timeseries to visualise any pattern in movements. 



<br>


### Tools:
- SQL Alchemy and Pandas to import data
- Pandas and NumPy for data manipulation  
- Matplotlib and Seaborn for plotting
- Shapely, Contextily and GeoPandas for mapping