# What's the Weather Like?

## Background

"What's the weather like as we approach the equator?"

Now, I know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would we **prove** it?

![Equator](Images/equatorsign.png)

##  WeatherPy

In this section, we create a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, we utilize a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

I then create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


Afterwards, I run a linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude


### VacationPy

Here, I explore planning for future vacations using the Weather API using jupyter-gmaps and the Google Places API.

* I create a heat map that displays the humidity for every city from the WeatherPy script/output csv file.

  ![heatmap](Images/heatmap.png)

* I narrow down the DataFrame to find my ideal weather condition. For example:

  * A max temperature lower than 39 degrees but higher than 33 (Celcius).

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * I drop any rows that don't contain all three conditions.

* Using Google Places API, I find the first hotel for each city located within 5000 meters of my coordinates.

* I plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)



## Note

* The city data that is generated is based on random coordinates as well as different query times; as such, outputs of WeatherPy will not be the same each time the script is rerun, which also influences the input for the VacationPy script.