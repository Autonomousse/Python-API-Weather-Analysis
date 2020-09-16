# Python-API-Challenge - What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's utilize Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"
Now, we know what you may be thinking: "Duh. It gets hotter..."
But, if pressed, how would you **prove** it?

## Part I - WeatherPy

Create a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

Your first requirement is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude

	![Temperature](/WeatherPy/Images/Latitude-vs.-Max-Temperature.png)

* Humidity (%) vs. Latitude

	![Humidity](/WeatherPy/Images/Latitude-vs.-Humidity.png)

* Cloudiness (%) vs. Latitude

	![Cloudiness](/WeatherPy/Images/Latitude-vs.-Cloudiness.png)

* Wind Speed (mph) vs. Latitude

	![Wind_Speed](/WeatherPy/Images/Latitude-vs.-Wind-Speed.png)

After each plot add a sentence or too explaining what the code is analyzing.

Your second requirement is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude

	![North_Temperature](/WeatherPy/Images/Northern_Hemisphere_-_Max_Temperature_vs._Latitude.png)

* Southern Hemisphere - Temperature (F) vs. Latitude

	![South_Temperature](/WeatherPy/Images/Southern_Hemisphere_-_Max_Temperature_vs._Latitude.png)

* Northern Hemisphere - Humidity (%) vs. Latitude

	![North_Humidity](/WeatherPy/Images/Northern_Hemisphere_-_Humidity_vs._Latitude.png)

* Southern Hemisphere - Humidity (%) vs. Latitude

	![South_Humidity](/WeatherPy/Images/Southern_Hemisphere_-_Humidity_vs._Latitude.png)

* Northern Hemisphere - Cloudiness (%) vs. Latitude

	![North_Cloudiness](/WeatherPy/Images/Northern_Hemisphere_-_Cloudiness_vs._Latitude.png)

* Southern Hemisphere - Cloudiness (%) vs. Latitude

	![South_Cloudiness](/WeatherPy/Images/Southern_Hemisphere_-_Cloudiness_vs._Latitude.png)

* Northern Hemisphere - Wind Speed (mph) vs. Latitude

	![North_Wind_Speed](/WeatherPy/Images/Northern_Hemisphere_-_Wind_Speed_vs._Latitude.png)

* Southern Hemisphere - Wind Speed (mph) vs. Latitude

	![South_Wind_Speed](/WeatherPy/Images/Southern_Hemisphere_-_Wind_Speed_vs._Latitude.png)

Your final notebook must:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

## Part II - VacationPy


Now let's use your skills in working with weather data to plan future vacations. Use jupyter-gmaps and the Google Places API for this part.

* **Note**: if you having trouble displaying the maps try running `jupyter nbextension enable --py gmaps` in your environment and retry.
* Create a heat map that displays the humidity for every city from the part I.

![Humidty](/VacationPy/Images/humidty.png)

* Narrow down the DataFrame to find your ideal weather condition. For example:

    * A max temperature lower than 80 degrees but higher than 70.


    * Wind speed less than 10 mph.


    * Zero cloudiness.


    * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.


    * **Note**: Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

![Hotels](/VacationPy/Images/hotel.png)



