# VacationPy and WeatherPy

This project includes two Jupyter notebooks - WeatherPy and VacationPy - that use Python, Pandas, and APIs to visualize the weather of 500+ cities across the world and identify ideal cities for vacation based on weather conditions.

# WeatherPy

**Overview**

The WeatherPy notebook uses Python libraries, including Pandas and Matplotlib, to create a representative model of weather across world cities. The notebook leverages the OpenWeatherMap API to create a dataset of over 500 random cities across the world and utilizes data from the API to create scatter plots that visualize the relationships between latitude, temperature, humidity, cloudiness, and wind speed. The data visualization shows how weather changes as we approach the equator.

![image](https://user-images.githubusercontent.com/119364045/230742929-58537693-1d01-471a-9c9d-af835dc4a973.png)


**Code**
The notebook begins by importing necessary libraries, reading in the API key, and creating a URL that can be used to call OpenWeatherMap API. It then uses the numpy.random library to generate random coordinates for cities, makes API calls to OpenWeatherMap for each of the cities, and stores the retrieved data in a Pandas DataFrame. It then uses the data to create scatter plots that visualize the relationship between latitude and different weather conditions, such as temperature, humidity, cloudiness, and wind speed.



# VacationPy

**Overview**

The VacationPy notebook builds on the dataset created in the WeatherPy notebook to identify the ideal vacation spots based on specific weather conditions. The notebook uses the Pandas library to filter the original dataset to include only cities that have temperature, wind speed, and humidity within certain desired ranges, and then leverages the Geoapify API to find the first hotel within 10,000 meters of each city's coordinates. Finally, it uses the hvplot library to create an interactive map with points that show the location of each city, with the size of the points representing the humidity level, and additional information such as the name of the nearest hotel and the country appearing in the hover message.

![image](https://user-images.githubusercontent.com/119364045/230743385-182c8de6-ece0-4281-8712-1c7d9cafbad8.png)



**Code**


The notebook begins by importing the necessary libraries, including hvplot, Pandas, and Requests. It then reads in the cities.csv file that was created in the WeatherPy notebook and uses Pandas to filter the cities based on certain weather conditions. It then uses the filtered data to call the Geoapify API to find the first hotel within 10,000 meters of each city's coordinates. It then creates an interactive map using the hvplot library, where the size of the points representing the humidity level and additional information, such as the name of the nearest hotel and the country, appearing in the hover message.

***required for hvplot:*** 
 Step 1.

conda create -n hvplot-env -c pyviz -c conda-forge -c nodefaults hvplot geoviews datashader xarray pandas geopandas dask streamz networkx intake intake-xarray intake-parquet s3fs scipy spatialpandas pooch rasterio fiona plotly matplotlib jupyter

 Step 2.
conda activate hvplot-env

 Step 3. 
pip install --upgrade nbconvert

 Step 4.
jupyter notebook




Overall, the project demonstrates the use of APIs, Pandas, and Python libraries to analyze and visualize real-world data.
