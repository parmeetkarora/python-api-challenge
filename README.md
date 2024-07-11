Python API Project - What's the Weather Like?
Background
This python is created to visualize the weather of 580 cities across the world. The premise of the analysis was that specific weather variables (y-axis) are correlated with (possibly dependent on) latitude (x-axis). The four comparisons were: 1) Temperature vs. Latitude, 2) Humidity vs. Latitude, 3) Cloudiness vs. Latitude, and 4) Wind Speed vs. Latitude.
Part I – WeatherPy
Date: 2024-06-17
The purpose of this project was to analyze how weather changes as you get closer to the equator. To accomplish this analysis, we first pulled data from the OpenWeatherMap API to assemble a dataset on over 580 citites.
After assembling the dataset, we used Matplotlib to plot various aspects of the weather vs. Latitude Factors we looked at included: temperature, cloudiness, wind_speed and humidity. This site provides the source data and visualizations created as part of the analysis, as well as explanations and descriptions of any trends and correlation witnessed.
•	Max Temperature(F) vs. City Latitude
•	Humidity (%) vs. City Latitude
•	Cloudiness (%) vs. City Latitude
•	Wind Speed (mph) vs. City Latitude

Observation
1.	The correlation between temperature and distance from the equator (i.e., positive and negative latitudes) is strong. 
Northern Hemisphere:
Performing a linear regression analysis on the relationship between maximum temperature and latitude in the Northern Hemisphere. The r-value of 0.422 indicates a moderate positive correlation between these two variables. it indicates that approximately 42.24% of the variation.
Max temperature drops as the latitude increases.
Southern Hemisphere:
The ( R^2 ) value of 0.7389 indicates that about 73.89% of the variance. This value suggests a strong correlation between the two Max temperature and Latitude

2.	The correlation between humidity, cloudiness and wind speed was low 
NORTHERN HEMISPHERE
The R-squared value 3.284260298844667e-05, is very close to zero. A value close to zero indicates that there may not be a linear relationship between Latitude and Humidity. 
SOUTHERN HEMISPHERE
The R-squared value 0.00628893090700073, is still very close to zero. This value indicates that only about 0.63% of the variance.
A low R-squared value like this suggests that the independent variable has very little explanatory power in predicting the dependent variable. Again it indicates almost no relationship between latitude and humidity
Northern hemisphere
•	The R-squared value 0.013775281652776647, is quite low. This value indicates that approximately 1.38% of the variance and indicates no relation between Latitude and cloudiness
•	A low R-squared value suggests cloudiness has limited explanatory power in predicting the latitude.
Southern Hemisphere
•	The R-squared value 0.008792074185791933, is relatively low. This value indicates that around 0.88% of the variance in cloudiness can be explained by the Latitude.
Northern hemisphere
•	The ( r^2 ) value you is 0.0399, which means that about 3.99% of the variability and this value indicates a weak relationship between the Latitude and Wind speed.
Southern hemisphere
•	The ( r^2 ) value  is 0.0249, which means that about 2.49% of the variability and again this value also indicates a weak relationship between the two variables.
REQUIREMENTS
The first requirement is to create a series of scatter plots to showcase the following relationships:
•	Temperature (F) vs. Latitude
•	Humidity (%) vs. Latitude
•	Cloudiness (%) vs. Latitude
•	Wind Speed (mph) vs. Latitude
After each plot, add a sentence or two explaining what the code is analyzing.
The second requirement is to compute the linear regression for each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):
•	Northern Hemisphere - Temperature (F) vs. Latitude
•	Southern Hemisphere - Temperature (F) vs. Latitude
•	Northern Hemisphere - Humidity (%) vs. Latitude
•	Southern Hemisphere - Humidity (%) vs. Latitude
•	Northern Hemisphere - Cloudiness (%) vs. Latitude
•	Southern Hemisphere - Cloudiness (%) vs. Latitude
•	Northern Hemisphere - Wind Speed (mph) vs. Latitude
•	Southern Hemisphere - Wind Speed (mph) vs. Latitude
After each pair of plots, explain what the linear regression is modeling. For example, describe any relationships that you notice and any other findings you may have.
Your final notebook must:
•	Randomly select at least 500 unique (non-repeated) cities based on latitude and longitude.
•	Perform a weather check on each of the cities using a series of successive API calls.
•	Include a print log of each city as it's being processed, with the city number and city name.
•	Save a CSV of all retrieved data and a PNG image for each scatter plot.
Part 2: VacationPy

Create a map that displays a point for every city in the city_data_df DataFrame 
Narrow down the city_data_df DataFrame to find your ideal weather condition 
For each city in the hotel_df DataFrame, use the Geoapify API to find the first hotel located within 10,000 metres of your coordinates 
Add the hotel name and the country as additional information in the hover message for each city in the map. 
I installed geoviews, pyproj and cartopy to get the map view
Add a .gitignore File
For this assignment, you will need to add a .gitignore file to your repo. Doing so will prevent the api_keys.py file that contains your API key from being shared with the public. If you skip this step, anyone using GitHub could copy and use your API key, and you may incur charges as a result.
To get started, type git status in the command line to see a list of all the untracked files that you have created so far.
To add only the WeatherPy.ipynb file to GitHub, for example, type git add WeatherPy.ipynb. Keep in mind that you would have to add each file individually when adding or updating a file. A more efficient solution is to add all of the files that you don't want to track to the .gitignore file.

Before adding your files to GitHub, add api_keys.py to the .gitignore file by following these steps:

Open your python-api-challenge GitHub folder in VS Code.

Open the .gitignore file and type the following code on the first line:

# Adding config.py file.
api_keys.py
In the command line, type git status and press Enter. The output should indicate that the .gitignore file has been modified and the api_keys.py file is untracked.

Use git add, git commit, and git push to commit the modifications to the .gitignore, WeatherPy.ipynb and VacationPy.ipynb files to GitHub.

On GitHub, the only new python files you should find are WeatherPy.ipynb and VacationPy.ipynb.
