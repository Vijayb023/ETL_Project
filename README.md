Stock Market Pricing & Homicide Rates
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
San Francisco

Data Import/Extract Sources and Method: 
-	www.kaggle.com
-	GCP - (Google Cloud Platform)
-https://finance.yahoo.com/quote/%5EGSPC/history?period1=-349815600&period2=1576904400&interval=1d&filter=history&frequency=1d

Essentially, we used the website Kaggle to import homicidal data which we derived from 10 major cities in North America. All our data was already in a CSV format, so we simply merged all of our CSV files together using BigQuery. 

Data Acquisition: Our data is static currently. However, it has the potential to become dynamic in the future. Since we found out that datasets on crimes in major cities in North America is limited. We will need to compare and contrast all our datasets and ensure their dates are roughly ranging between the years 1990 through 2019.

Data Transform: We scraped the data in BigQuery using SQL code and extracted the following columns from our city data sets: City, Date, Offense Code Group, Description, Latitude and Longitude. The following snippet is an example of how the Detroit dataset was cleaned up using SQL:
The following snippet is an example of how the San Francisco dataset was cleaned up using SQL:


As far as the stock market data set is concerned, we used jupyter notebook to merge this data set with all the consolidated cities dataset:

After the initial data extraction we were left with two seperate data sets. One was comprised of Homicide data. The other was data pertaining to the S&P 500. 

Data Integrity: For the most part, all our data sets had the information readily available which of course was relevant for our testing. But none of our city datasets are updated daily. However, our stock market dataset is updated on a daily basis. We decided to use stock market data for S&P 500 for the years ranging from 1958-2019. However, we did obviously run into a few issues as follows. The New York dataset had dates ranging from the years 1958-1995 which were all outliers as opposed to all other cities which had dates ranging from 2001-2019. Furthermore, the Atlanta dataset was only limited to the year 2017. The Austin dataset was only limited to the years 2014-2016 and had no data on Latitude and Longitude past the year 2014. Boston's dataset was missing 9 entries for latitude and longitude in the years 2017-2018. Our Los Angeles dataset had no data for latitude and longitude and our San Francisco dataset was limited to only 23 entries ranging from the years 2003-2017. Lastly, Denver's dataset had its dates in an odd date format “0014-01-12” (YYYY-MM-DD) which was difficult to read due to the first value being “0” instead of “2”. The reason we chose to use the S&P 500, is due to it its basket of information from over 500 of the top companies in the market. It can be stated that this could  be used to represent the Stock market as a whole. 

Data Refresh Frequency: Our data refresh frequency is on a yearly basis which covers dates ranging from 01/01/1958 through 1/31/2019. The data for the S&P 500 ranges from 1958 to 2019. The original csv file came from Yahoo finance a reputed source for financial information. 

Data Security: Since we used jupyter notebook, our data cannot be altered by any outside source. Therefore, it is secure according to the HIPAA considerations. 

Data Loading and Availability: We used jupyter notebook to load our datasets in order for clients and users to access the data but not manipulate it in any way. 

Data Quality: We used BigQuery which is a serverless, highly-scalable, and cost-effective cloud data warehouse. 
Conclusion: Data scientists interested in looking at correlations between stock market price fluctuations and homicidal death rates could use our consolidated dataset to support their hypothesis. 


