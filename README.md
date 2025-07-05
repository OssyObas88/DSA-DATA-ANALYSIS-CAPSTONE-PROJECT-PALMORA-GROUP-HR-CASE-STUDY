# DSA DATA ANALYSIS CAPSTONE PROJECT PALMORA GROUP HR CASE STUDY
This is my project work after the training organised by DSA. This repository is based on the final project work in the DSA Data Analysis training where students were given 3 files to work on but to analyze 2 out of the 3. This repository is the case 3 study (Palmora Group HR). 

## Steps taken to clean the data set
- I started by using countblank function to determine the number of blanks that needed to be filled.
- I proceeded to fill them with the required information.
- The next step was to import the data into my power bu environment and used the transform data function to work on the dataset. I removed the “null” for the columns where they appeared because they had no use. I ensured to use “keep top rows” function to keep the nulls from returning before clicking on close and apply.
- I re-launched the file and also imported the second file that also needs to be transformed and then clicked on transform data. 
- I unpivoted the table except the department column in order to establish a relationship between the datasets. I proceeded to create a “custom column” and named it Dept Rating.
- I merged the queries as new.
- Next, I created another custom column in order to formulate “annual bonus”.
- In order to show the pay distribution of employees, I created a conditional column to show the band of salary and to know the number of employees receiving the minimum salary of 90,000.
- Finally I clicked on close and apply.

## Key Measures

1.	Gender Distribution Analysis 
Measures Used
Gender Count = COUNT('Employee'[Gender])
Gender Percentage = DIVIDE(CALCULATE(COUNT('Employee'[Gender])), CALCULATE(COUNT('Employee'[Gender]), ALL('Employee'[Gender])))`

2.	Minimum Salary Requirement Analysis
Measures used
 Employees Below Minimum Salary = COUNTX(FILTER('Employee', 'Employee'[Salary] < 90000), 'Employee'[Salary])

3.	Rating insights based on gender
Measures used
Average rating by Gender = AVERAGE('Employee'[Rating])`
Rating Count by gender = COUNT('Employee'[Rating])`

4.	Salary Structure and Gender Pay Gap Analysis
Measure used
Average Salary by Gender = AVERAGE('Employee'[Salary])`
Salary Count by Department and Region = COUNT('Employee'[Salary])`

## Key Conclusions

### 1. Gender Distribution
- There is an observable gender imbalance across departments and regions.
- A portion of employees did not disclose their gender and were categorized as **“Undisclosed”** for clarity.

### 2. Salary Structure & Compliance
- Multiple employees earn **below the mandated $90,000 minimum wage**, signaling a compliance issue.
- Salary bands show most employees fall below the $100,000 threshold.

### 3. Gender Pay Gap
- Significant pay gaps exist between male and female employees across several departments and regions.
- Targeted adjustments are needed in high-disparity areas.

### 4. Performance & Bonus Allocation
- Bonus payouts were calculated using performance-based rules.
- Total compensation (salary + bonus) was summarized per employee and region-wide.

### 5. Organizational Insights
- Departments with the widest salary disparities and lower ratings were flagged.
- Visual dashboards deliver insights for prioritizing inclusion and equity improvements.


## Recommendations

- **Audit and raise** salaries below the $90,000 policy threshold
- **Promote equity** in compensation by targeting affected departments and regions
- **Implement inclusive policies** encouraging gender disclosure (with privacy)
- **Standardize rating systems** to reduce bias in performance assessment
- **Use dashboards regularly** to monitor improvements
-	**Implement equitable pay practices**, focusing on regions and departments with the largest disparities.
-	**Develop gender inclusion programs** and encourage voluntary gender disclosure with privacy assurance.
-	**Review and standardize performance** evaluation criteria to avoid potential bias.
-	**Use dashboard insights** regularly to track improvements and support evidence-based HR planning.
- **This analysis equips Palmoria Group** with the knowledge to transition toward a more inclusive, fair, and compliant workplace culture.
