A. Overview 

This dataset shows the cost of living indexes in different countries. It contains 202 rows and 5 columns. The data includes indicators such as the rent index, the groceries index, the restaurant price index, and the purchasing power index. It helps compare living costs across countries. 

* Dataset Size: 202 rows x 5 columns
* Final dataset after cleaning: 200 rows x 5 columns

Columns:

      •	Country (object): The name of the country where the data was recorded.
      •	Region (object): The geographical region to which the country belongs 
      •	Year (int): The year when the data was recorded.
      •	Average_Monthly_Income (float64): The average monthly income of individuals in USD.
      •	Cost_of_Living (int): The average monthly cost of living in USD, including essentials like housing, food, and utilities.

<img width="537" height="408" alt="image" src="https://github.com/user-attachments/assets/6bd16898-74af-4567-93bb-eb0b439c5c52" />

B. Data Cleaning
   
1. Duplicate Records
  *  Duplicates found: 2 rows
  *  Action taken: Removed both duplicate records to avoid inaccurate descriptive statistics.
  *  Reasoning: Each Country–Year combination must be unique to maintain data integrity and prevent double-counting.  

<img width="703" height="131" alt="Screenshot 2025-10-30 205804" src="https://github.com/user-attachments/assets/647d90b0-d549-4936-baf9-e6f716bc7e25" />

2. Missing Values
* Average_Monthly_Income
  - Missing rows: 160 and 176
  - Action taken: Replaced missing values using the Excel `MEDIAN()` function.
  - Reasoning: The median is less affected by extreme income differences and provides a more balanced estimate for imputation.

<img width="565" height="504" alt="image" src="https://github.com/user-attachments/assets/4ed6f3f1-6f08-4ff7-8ed4-fd5df6a65730" />


* Region
  - Missing rows: 26 and 38
  - Action taken: Filled in missing regions manually, based on geographical knowledge (for example, Mexico → North America, Egypt → Africa).
  - Reasoning: Manual correction ensures accuracy in regional classification, which is critical for grouped visualizations and comparisons.

<img width="564" height="401" alt="image" src="https://github.com/user-attachments/assets/85a89897-2c24-44d7-aeca-e09eab668fa4" />

C. Descriptive Statistics

<img width="911" height="315" alt="image" src="https://github.com/user-attachments/assets/29f8f724-06f2-43a8-ad63-ab53a7d52e24" />

* The mean income (USD 4,243.967156) and mean cost of living (USD 3,705.127286) show that, on average, people earn slightly more than their basic expenses.
* The median values are close to the means, indicating a balanced data distribution without major outliers.
* The minimum values (income: USD 534.74, cost: USD 464.49) reflect developing countries with low earnings and expenses, while the maximum values (income: USD 7,976.56, cost: USD 6,981.02) represent high-income economies with higher living standards and costs.

D. Key Insights: 

1. Comparison of Average Monthly Income and Cost of Living by Region

This chart compares the average monthly income and cost of living in different regions.
* Europe and Asia have the highest incomes, with income slightly higher than the cost of living.
* North America shows similar income and living cost levels, meaning people earn about the same as they spend.
* In Africa, Oceania, and South America, income is lower, but the cost of living is also lower.
* Overall, higher-income regions also have higher living costs, showing a close relationship between the two factors.

<img width="1036" height="477" alt="image" src="https://github.com/user-attachments/assets/ebc39a01-9034-48ca-9c07-6900e176a40f" />

2. Income vs. Cost of Living

The scatter chart illustrates the relationship between Average Monthly Income and Cost of Living across 199 observations.  
* The data points are widely dispersed, showing no clear linear correlation between the two variables.  
* Some countries with higher living costs do not necessarily have higher incomes, while others with moderate costs achieve relatively high earnings.  
* This suggests that income and living expenses vary independently across regions, influenced by factors such as economic structure, purchasing power, and local price levels.

<img width="852" height="428" alt="image" src="https://github.com/user-attachments/assets/de20c864-2367-4e7a-84f6-82ab32e14f7c" />
