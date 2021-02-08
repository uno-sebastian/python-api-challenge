# Sebastian's Python API Challenge - What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it?

![Equator](Images/equatorsign.png)

## Part I - WeatherPy

In this example, you'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

The first requirement is to create a series of scatter plots to showcase the following relationships:

#### Temperature (F) vs. Latitude
![Cities Temp vs Latitude](Images/Cities_TempVLat.png)

#### Humidity (%) vs. Latitude
![Cities Humidity vs Latitude](Images/Cities_HumidityVLat.png)

#### Cloudiness (%) vs. Latitude
![Cities Cloudiness vs Latitude](Images/Cities_CloudinessVLat.png)

#### Wind Speed (mph) vs. Latitude
![Cities Wind Speed vs Latitude](Images/Cities_WindSpeedVLat.png)

The second requirement is to run linear regression on each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

#### Northern Hemisphere - Temperature (F) vs. Latitude
![Northern Hemisphere Temp vs Latitude](Images/NorthHemiSphere_TempVLat.png)

#### Southern Hemisphere - Temperature (F) vs. Latitude
![Southern Hemisphere Temp vs Latitude](Images/SouthHemiSphere_TempVLat.png)

#### Northern Hemisphere - Humidity (%) vs. Latitude
![Northern Hemisphere Humidity vs Latitude](Images/NorthHemiSphere_HumidityVLat.png)

#### Southern Hemisphere - Humidity (%) vs. Latitude
![Southern Hemisphere Humidity vs Latitude](Images/SouthHemiSphere_HumidityVLat.png)

#### Northern Hemisphere - Cloudiness (%) vs. Latitude
![Northern Hemisphere Cloudiness vs Latitude](Images/NorthHemiSphere_CloudinessVLat.png)

#### Southern Hemisphere - Cloudiness (%) vs. Latitude
![Southern Hemisphere Cloudiness vs Latitude](Images/SouthHemiSphere_CloudinessVLat.png)

#### Northern Hemisphere - Wind Speed (mph) vs. Latitude
![Northern Hemisphere Wind Speed vs Latitude](Images/NorthHemiSphere_WindSpeedVLat.png)

#### Southern Hemisphere - Wind Speed (mph) vs. Latitude
![Southern Hemisphere Wind Speed vs Latitude](Images/SouthHemiSphere_WindSpeedVLat.png)

### Part II - VacationPy

Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part of the assignment.

* **Note:** Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure you can't be charged. Check out [Google Maps Platform Billing](https://developers.google.com/maps/billing/gmp-billing#monitor-and-restrict-consumption) and [Manage your cost of use](https://developers.google.com/maps/documentation/javascript/usage-and-billing#set-caps) for more information.

![heatmap](Images/heatmap.png)

Do the following:

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  * **Note:** Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

![hotel map](Images/hotel_map.png)
