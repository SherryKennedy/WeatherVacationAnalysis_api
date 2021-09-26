# WeatherVacationAnalysis_api
Coding Python in Jupyter Notebooks, utilizes the OpenWeatherMap API and the citipy library. Analyze weather relationship. Use jupyter-gmaps and the Google Places API for weather based vacation references.

## Setup
Created a github repository
Created a FOLDER 'starter_code' which has ***WeatherPy.ipynb*** and ***VacationPy.ipynb*** execution files.
Created a file  which has the configuration for the api keys used. This file has not been pushed to github.
Created a FOLDER 'output_data_files' which has the output files and images from WeatherPy and two additional snapshots from VacationPy
Two csv files were output, one cities.csv, the collection of cities from the cityPy module that was used, and CityWeatherData.csv which has all of the City and weather data together.

* Included a written description of observable trends based on the data.
* included a screenshot of the heatmap you create and include it in your submission.

API's used: [OpenWeatherMap API](https://openweathermap.org/api), [Google Places API]
(https://developers.google.com/maps/documentation/places/web-service/overview)

### Part I - WeatherPy

# What's the Weather Like?
Created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. Utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and created a representative model of weather across world cities.

Created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, added a sentence or two explaining what the code is analyzing.

Run linear regression on each relationship. This time, separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots, took the time to explain what the linear regression is modeling. For example, described any relationships noticed and any other analysis.

* **Note:** Notebook conderations:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.



### Part II - VacationPy

# Where to Vacation Based on Weather Results?

Used jupyter-gmaps and the Google Places API for this part.

* **Note:** Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure you can't be charged. Check out [Google Maps Platform Billing](https://developers.google.com/maps/billing/gmp-billing#monitor-and-restrict-consumption) and [Manage your cost of use](https://developers.google.com/maps/documentation/javascript/usage-and-billing#set-caps) for more information.

* **Note:** if you having trouble displaying the maps, try running `jupyter nbextension enable --py gmaps` in your environment and retry.

To complete this part, I had to do the following:

* Created a heat map that displays the humidity for every city from Part I.

* Narrowed down the DataFrame to find the ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Dropped any rows that don't contain all three conditions. You want to be sure the weather is ideal.

  * **Note:** Feel free to adjust to your specifications but be sure to limit the number of rows returned by your API requests to a reasonable number.

* Used Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Plotted the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.



