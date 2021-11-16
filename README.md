# Citi Bike Analytics
This project uses a combination of python and Tableau to generate reports for CitiBike data in the year 2020.

## Background

![Citi-Bikes](Images/citi-bike-station-bikes.jpg)

CitiBike Program is the largest bike sharing program in the United States. Since 2013, the Citi Bike Program has implemented a robust infrastructure for collecting data on the program's utilization. Through the team's efforts, each month bike data is collected, organized, and made public on the [Citi Bike Data](https://www.citibikenyc.com/system-data) webpage.

## Python: Data Aggregation and Cleaning

Due to the limited nature of Tableau Public and the large amount of data, I made the decision to only work with Jersey City data from 2020 (62.4 MB). The process went as such:
* downloaded each Jersey City 2020 CSV file from the [Citi Bike Data](https://www.citibikenyc.com/system-data) webpage
* combined, converted (to pandas DataFrame), and exported all 12 CSV files with 8 lines of code (credit to [Free Code Camp](https://www.freecodecamp.org/news/how-to-combine-multiple-csv-files-with-8-lines-of-code-265183e0854/))
* removed anomalies (such as coordinates far outside the reach of a CitiBike or riders who claimed to be over 100 years old)
* saved and exported changes to CSV file (59 MB)

## Tableau: Data Visualization and Analytics 

After exploring the data and creating many visualizations in the Worksheets, 6 Dashboards were designed, then combined to create a Story. The whole Tableau file can be viewed by downloading the .twbx file on this repo or on [Tableau Public](https://public.tableau.com/views/CitiBike_Jersey_City_2020/CitiBikeJerseyCity2020?:language=en-US&:display_count=n&:origin=viz_share_link). See below for a non-interactive version of the Tableau Story.

## Trips Overview
There was CitiBike data available from 2013 till September 2021, but I wanted to focus on 2020, as that was a very pivotal year in New York. I also decided to only use Jersey City data due to the limitations of Tableau Public. There were 336,780 trips recorded in 2020. If broken down by Gender, Males took almost 60% of all trips, with Females trailing at 25% and Unknown at 15%. The Start and End Station chart highlights the most common routes, which based on the current filters (only stations with 10,000 trips as Start and End Stations) the roundtrip to and from Liberty Light Rail seems to be the most popular. According to the chart, people generally return the CitiBikes to the same location they started, as indicated by the dark diagonal line. Based on the bar/line graph, April and December had the lowest number of trips, while April through July had the longest average trip length. Of all weekdays, the weekend had the most trips, with all other days about equal.

![trips overview](Images/1_Trip_Overview.png)

## Trip Duration - Pt. I
Below are two graphs depicting the number of trips taken within each 5 minute increment. Most trips were less than an hour, but there were also trips lasting 37 days, so neither graph can really show the extremely long rides. The next Dashboard solves this by breaking up the rides up into 3 categories: < 1 hr, 1-24hr, and >24hr.

![trips duration pt 1](Images/1_Trip_Overview.png)
