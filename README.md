# ETL_Project
Homicides & The Stock Market
Team Members:
Yannick Kalukuta
yanowen
Vijay Bagavatula
vijayb023
Adil Sarwar
asarwar1
Lawrence F.
lferretti
 
Project Objective: We will be comparing and contrasting murder, homicide and manslaughter in various cities across the United States and seeing how it is affected by stock market price fluctuations. 
Cities we derived data sets for: 
Atlanta
Boston
New York
Philadelphia
Austin
Chicago
Los Angeles
Detroit
Baltimore
Denver
Columns: CITY(STRING), LAT(FLOAT), LONG(FLOAT), OFFENSE_CODE_GROUP(STRING), DESCRIPTION(STRING), DATE (TIMESTAMP)

Data Import/Extract Sources and Method: 
-	www.kaggle.com
-	GCP - (Google Cloud Platform)
Essentially, we used the website Kaggle to import homicidal data which we derived from 10 major cities in North America. All our data was already in a CSV format, so we simply merged all of our CSV files together using BigQuery. 
Data Acquisition: Our data is static currently. However, it has the potential to become dynamic over the course of the period.

Data Transform: We scraped the data in BigQuery and extracted the following columns from our city data sets: City, Date, Offense Code Group, Description, Latitude and Longitude. As far as the stock market data set is concerned, we all used the columns 

Data Integrity: For the most part, all our data sets had the information readily available which of course was relevant for our testing. But none of our city datasets are updated daily. However, our stock market dataset is updated on a daily basis. We decided to use stock market data for S&P 500 for the years ranging from 1958-2019. However, we did obviously run into a few issues as follows. The New York dataset had dates ranging from the years 1958-1995 which were all outliers as opposed to all other cities which had dates ranging from 2001-2019. Furthermore, the Atlanta dataset was only limited to the year 2017. The Austin dataset was only limited to the years 2014-2016 and had no data on Latitude and Longitude past the year 2014. Boston's dataset was missing 9 entries for latitude and longitude in the years 2017-2018. Our Los Angeles dataset had no data for latitude and longitude and our San Francisco dataset was limited to only 23 entries ranging from the years 2003-2017. Lastly, Denver's dataset had its dates in an odd date format “0014-01-12” (YYYY-MM-DD) which was difficult to read due to the first value being “0” instead of “2”. 

Data Refresh Frequency: Our data refresh frequency is on a yearly basis which covers 

Data Security: 

Data Loading and Availability: 

Data Quality: We used BigQuery which is a serverless, highly-scalable, and cost-effective cloud data warehouse. 


