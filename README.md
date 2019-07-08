# CKME136Project
Data Mining Transit Information from King St Pilot Project
Data Mining Transit Information from King St Pilot Project 
Introduction
Transportation impacts the lives of all Torontonians. While there is no easy answer to transport people more efficiently in the downtown core there has been an interesting pilot project on one of Toronto’s busiest streets, King Street. The King Street pilot project aims to improve transit reliability, speed, and capacity by giving transit priority on King Street from Bathurst Street to Jarvis Street. This capstone project will examine the effects of the King Street Pilot project has made on streetcar transportation in that area. This project will seek to quantify the changes the pilot project has made on travel times, and delays on the 504 streetcar route. Some example questions are: Did the pilot make an improvement to TTC travel time or reduce delays on that route? Data mining techniques using machine learning algorithms like clustering, logistic regression and classification will be used to find meaningful patterns in the dataset. 

Dataset
There are three datasets used for this project. Two datasets are from the City of Toronto Open Data (www.toronto.ca/open), more specifically, TTC travel and delay information for the King St. Pilot Project from 2017 – 2018. The third dataset is weather data for Toronto, Ontario provided by the Government of Canada (http://climate.weather.gc.ca). From this dataset the daily temperature and precipitation information from 2017 – 2018 will be used.
The datasets will be restructured and grouped by certain time of day ranges and then joined into one table for exploratory analysis and data modelling. The dataset will focus only on weekday information, thus, excluding weekends and holidays. Our area of interest will be anywhere between King St. and Bathurst St and King St. and Jarvis. We will be looking at 2017 and 2018 only, providing almost a year pre pilot project and post pilot project (the project started Nov 12 2017).

Table 1: Dataset Attribute Descriptions
Attribute	Description
date	Date of measurements
time_of_day	Time of day of measurements: Early, AM Peak, Mid, PM Peak, Evening, Late
day_of_week	Day of the week, eg. Monday, Tuesday, Wednesday.
no_of_screetcars	The number of streetcars on the route during the measurement period
direction	The direction the streetcar was travelling, either Eastbound or Westbound
avg_travel_time	The average travel time of street cars on the route during the measurement period.
no_of_delays	The number of delays the occurred on the route during the measurement period.
avg_delay_time	The average amount of delay time during the measurement period.
avg_speed	The average speed of the streetcars on the route during the measurement period.
temp	The average temperature during the measurement period.
weather_type	The type of weather during that period, either sunny/overcast, rain, snow, or freezing rain etc.
pilot_non_pilot	Label to indicate if the measurement occurred during the pilot or before the pilot project.


Approach
This project’s approach starts with importing, cleaning and restructuring the data. Data cleaning includes removing missing values, standardizing naming conventions and grouping measurements based on certain times of the day. Then, exploratory analysis is performed to become familiar with the dataset, identify outliers and relationships between attributes. Then data modelling will be used and then the results will be interpreted into meaningful observations. 

Step 1: Data Preparation
The first step is to collect the data sources from the City of Toronto and the Government of Canada websites for both 2017 and 2018. The data is imported into the software tools. Firstly, missing and NA values will be removed or estimated as necessary. In the case of the transit delay data, only delays that occurred with route 504 between Bathurst St. and Jarvis St. will be extracted for use in the dataset. Unnecessary attributes will be removed from the datasets, for example in the transit delay dataset attributes such as vehicle number and type of delay will be removed. In the case of the weather data, only the temperature and type of weather will be extracted for use in the main dataset. And for the TTC travel time dataset, attributes such as vehicle number, run number, and route number will be removed. Then the measurements will be restructured and grouped base on time of day, for example, a measurement taken at 5AM will be grouped into a category called “EARLY”. The datasets will then be joined based on date and time of day into the main dataset to be used for exploratory analysis and data mining. 
Step 2: Exploratory Analysis 
The step will help to better understand the data and to discover initial patterns in addition to getting familiar with the dataset. During this step, values will be plotted for visualization using scatter plots and box plots. This will also help in identifying outliers. Another part of this step will be to use a simple spearman correlation to uncover any potential relationships between attributes. Anything of interest will be included in the final report.
Step 3: Data Mining/Modelling  
In this step, machine learning K nearest neighbor clustering technique will be used to identify patterns in the data. During this step, measurements will be clustered into groups in order to identify unique characteristics.  Logistic regression will be used to identify relationships between attributes to identify which attribute had the most impact on streetcar travel time. Naive Bayes classification will be used to see if pre pilot project and post pilot project measurements can be predicted using the attribute of the dataset.  
Step 4: Interpretation/Evaluation
The final step will evaluate the accuracy of the models and interpret what the correlations and relationships between attributes mean to the impact of the King St pilot project. Can this analysis show improvements in transit due to the pilot project?

