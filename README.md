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




