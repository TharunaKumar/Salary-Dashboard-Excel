# Salary-Dashboard-Excel
Dashboard using Excel comparing salaries of different jobs    

![Salary_Dashboard_Image.png](/Image/Salary_Dashboard_Image.png)

## INTRODUCTION

This salary dashboard provides an analysis of salaries for different data jobs.  
The following Excel skills were utilized for analysis:

- **Charts**
- **Formulas and Functions**
- **Data Validation**

### DASHBOARD FILE
My final dashboard is in [Salary_Dashboard.xlsx](Salary_Dashboard.xlsx).  

## DASHBOARD BUILD

###  Charts

#### Data Science Job Salaries - Bar Chart

<img src="/Image/Bar_Chart.png" width="550" height="350" alt="Salary Dashboard Chart1">

- **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- **Design Choice:** Horizontal bar chart for a visual comparison of median salaries.
- **Data Organization:** Sorted job titles by descending salary for improved readability.
- **Insights:** This identifies salary trends of different roles. Senior roles and Engineers are paid more Analyst roles.

  ####  Country Median Salaries - Map Chart

![1_Salary_Dashboard_Chart2.png](/Image/Map_Chart.png)

- **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- **Design Choice:** Colour-coded map to visually differentiate salary levels across regions.
- **Data Representation:** Plotted median salary for each country with available data.
- **Insights:** Visualises global salary disparities and highlights high/low salary regions.

  ###  Formulas and Functions

#### Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- **Insights:** Provides specific salary information for job titles, regions, and schedule types.

Background Table

![1_Salary_Dashboard_Screenshot1.png](/Image/Median_Salary_Table.png)

