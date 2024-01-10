# Data_analytics_capstone
# Data_analytics_capstone
Capstone project of the Google Data Analytics Certificate course.
We will be analysing
Ask Phase
Business task: Design marketing startegies to convert casual riders into annual members
Stakeholders: Lily Moreno: Director of marketing and manager
 Cyclistic Executive Team: A team who will decide whether to approve the recommended marketing program or not 
 Cyclistic marketing analytics Team: A team of data analysts responsible for collecting, analyzing, and reporting data

 Prepare Phase
 I will use the public data of Cyclistic’s historical trip data to analyze and identify trends. The data has been made available by Motivate International Inc. under the license. I am using Microsoft Excel to get a glimpse of the data. 
 There is one csv file for each month and has information about the bike ride which contain details of the ride id, rideable type, start and end time, start and end station, latitude and longitude of the start and end stations.
 For the purpose of my analysis I will use the csv files from november 2022 to october 2023.
 We will be extracting all of our files into a folder “Divvy_Monthlytripdata” to organize and provide context.

We will also be renaming the files to represent the data more clearly, it would also help with readability for other team members. Below is how I would do so:

(202101-divvy-tripdata.csv) -> (2021_01.csv)

(202102-divvy_tripdata.csv) -> (2021_02.csv)

and so on.


In order to process the 5,595,063 total records, spreadsheets wouldn’t be able to handle the sheer amount of data. In this case, we would be using Rstudio instead.

Firstly, we would need to install & load the packages required for this process, which in this case will be: Tidyverse, Janitor & Lubridate.

Process
In order to process the 5,595,063 total records, spreadsheets wouldn’t be able to handle the sheer amount of data. In this case, we would be using Rstudio instead.

Firstly, we would need to install & load the packages required for this process, which in this case will be: Tidyverse, Janitor & Lubridate.
The next step would be to merge all the csv’s(which we will now call dataset) into one table, however before doing that we would need to verify if there are any extra or missing columns.
We would also need to check if there are any discrepancies with formatting as well (maybe one dataset’s ID column is formatted as INT and another dataset’s ID column is formatted as CHR). We would do this by using ‘str()’ to list the structure of our datasets.

Now we’re ready to merge all datasets into one table(which will be called a dataframe), which I will be naming merged_df, and to do that we would be using bind_rows.

After that, we will also be cleaning our column names to remove spaces, parentheses, camelCase, and so on. This will also automatically separate words by capital case. IE:

This.Is An.Example -> this_is_an_example
This is An example -> this_is_an_example

We should also remove any empty columns and rows in our dataframe, we can do so by using remove_empty().



