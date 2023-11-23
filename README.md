## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data analysis](#data-analysis)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)

  
## Project Overview:
The analysis aims to uncover trends, compare salaries between departments, categories of employees working overtime, job level earning the highest salary and the rationale for this, compare current average work-life balance, etc. Rigorous data cleaning, modeling and visualization were performed using Power BI. 

<img width="577" alt="HR Analysis Dashboard" src="https://github.com/Oludamilola87/HR-Analysis-PowerBI/assets/151797326/9019bf80-957b-40ca-8528-98aa38dffea4">

## Data Source:
HR Data: The primary dataset used for this analysis is the HR_data Excel file, which contains detailed employee information. The data utilized for analysis was sourced from Kaggle, a renowned platform for hosting and sharing datasets.

## Tools:
Data was cleaned and transformed using a power query then data analysis and visualisation were done using Power BI.
- Power Query - Data cleaning
- Power BI - Data analysis and visualization

## Data Cleaning and Preparation
In the initial data preparation phase, we performed the following tasks:
- Data loading and inspection
- Data transformation (Replacing values, removing unnecessary columns, used custom columns, changing data types, e.t.c.)
- Data cleaning and formatting

## Exploratory Data Analysis
EDA involved exploring the sales data to answer key questions:
- the percentage of employee working overtime, their gender and status?
- Which job level received the highest salary?
- what is the number of employees on overtime?
- what is the average working years by gender?
- what is the monthly salary by department?
- what is the number of job roles in the organisation?
- what is the annual salary?
- How is average work-life balance compared to target?
- What is the number of employees?
- What is the average monthly pay?
- What is the average length of employment?

## Data analysis
measures were created such as average monthly pay, maximum no of job level, no of employees on overtime.

`Average Monthly pay = AVERAGE(HR_Analytics[MonthlyIncome])`

`Max no of job level = 
  MAXX(
    VALUES(HR_Analytics[JobLevel]),
    CALCULATE(
        COUNTROWS(HR_Analytics),
        ALLEXCEPT('HR_Analytics', HR_Analytics[JobLevel])
    )`

`No of employees on overtime = COUNTROWS(FILTER(HR_Analytics,HR_Analytics[OverTime]=1))`
    

## Key Insights
Our analysis revealed some key insights and we were able to use the key insights to make recommendations.
- 28% of employees work overtime.
- 44% of employees who work overtime are married, compared to singles and divorcees who make up 31% and 23%, respectively.
- The average work-life balance (2.76) is extremely low compared to the target value of 4.50. 
- Job level 2 receives the highest salary compared to other job levels. 
- The salary of the research and development department is 63% higher compared to sales and human resources


## Recommendations
The HR Analysis underscores critical areas demanding organisational attention. A staggering 28% of employees working overtime signals a potential risk of burnout, necessitating immediate action. To enhance work-life balance, strategies like workload redistribution or staff augmentation are recommended. Notably, 44% of those working overtime are married, suggesting a need for tailored support programs, possibly involving flexible schedules or family-friendly policies. The stark disparity between the current work-life balance rating (2.76) and the target (4.50) underscores the urgency for comprehensive initiatives, including flexible work arrangements and well-being programs. Acknowledging the nuanced challenges faced by married employees and implementing targeted solutions can foster a more balanced and sustainable work environment. These recommendations aim to fortify employee well-being, mitigate burnout risks, and align organizational practices with the evolving needs of the workforce.

