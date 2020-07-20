# Citi Bike Tableau Analysis

*Analysis of Jersey City's December 2019 Citi Bike data to uncover two trends*


## Data Transformation:

CSV data was pulled from https://s3.amazonaws.com/tripdata/index.html for the month of December 2019. Data transformed using Excel and Pandas Notebook. 

**Excel**  
Distance from each start station and end station longitude and latitude point calculated with formula =ACOS(COS(RADIANS(90-Point 1 Latitude)) *COS(RADIANS(90- Point 2 Latitude)) +SIN(RADIANS(90-Point 1 Latitude)) *SIN(RADIANS(90-Point 2 Latitude) *COS(RADIANS(Point 1 Logitude-Point 2 Longitude))) *3959

**Pandas Notebook**  
Works is done in count.ipynb file. Was unable to add trips taken from and to each station in Tableau, so value counts were done for each start station ID and end station ID. Two separate DataFrames were created and outer merged. Then values added together to create a series and then added to DataFrame and exported to totalstationcount.csv files


## Data Visualizations:  
The totalstationcount.csv and JC-201912-citibike-tripdata.xlsx were merged on the station ids in Tableau and a total of 8 visualizations were created for 2 stories.  

1st story discovered how more popular stations were located downtown and around more stations, compared to the ones on city edges which had less trips. Horizontal bar charts were created, counting number of trips by start station, by end station and then finally being added as a total count to determine their overall popularity. These were plotted on a map:

![Story 1](https://github.com/nabilq/CitibikeTableau/blob/master/Capture3.PNG)

2nd story created horizontal bar charts for trip duration and distance side-by-side and uncovered how longer trips were taken by stations further out from the core which also had less stations clustered. It was sorted using trip durations and trip durations plotted on map using longitude and latitude measures. Only the top 10 and bottom 10 in duration were shown and coloured appropriately. 

![Story 2](https://github.com/nabilq/CitibikeTableau/blob/master/Capture1.PNG)
![Story 2](https://github.com/nabilq/CitibikeTableau/blob/master/Capture2.PNG)

