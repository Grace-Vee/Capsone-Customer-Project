# Capsone-Customer-Project

## Project Title: LITA Capstone Customer Data

## Outline
[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Data Description](#data-description)

[Tools used](#tools-used)

[Data Cleaning and preparation](#data-cleaning-and-preparation) 

[Data Transformation](#data-transformation)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

[Insights](#insights)

[Recommendations](#recommendations)

### Project Overview
---
This project involve analyzing customer data to undestand customer behaviour for a subscription service, to identify segments and trends that caused cancellations and renewals of subscriptions. The analysis includes deriving various objectives to find subscription patterns and other insights that would enable us get informed decision on how to generate profits and reduce the canellation rate.

### Data Sources
---
Data used for this project was an excel data provided by the Incubator Hub LITA facilitators, the data was converted to CSV format, before importing to SQL, for easy and seamless analysis.

### Data Description
---
- The dataset includes the following fields:
    1. Customer ID: Unique identifier givemn to each customers
    2. Customer Name: Names of the customers
    3. Region: Regions subscriptions were made from
    4. Subscription Type: Type of Subscription package done bu the customers
    5. Subscription Start: Date when the subscription commenced
    6. Subscription End: Date when the subscription ended
    7. Cancelled: Shows if the subscription was actually cancelled or not
    8. Revenue: Total amount of money made from the packages
    9. Subscription Duration: Time the Subscription lasted
 
  ### Tools used
---
-  Microsoft Excel [Download Here](https://www.microsoftexcel.com)
     1. For Data Input
     2. For Analysis
     3. For Data Cleaning
     4. For Data visualization
-  Microsoft SQL Server [Download Here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
     1. To manage and querry data 
-  Microsoft Power BI [Download Here](https://www.microsoftpowerbi.com)
     1. For Data Transformation
     2. Data modelling
     3. To Create reports and dashboards that are collections of visuals.
-  GitHub [Download Here](https://www.github.com)
     1. For Portfolio Building

### Data Cleaning and preparation
---
During the initial phase of the data entry, the folowing actions were performed
     1.  Data quality was ensured by correcting any spelling errors, removing duplicate entries, and addressing 
         missing values.
     2.  Standardization: Used find and replace to standardize certain fields
     3.  Data import from Excel to SQL and Power BI

     ### Data Transformation:
 ---
 - Data was transformed to thoroughly clean, remove issues with data and increase column quality, column distribution and profile to 100%
      1. Data Types and Formatting: This was done to ensure all data fields were assigned the correct data types, with numerical fields formatted as whole numbers, 
         text as text and date fields set to date format. 
      3. Sorting: Sorted the dataset by the Date column to organize transactions chronologically.
      4. Created New Columns: Added a new column to have more calculations like Revenue

### Data Analysis
---
Some of the code used to analysed the data are:
```Excel
VLOOKUP(lookup_value,table_array,col_index-number,[range_lookup])
LEFT(text,[num_char])
SUMIF(range,criteria,[sum_range])
```
```SQL
SELECT * FROM [dbo].[LITA Capstone Dataset CSV(1)]

select Region,
count(customeriD) as Total_Customers
from [dbo].[LITA Capstone Dataset CSV(1)]
group by
Region;

select Top 1
SubscriptionType,
count(customerID) as Number_of_Customers
from 
[dbo].[LITA Capstone Dataset CSV(1)]
Group by
SubscriptionType
Order By
Number_of_customers DESC
```
```Power Bi
Total Customer = COUNT('Customer Data B'[CustomerID])
Avr Revenue 1 = AVERAGE('Customer Data B'[Revenue])
Rate Of Cancellation = SUM('Customer Data B'[Cancelled count])/SUM('Customer Data B'[Customer Count])
```

### Data Visualization
---
