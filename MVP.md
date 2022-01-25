
## MVP Overview

### Goal:
- To investigate patterns in passenger movement in severe weather events and advise the City on where to focus emergency services / infrastructure upgrade by looking for patterns in ridership due to heavy rainfall.

### Scope: 
- 2021 turnstile and precipitation data for all MTA stations

### Process:

- Merged hourly precipitation data to the hourly entries to each station by timestamp.
- Looked at 2 main questions:

    1. Investigated whether we can observe a relationship between precipitation and entries via a scatterplot. Then ran a more granular correlation calculation for each station.

    2. Do extreme storm days affect certain stations more? <br>Deep dive into 9/1/2021 when Hurricane Ida passed over NYC which had the highest daily precipitation (172.7mm). Looked to see whether certain stations displaying high increase or decrease in entries compared to the previous day with zero precipitation. Visualized using Matplotlib barcharts.

<br>

### Preliminary Results:


### 1. 

**Scatterplot**

<img src="/graphs/prcp_vs_entries_exits.png" width="500">


<br>

**Overall Correlation between total entries/exits & precipitation**

<img src="/graphs/correlation.png" width="250">


<br>

**Correlation between total entries/exits & precipitation by station**
| Top 10 negatively correlated stations| Top 10 positively correlated stations| 
| --------------- | --------------- | 
| <img src="/graphs/top_neg_corr.png" width= "200"> |<img src="/graphs/top_pos_corr.png" width= "200"> | 

<br>

### 2.   

**Deep dive into Storm day 10/26/2021**
#### Graph 1
<img src="/graphs/top_decreases.png" width="500">

#### Graph 2
<img src="/graphs/top_increases.png" width="500">


<br>

### Further development:
- Improve methodology for comparison to a "baseline" datestamp. Create an average over the same day of the week i.e. Hurricane Ida happened on a Wednesday, compare to mean & standard deviation of Wednesdays over the year. 
- Look at top 10 decreases and create time series graph of prcp and entries/exits over time to visualize the relationship.
- Map key stations of concern on a flood hazard map.