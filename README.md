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
![trips overview](Images/1. Trip Overview.png)


## Submission 

Your final submission should include:

* A link to your Tableau Public workbook that includes: 
  * 4-10 Total "Phenomenon" Visualizations 
  * 2 Dashboards
  * 1 City Official Map
  * 1 Story 
* A text or markdown file with your analysis on the phenomenons you uncovered from the data.

