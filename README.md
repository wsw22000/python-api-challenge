# Python API - What's the Weather Like?

![globe](output_data/Images/weather_satellite_image.png)

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. In this exercise, utilized what's been learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

While the answer seems fundamental - it gets hotter - this project utilized data to **prove** it?

![Equator](output_data/Images/city_lat_v_max_temp.png)

## WeatherPy

In this example, created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

Created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

![Temp](output_data/Images/city_lat_v_max_temp.png)
![Humidity](output_data/Images/city_lat_v_hum.png)
![Cloudiness](output_data/Images/city_lat_v_cloud.png)
![Wind Speed](output_data/Images/city_lat_v_wind.png)

Next ran linear regressions on each relationship, only this time separating them into Northern Hemisphere and Southern Hemisphere. Wrote a function that creates the linear regression plots listed below to optimize the code. Plots created were:

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

Below are a few examples of final linear regression plots.

![Temp Regression](output_data/Images/north_hem_city_lat_v_max_temp.png)
![Cloud Regression](output_data/Images/north_hem_city_lat_v_cloud.png)
![Humidity Regression](output_data/Images/north_hem_city_lat_v_hum.png)
![Wind Regression](output_data/Images/south_hem_city_lat_v_wind.png)

Final notebook:

* Randomly selects **more than** 500 unique (non-repeat) cities based on latitude and longitude.
* Performs a weather check on each of the cities using a series of successive API calls.
* Includes a print log of each city as it's being processed with the city number and city name.
* Saves a CSV of all retrieved data and a PNG image for each scatter plot.