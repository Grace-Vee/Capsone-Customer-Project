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
![Cus table](https://github.com/user-attachments/assets/7e724407-6370-4e6d-8f17-5eaccb3e1aaa)

![Cus chat](https://github.com/user-attachments/assets/ffd76271-b946-4cb8-a1e6-634db47e182e)

![Cus SQL](https://github.com/user-attachments/assets/d7e75294-0cef-44c1-8c72-3592dd6048e6)

![Cus SQL 1 png](https://github.com/user-attachments/assets/bb1c5678-d25f-46d9-bfb1-57d399b04373)

![Cus SQL 2 png](https://github.com/user-attachments/assets/95568ac3-fac4-4ff9-af04-3a8b0a1c504b)

![Cus SQL 3 png](https://github.com/user-attachments/assets/dddef420-6dc6-4797-9637-bae10014b14f)

![Cus SQL 4 png](https://github.com/user-attachments/assets/a7e2a619-81b1-456e-bce2-32eef639c024)

![Cus SQL 5 png](https://github.com/user-attachments/assets/cabb21ab-7da8-4a7d-b2c6-c4078ce86db6)

![Cus SQL 6 png](https://github.com/user-attachments/assets/799f008b-4460-4dec-8540-89c76bd0853d)

![Cus visual](https://github.com/user-attachments/assets/ea8ba944-3849-4259-85cf-98eec854abc1)


### Insights
---
- The visual showed:
   1. Sales Revenue: Total revenue is 68 million naira, while average revenue is 2 thousans naira, with 25 billion naira total turnover, from 34 thousand customers 
      across 4 regions.
   2. Out of the 33,787 customers that subscribed, 15,175 cancelled their subscription, which gave us a 45% rate of cancellation.
   3. Regional Supscription Pattern: Subscription revenue was remarably high, with 16,958,763 naira in the Eastern region, 16,899,064 Naira in the southern region, 
      16,864,376 Naira in the Western region, and then 16,817,972 Naira in the Norther Region.
     
![Cus pattern](https://github.com/user-attachments/assets/d303ec9e-abc6-49f6-a2e1-ae9655168bf8)

   5. Cancellation counts: Northern region has the highest cancelled count of about 5067 counts, followed by southern region with 5064 cancelled counts and then 
      Western region with 5044 counts. None of the customers in the East cancelled their subscriptions
   6. Most Popular Subscription count: The Most popular subscription type is Basic, which means more of the customers were satisfied with the package
   7. Out of the 8488 total number of customers that subscribed, none of them cancelled in the Eastern Region, this shows that they were greately satisfieed with te 
      services rendered at that region
   8. Percentage cancellation: Only 30% of basic users cancelled their subscriptions, while 60% of Premium users cancelled their subscriptions and 60% of Standard 
      users cancelled their sunscriptions, one of the reasons while basic had the higheest revenue
     
### Recommendations
---
- The followings were recommended based on findings from the Data Analysis, which enabled us took informed decisions such as:
   1. Supsription pattern in the Eastern region should be studied extensively to know why none of the customers cancelled their subscriptions, this should be 
      implemented in all the regions, to boost revenue.
   2. Cost of subscriptions for both Premium and Standard should be reduced, this might probably be the reason why most of their users cancelled.
   3. The rate of cancellation (45%) is not encouraging, research need to be done to know why almost half percentage of the customers cancelled, these findings should 
      be integrated into the system, to prevent further cancelation
   4. The Company shouldbmake available more of basic susbcription, to satisfy customers wants
   5. Aggressive marketing should be carried on Premium and standard subscriptions, promotions should be done on these packages and loyalty rewards should alos be 
      given to top subscribers of these packages, to encourage more customers to subscribe to them
