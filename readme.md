# Project: Write a Data Science Blog Post

## by Michael F. H. Georgy

## Motivation
During my work on the Data Analyst Nanodegree program with Udacity, I came across an interesting data set for the GoBike bike-sharing system (now called Baywheels) covering the greater San Francisco Bay area. This is a network of rentable bicycles available at 262 stations throughout the bay area to rent with a credit card.
I was wondering whether the idea was actually working and if people did depend on bikes in their daily life, so I decided to collect the data of the first 3 months of 2020 and work on it. You can find the link to my original work in this [Github repo](https://github.com/michael-fawzy/DAND5-Communicate-Data-Findings)).

## Business Understanding
GoBike bike-sharing system (now called Baywheels) is a network of rentable bicycles covering the greater San Francisco Bay area. It's available at 262 stations throughout the bay area to rent with a credit card.
They have two types of users; casual customers and subscribers(members).
The questions that arose my attention were:
1. When were most trips taken in terms of “day of the week”?
2. How long did the average trip take?
3. Did the trip duration depend on the user type?
4. Is the idea working?

## Data Understanding and Preparation
This data set includes information about individual rides made in GoBike bike-sharing system (now called Baywheels) covering the greater San Francisco Bay area in the first 3 months of 2020.

The dataset was downloaded from https://s3.amazonaws.com/baywheels-data/index.html and multiple data files needed to be joined together to get a single dataset that required some data wrangling to prepare it for analysis.

The following libraries were used:
pandas, numpy, seaborn, matplotlib, zipfile, requests, and io


Data wrangling included the following:

	Data was gathered, assessed and cleaned as follows:

	I- Tidiness
		T1. Month column added  with the month name as value so that it is easy to distinguish the month after joining the datasets.

		T2. 3 separate dataframes joined into 1.

		T3. Unrequired columns for analysis (ex: start_station_latitude, start_station_longitude, end_station_longitude, end_station_longitude) were deleted.

		T4. Columns containing duration in minutes, hours, and days were added to improve perception of time.

		T5. 2 columns (start_day, end_day) containing day name obtained from start_time and end_time were added after converting data type to datetime.

	II- Quality
		Q1. Erroneous datatypes (start_time, end_time, start_station_id, end_station_id, bike_id) were converted to string since no operation will be performed on its values.

		Q2. Outlier in Jan dataset was deleted

For more details on the process, please check the jupyter notebook.

## Data Modeling
The data didn't require modeling. Statistical approaches were applied to get the required insights.
More details on the results and visualizations can be found in the jupyter notebook.

## Summary of Findings
The Most important findinngs are:

1. An average ride duration lies in the 3-14 minute range.
2. Most trips trips started and ended on Wednesday.
3. At durations less than or equal to 60 minutes, both customers (casual) and subscribers (members) have achieved similar duartions of use
4. When viewed by Month, without setting a duration limit, the plot shows that some customers had longer trip durations than subscribers.
5. The idea is succeeding since the average Trip duration has been increasing since Jan 2020 and reached it's peak in March which concludes that people are depending more on bikes to go to farther places.

You can find more detailed explanation with plots in this [medium post](https://michaelfawzy.medium.com/ford-gobike-is-it-working-5bafbea214b6)

## Files
The current repo was created specifically for the 1st project in the Data Scientist Nanodegree "Write a Data Science Blog Post". It contains the following files:

1. Ford_GoBike.ipynb: This is the original file where all the work was done.
2. Ford_GoBike.html: The HTML version of the previous file.
3. Readme file: A file to provide project description and summary of the results.
4. Medium Blog Post.docx: An MS Word file used to write the post before publishing it on Medium.
