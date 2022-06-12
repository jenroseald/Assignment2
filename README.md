# Assignment2
Summary observations of case and vaccination data

Two different csv files were analysed as part of week 2, course 2 assignment activity:
-	cases.csv
-	vaccinated.csv

The cases file contains does not appear to contain a primary key / unique identifier. Within the vaccination file, the date can be used as a primary key. As no index was specified when both files were read into DataFrames, python auto created unique identifier indexes for both data sets.
Both data sets were inspected in terms of their shape, size and type
Both the cases and vaccinated DataFrames have 7584 rows. The cases DataFrame has 12 columns and the vaccinated DataFrame has 11 columns. Data types consist of objects, floats and integers.

Data was also checked for missing values. There does not to be any missing data within the vaccination.csv, however there are 2 rows that contain missing data within the cases.csv. Further analysis shows that this missing data can be classed as MNAR (missing not at random) as it occurs within the Bermuda state and on the two days when Hurricane Teddy hit Bermuda on the 21st to 22nd September 2020.
Subsets of both DataFrames were created to specify Province/State as Gibraltar. The Cases DataFrame was further filtered by date, deaths, cases, recovered and hospitalised. The vaccinated Data Frame was further filtered by date, vaccinated, first dose and second dose.

Overall Initial insights:
-	Hard to see how rate of death and vaccination rages have changed over time - can visualise in excel but at moment, can’t in python.
-	Average mean deaths are low compared to average case numbers.
-	Distribution looks skewed - upper quartile is close to max.
-	When using describe(), the count result does not provide valuable insight as it only counts rows of data.

Gibraltar subset observations:
-	The Gibraltar Intermediate Region Code is set to Zero - is this correct?
-	Vaccination data does not start until 11 January 2021.
-	Case data does not start until 4 March 2020
-	Cases peaked on 14 October 2021
