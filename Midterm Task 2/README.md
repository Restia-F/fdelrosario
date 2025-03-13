# [Midterm Lab Task 2](https://github.com/user-attachments/files/19111495/Midterm.Lab.Task.2.xlsx)
This portfolio shows how to use Power Query for data preparation and cleansing. The dataset is made up of several connected tables, and before analysis, cleaning methods are used to enhance the consistency and quality of the data.

## Step-by-Step Process
### Step 1: Download and Load Data  
1.  Download the dataset (uncleaned_ds_jobs.csv).  
2.  Open Excel.  
3.  Navigate to Data > New Query > Open File > Text/CSV.  
4.  Click Load, then Edit with Power Query Editor.  

### Step 2: Duplicate Raw Data  
1. Right-click on the dataset in the Queries window.  
2. Select Duplicate. 

### Step 3: Clean Salary Data  
1. Select the Salary Estimate Column.  
2. Select Transform Menu → Extract → Text Before Delimiter.  
3. Type "(" and click OK.  
4. Create two new columns: Minimum Salary and Maximum Salary.  
- Select Salary Estimate column, then Add Column Menu, Column from Examples, and From Selections.  
- Enter the first minimum wage amount and click Enter (all rows will auto-fill).  
- Rename the column as "Min Sal"  
- Repeat the process for maximum salary.  

### Step 4: Add Role Type Column  
1. Go to the Add Column Menu → Custom Column.  
2. Rename the column "Role Type"  
3. Using this logic:  
- Assign "Data Scientist" if the job title contains that word.  
- Assign "Data Analyst" if the job title contains that word.  
- Assign "Data Engineer" if the job title contains that word.  
- Assign "Machine Learning Engineer" if the job title includes "Machine Learning".  
- Alternatively, assign "Other"  
4. Change column type to Text.  

### Step 5: Split Location Column  
1. Select the location column.  
2. Add a Custom Column with Corrections:  
- If "New Jersey" is the location, assign ", NJ".  
- If "Remote" or "United States" is the location, assign ", Other".  
- If Location = "Texas", assign ", TX"  
- If Location = "California": Assign ", CA"  
3. Click OK and then select the new column.  
4. Navigate to Transform > Split Column > By Delimiter (comma ",").  
5. Click OK.  

### Step 6: Split Size Column  
1. Create two new columns: MinimumCompanySize and MaximumCompanySize.  
2. Split values using the same technique as in Salary Estimate.  

### Step 7: Handle Negative Values  
1. Filter out -1s from the competitors column.  
2. Remove 0s from the Revenues column.  
3. Remove all -1s from the Industry column.  

### Step 8: Clean Company Names  
1. Remove any extra characters or ratings after company names  

### Step 9: Copy Cleaning Steps as Proof  
1. Go to the Home Menu and select Advanced Editor.  
2. Copy the code and save it to your portfolio.  


### Step 10: Reshape and Group Data  
#### Group by Role Type  
1. Duplicate the raw data and rename it "Sal By Role Type Dup".  
2. Select only the Role Type, Minimum Salary, and Maximum Salary columns.  
3. Change the Minimum and Maximum Salary types to currency.  
4. Multiply the values by 1000 (Numbers Column → Standard → Multiply → Type 1000).  
5. Group the rows by Role Type and find the average for the minimum and maximum salary.  

#### Group by Company Size  
1. Create a raw data reference and rename it "Sal By Role Size ref".  
2. Select only the Size, Minimum Salary, and Maximum Salary columns.  
3. Change the Minimum and Maximum Salary types to currency.  
4. Multiply the values by 1000.  
5. Group rows by size and calculate the average for the minimum and maximum salary.  


### Step 11: Merge State Mapping  
1. Click Unclean DS Jobs.  
2. Create a new query by right-clicking in the Queries pane and selecting Open Workbook State Mapping.  
3. Select the columns, then click OK.  
4. Select the Uncleaned DS Jobs inquiry.  
5. Select the state abbreviation column in both queries.  
6. Click Merge → OK.  
7. Rename the merged column to "State Full Name".  
8. Remove the nulls and blanks.

### Step 12: Group by State  
1. Create a raw data reference and rename it to "Sal By State ref".  
2. Select only the State Full Name, Minimum Salary, and Maximum Salary fields.  
3. Change the Minimum and Maximum Salary types to currency.  
4. Multiply the values by 1000.  
5. Group rows by state full name and find the average for the minimum and maximum salary.  



### Step 13: View Query Dependencies  
1. Go to View Menu → Dependencies.  
2. Check that all queries are linked correctly.  

## Here are the screenshots showcasing the table transformation process
### Here's the screenshot of my output before I started data cleaning (see screenshot)
![Image](https://github.com/user-attachments/assets/38ea140c-bb3b-44c1-b2cb-a25601ea8467)
## Here's the screenshot of the Advanced Editor
![Image](https://github.com/user-attachments/assets/363e27b5-76d2-4561-8907-6718216a3d45)
### Here's the screenshot of my output after I started data cleaning (see screenshot)
![Image](https://github.com/user-attachments/assets/dd368a40-ad15-4159-a5dd-3ab372efe33d)


### Here's the screenshot of Sal By Role type (see screenshot)
![Image](https://github.com/user-attachments/assets/4a2b5298-8a0b-4440-8e83-de4f0810d89d)
### Here's the screenshot of Sal By Role Size (see screenshot)
![Image](https://github.com/user-attachments/assets/f193001b-6da3-46fa-aa36-877f20cefc81)
### Here's the screenshot of Sal By State (see screenshot)
![Image](https://github.com/user-attachments/assets/d6e69440-32be-4cbf-af2c-5d8a99dfdcbc)
### Here's the screenshot of States (see screenshot)
![Image](https://github.com/user-attachments/assets/8c402690-1e7a-4253-899d-e0f74b6e302a)
### Here's the screenshot of the Query Dependencies
![Image](https://github.com/user-attachments/assets/e964092b-b535-4357-86aa-13795196b172)
