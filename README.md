# EXLORATORY DATA ANALYSIS
 Explored and analyzed a large dataset using SQL to uncover key insights. Focused on data cleaning, identifying patterns, and generating actionable insights for decision-making. The data used was gotten from the web and the link is provided: [Raw Dataset](https://www.kaggle.com/datasets/theakhilb/layoffs-data-2022).  
## DATA COLLECTION AND SKILLS USED.  
The data was collected from Kaggle website and it shows the different columns relevant that was used for the EDA process. After extraction, the data was cleaned using four different techniques:  
1. Removal of Duplicates  
A row number was used to match against all the columns in the dataset to find any duplicate after which a Common Table Expression (CTE) was used to confirm that there was no row number greater than one. Row Number greater than one would signify a duplicate.

2. Text Standadization  
Firstly, the company column was trimmed and then the industry column was standadized so that there were no spelling errors as was particularly found in cryotocurrency. Also the country United States. was updated to remove the dot in front. In addition to those, the date column was updated from a string into a date format that SQL recognizes

3. Blank and Null    
Blank and Null dataset that can be populated were done by comparing to relevant data. Companies like Airbnb that had the industry name (Travel) for some rows and blank/null for another row as compared and made to update. This was done by setting all blank industries to NULL and then updated to the relevant industry type using the self join command.

4. Removing Redundant Rows and Columns  
Rows that have both total_laid_off and percentage_laid_off as blank or null values were deleted because they will serve no function in subsequent Exploratory Data Analysis. Also, the Row_Number column that was created in the earlier stages of the data cleaning to remove duplicates was deleted because it is redundant and would not be used for further analysis.
## EXLORATORY DATA ANALYSIS AND FINDINGS  
The analysis of the dataset gave a general insight on the layoffs:  
-Maximum number laid-off in a day by a company as captured from the dataset was about 12,000 people.  
-The percentage laid-off was also investigated to see if there were any company that laid-off all the staff. The result of this query showed that the companies that had 100 percent layoffs were mostly startups.  
-Amazon also had the highest nimber of lay offs within the period of time under investigation as they had a total of 18,150 layoffs. Google, Meta, Salesforce, and Microsoft followed respectively.  
-When these companies are broken down by industries, the consumer and retail had the higest layoffs within the period of 3 years with 45,182 and 43,613 respectively.  
-Also, within the 4 years captured by the dataset (2020-2023), 2022 had the most layoffs with 2023,2020 and 2021 coming in as second, third and fourth respectively.  
-Common Table Expression (CTE) was used to find the rolling total of laid-offs across the months for the 4 years being looked at.  

## DISCUSSION AND INTERPRETATION  
The dataset analysis reveals significant patterns and trends in layoffs across different companies, industries, and time periods. Here are the key insights:

1. Large-Scale Layoffs Were Common in Big Tech
The highest single-day layoff recorded in the dataset was about 12,000 employees. This indicates that companies—especially in the tech sector—often conducted mass layoffs in large batches rather than gradually reducing staff.
Amazon led in total layoffs, with 18,150 employees affected, followed by other major tech firms like Google, Meta, Salesforce, and Microsoft.
This pattern suggests that large tech companies were significantly impacted by market conditions, potentially due to overhiring during the pandemic and economic downturns in subsequent years.
2. Startups Were the Most Vulnerable
Several companies had 100% of their workforce laid off, meaning they completely shut down. Most of these were startups, highlighting their vulnerability to economic downturns and funding shortages.
This suggests that startups often operate on tight financial margins, and when economic conditions worsen, they are more likely to collapse rather than implement partial layoffs.
3. Industry Trends: Consumer & Retail Were Hit the Hardest
The consumer and retail sectors experienced the highest layoffs, with 45,182 and 43,613 employees affected, respectively.
This trend indicates that businesses in these industries faced strong economic pressures, possibly due to changes in consumer behavior, inflation, or supply chain disruptions.
The high layoffs in retail suggest a shift toward e-commerce and automation, reducing the need for a large workforce in traditional retail.
4. 2022 Was the Peak Year for Layoffs
Among the four years analyzed (2020-2023), 2022 recorded the highest number of layoffs, followed by 2023, 2020, and 2021 in descending order.
This trend suggests that while 2020 (the start of the pandemic) led to some initial layoffs, companies recovered in 2021 before massive job cuts in 2022 due to economic uncertainty, rising interest rates, and cost-cutting strategies.




