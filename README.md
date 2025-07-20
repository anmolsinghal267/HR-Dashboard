
# HR Attrition Analytics-Dashboard

## Problem Statement

"The Human Resources department of a company is experiencing a high rate of employee turnover, which is affecting productivity, morale, and operational efficiency. There is a need to develop an interactive Power BI dashboard that helps identify key factors contributing to employee attrition, monitor workforce trends, and support data-driven retention strategies. The dashboard should visualize metrics such as attrition rate, department-wise exits, tenure, job satisfaction, and performance levels to empower HR managers with actionable insights."

### Steps followed 
Data Cleaning 
- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present in column named "YearsWithCurrManager".
- Step 5 : Conditional column is added by the applied condition on "Attrition" column . If "Yes" then '1' else '0'.
- Step 6 : In order to remove those null values I sorted the column in Ascending Order and then I deleted top 57 rows inorder to get rid of those empty Rows.
- Step 7 : Whole Table was then selected and Duplicated rows as a whole was deleted.
- Step 8 : In the "BusinessTravel" column "TravelRarely" is replaced by "Travel_Rarely". 
- Step 9: Then the changes are closed and applied.

Dashboard Creation
- Step 10 : In the report view, under the view tab, black wallpaper was selected.
- Step 11 : Several important KPI's are showed using a card visual which includes "Overall Employee","Attrition Count","Attrition Rate","Average Age","Average Salary". 
- Step 12 : Visual filters (Slicers) were added for three fields named "Human Resources", "Research & Development", "Sales".
- Step 13 : New measure was created inside a Measure Table to calculate Total Attrition Rate.

Following DAX expression was written for the same,
        
        Attrition Rate = [Total Attrition]/SUM(HR_Analytics[EmployeeCount])
- Step 13 : A donut chart is used to represent "Attrition by Education Field"
- Step 14 : A bar chart and a column chart was also added to the report design area representing the "Attrition count by Age Group" and "Attrition count by Salary".
  
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some Employees.

All these values have been ignored while calculating Attrition rate of Employess.

- Step 12 : Various other visualizations representing various factors of Attrition by "Line Graph","Tree Map","Funnel chart"and with the "Matrix" 
- Step 13 : The report was then published to Power BI Service.
 
# Insights

A single Double Page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Employees = 1416
 Attrition Rate is = 16.17%


           thus, a little higher considering company's Target of 15%
           

  ### [2] Age Group Factor  
  Maximum Attrition is among the Young age group people with an age group of about 26-35 , depicting their curiousity of exploration.

 ### [3] Some other insights
 
 ### YearsAtCompany
 People who have spent more than Five years at the company have less chances of Attrition.
 
 ### Salary
Employees getting a salary of less than 5k have attritiated the most.
Hence Company can look towards increasing their basic Salary.
         
### JobRole

Maximum People attritiated are from "Laboratory Technician" role from Research and Development Department.
