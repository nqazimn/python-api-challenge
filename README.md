# Python-API-Challenge
![gif_image](/Outputs/Images/10.Ideal_vacation_spots_02012020.PNG)
## Background
There are essentially 3 main objectives:-
1. Analyze the relationship between various weather parameters (_maximum temperature, wind-speed, cloudiness & humidity_) with Latitude.
2. Visualize the weather of 500+ cities using [OpenWeatherMap API](https://openweathermap.org/api) using gmap heatmaps
3. Search for ideal vacation spots (based on certain weather conditions) using Google Places API.
## Prerequisites
You should have the following python packages installed in your Python environment to run the included jupyter notebooks:-
```
os
random
pandas
numpy
scipy
matplotlib
datetime
os
citipy (source: https://github.com/wingchen/citipy)
pycountry (source: https://pypi.org/project/pycountry/)
gmaps
```
You will also require: _(a) Google Maps API key_ and _(b) OpenWeatherMap API key_ which can be replaced in ```api_keys_template.py```. The file then should be renamed to ```api_keys.py``` to work with the existing code.
## File Layout
There are 2 main folders which contain the Jupyter notebooks prepared for analysis.
1. The data retrieval from **OpenWeatherMap API** and data cleaning is peformed in _/WeatherPy/WeatherPy_data_retrieval.ipynb_. The data was retrieved on February 01, 2020. To ensure that the accurate results are shown in the analysis, a variable ```days_since_data_request``` has been encoded in the notebook. It is essential that this parameter be changed to obtain accurate plot titles.
**Example**: If the code is being run on February 9, 2020, then ```days_since_data_request = 8```. The ```timedelta``` function of ```datetime``` is used to show the correct date on plot titles.
2. The analysis of relationships between Latitude and weather conditions is performed in _/WeatherPy/WeatherPy_analysis.ipynb_. The analysis is performed for cities in Northern and Southern hemispheres for each of the four weather parameters mentioned above.
3. Visualizations and recommendation for ideal vacation spots based on given weather conditions is performed in _/VacationPy/VacationPy_analysis.ipynb_.
4. The generated images from analyses are exported as ```.png``` format and placed in _/Outputs/Images_ folder.
5. The queried dataframe using OpenWeather API on Feb 01, 2020 is also included in _/Outputs/weather_df.csv_.
## Major findings

**Maximum Temperature**:-

(1) Southern Hemisphere: Weak positive correlation with Latitude. As distance from South Pole increases, Maximum Temperature increases.

(2) Northern Hemisphere: Strong negative correlation with Latitude. As distance from North Pole decreases, Max Temperature increases.

**Humidity**: Humidity is **not** correlated with Latitude.

**Cloudiness**: Cloudiness is **not** correlated with Latitude.

**Wind Speed**:-

(a) Southern Hemisphere: Very Weak negative correlation with Latitude.

(b) Northern Hemisphere: Very weak positive correlation with Latitude.
