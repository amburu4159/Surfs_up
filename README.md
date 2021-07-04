# Surfs_Up Analysis

## Overview of the analysis
The purpose of this analysis is to review weateher patters in Hawaii for the months of June and December as we look into opening up an icream and surf shop. We need to 
to determine whether the weather conditions will be ideal for the shops to operate and be successful.

## Results: 
The following tables shows June's temperature over time.

![June Tobs](https://user-images.githubusercontent.com/83129180/124373117-4ac9c480-dc55-11eb-98c7-8185b8865efd.PNG)

The following tables shows December'stemperature over time.

![Dec Tobs](https://user-images.githubusercontent.com/83129180/124373112-41405c80-dc55-11eb-8d79-f379bdfbec3f.PNG)

o   Results of the analysis show that there 

1.The Average temperature between June and December is 75 and 71 degrees respectively. The temperatures are fairly steady with little fluctuation between the two periods on average.	

2.June temperatures range from 64 to 85 degrees. December temperatures range from 56 to 83 degrees.

3. Temperature in December are more spread out than in June since the standard deviation for December temperatures is higher.	

## Summary - Recommendations
The weather on average in December is slighltly lower than it is in June (75 vs 71 degrees). It is still suitable for an icecream and surf shop business.
 
### Additional queries to perform to gather more weather data for June and December

o   Get total precipitation levels for June and Dec

session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()

session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()

o Get the percipitation for the most active station for June and Dec

session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 6).all()

session.query(Measurement.prcp).filter(Measurement.station == 'USC00519281').filter(extract('month', Measurement.date) == 12).all()