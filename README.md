# Surfs_up

# Overview
In this analysis, I am creating a database that analyses the temperature in a given area. I will be using Oahu, Hawaii for this analysis. The purpose of this analysis is to see how the weather conditions vary between the summer months (June) and the winter months (December). Since Hawaii is known to rain, getting the weather results would be very useful in planning a trip / business venture in Oahu.

# Resources
- Software: Python3.8, Jupyter notebook 6.3.0
- Languages Used: Python.

# Results
From the query, the temperatures are relatively the same during the winter and summer months. June had an average temp of 74 degrees Farenheit while December had an average temperature. This is great considering that during the winter months, Oahu would have hot weather thats a good escape from the colder cities. This also helps businesses run all year round. Temperature alone, does not solve the problem though. Since Hawaii gets a lot of rain, its best to check the average precipitation for the same time period. 

If we were to run a query for the average precipitaion it would be as follows:

rain_dec = session.query(Measurement.date, Measurement.prcp).filter(extract('month',Measurement.date)==12).all()

In the end, getting the average precepitation would give us a better idea of the conditions in Oahu. From the analysis, I  was able to create a dataframe showing the average preciepitation for [June](https://github.com/somtoesomeju/Surfs_up/blob/main/june_rain.png) and [December](https://github.com/somtoesomeju/Surfs_up/blob/main/dec_rain.png). From the screenshots, June has a higher precipitation, indicating that it rains more during the summer months. December might be the best month overall in terms of temperature and precipitation.
