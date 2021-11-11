# Weather API Project

## WeatherPY
This notebook first produces a paired list of latitudes and longitudes using the `random` command from the **numpy** module.

It then generates a list of cities based on these co-ordinate pairs using the **citipy** module, the last line of this cell outputs the length of the `cities` list to confirm that the `for` loop is functioning correctly.

The list of cities is the sent through a `for` loop which calls the **openweather** API. If the city name is found a confirmation message is printed that the city is processed and a collection of data is saved to a series of lists. The created lists are then formed into a dictionary which is translated into a data frame and exported as a CSV file.

The notebook then produces a series of plots evaluating the data for latitude vs cloudiness, wind speed, and humidity. These plots are also saved as seperate PNG files.

A series of linear regressions are run comparing the northern and southern hemispheres, comparing latitude vs max temp, humidity, cloudiness and windspeed.

## VacationPY
This notebook retrieves the saved CSV from WeatherPY, first it creates a heatmap based on the humidity value.  Then cities are removed based on hard coded variables, in a user facing environment these parameters could easily be attached variables which accept input.

The notebook then calls the **Google Maps** API to locate places to stay in the remaining cities. The information for these places are then added to markers on the heatmap.
