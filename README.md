# Surf's Up Analysis
Challenge 9 for Butler Data Science

## 1. Overview of Surf's Up Analysis
### 
* The goal of this module is to determine if it is viable to open a surf shop. Our partner in this endeavor wants to to be sure the weather will be ideal for surfing year round. To determine this we took weather data from stations in Hawaii and analyzed the temperatures.

## 2. Results
### 
* June Vs. December
	- To analyze weather differences we took the high point of the summer and compared it to the low point of the winter. We had to ensure the summer data was warm enough to sustain surfing and that the winter months would not force our business to close. For this analysis we will be comparing the summary statistics table below for temperatures in both months.

	  - Summary Statistics

![Summary Statistics](https://github.com/coxjack/AdvDataStorageChallenge9/blob/main/Additional%20Supporting%20Images/Temps%20Compare.png)

	- Mean Temps
	  - Comparing the data we can see that there is an average temperature of 74.9 degrees in June and an average temperature of 71 degrees in December. This tells us that on average in either month we would have no issue attracting surfers because it is warm enough to surf.

	- Min Temps
	  - Comparing the data we can see that there is a minimum temperature of 64 degrees in June and a minimum temperature of 56 degrees in December. This tells us that yes in either month there would be days where it would be cold to surf but not impossible to do so.

	- Max Temps
	  - Comparing the data we can see that there is a maximum temperature of 85 degrees in June and a maximum temperature of 83 degrees in December. This tells us that it can be almost in warm in December on any given day as it is in June. Combined with the average temperature calculation this is promising weather for December.


	
## 3. Summary
### 
* Overall, there are key differences between summer and winter in our dataset but not large enough of a difference to detract surfers from visiting our shop year round. To show this there are additional queries comparing the data per station for June & December.

	- June Station Temps
	  - june_station = session.query(Measurement.tobs, Measurement.station).\
                filter(extract('month',Measurement.date)== 6).all()

	- December Station Temps
	  - dec_station = session.query(Measurement.tobs, Measurement.station).\
            filter(extract('month',Measurement.date)== 12).all()

	  - Combined Station Temps

![Combined Station Temps](https://github.com/coxjack/AdvDataStorageChallenge9/blob/main/Additional%20Supporting%20Images/Summary%20Stations.png)



