# Average_Max_Temp
Have a list of cities and return the average maximum temperature predicted for the next 7 days.


The initial request was to use the MetaWeather API, but it is no longer working, and all callbacks returned errors. According to my research the API was turned off.

The solution was pivoted to another public-use API, open-meteo (https://open-meteo.com/en/docs?), which is functional and contains the necessary information for the initial project request.

Below is the code used to fulfill the scope for three cities: Salt Lake City, Los Angeles, and Boise, Idaho.

The latitude and longitude of each city are required; this can be found on the API provider's website, as per the link above.

By providing a list of city names, latitude, and longitude, the "get_weekly_avg_high" function is used. This function parallelizes API calls, allowing up to 5 workers to be called simultaneously. The "fetch_city_weather" function queries the API, extracts the data, and calculates the average maximum temperature for the next 7 days for each city.

The result is a dataframe with the features city name, latitude, longitude, and average_maximum_temperature in °C.

Above each snippet is a brief description of its function.
