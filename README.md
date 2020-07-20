## Citi Bike Tableau Analysis

*Analysis of Jersey City's December 2019 Citi Bike data to uncover two trends*


**Data Transformation:**

CSV data was pulled from https://s3.amazonaws.com/tripdata/index.html for the month of December 2019. Data transformed using Excel, Pandas Notebook, and Tableau itself. 

**Excel**
Distance from each start station and end station longitude and latitude point calculated with formula =ACOS(COS(RADIANS(90-Point 1 Latitude)) *COS(RADIANS(90- Point 2 Latitude)) +SIN(RADIANS(90-Point 1 Latitude)) *SIN(RADIANS(90-Point 2 Latitude) *COS(RADIANS(Point 1 Logitude-Point 2 Longitude))) *3959


