# Financial Analysis Report

## INTRODUCTION

Welcome to our in-depth Financial Analysis Report, where we meticulously analyze three crucial datasets: employee, salary, and department. In this comprehensive study, we aim to unravel valuable insights by examining the profiles of the top 7 high earners within our organization. These datasets provide a wealth of information, encompassing details such as names, cities, education backgrounds, and designations.

Beyond individual profiles, our report ventures into the geographic landscape of our workforce. By calculating the count of salaries in each city, we seek to provide a nuanced understanding of salary distribution across different locations. Furthermore, a detailed ranking of employee salaries will be presented, unveiling the bottom 10 earners and allowing for a thorough examination of the lower spectrum of our compensation structure.

The analysis extends beyond salary figures; we delve into the dynamics of yearly increments, capturing the top 5 and bottom 5 customers with the highest and lowest increments. To enrich this exploration, we've included essential details such as names, cities, and designations, along with contact information like phone numbers and emails, providing a comprehensive view of the financial landscape within our customer base.

Embark on this insightful journey with us as we decipher intricate patterns within our datasets. This report offers a strategic overview to inform decision-making processes, cultivating a profound understanding of our organizational dynamics based on robust data analysis.

## PROBLEM STATEMENT

Organizational financial analysis is pivotal for informed decision-making and equitable resource allocation. However, challenges in comprehensively understanding key financial metrics hinder our ability to optimize employee compensation and strategic planning. The following questions outline the specific areas of concern that need to be addressed to enhance our financial insights.

Questions:

 1. Display names, cities, education, and designations of the top 7 customers with the highest salaries
 2. Calculate and display the count of salaries by city
 3. Rank the employee's salaries, displaying the bottom 10 salary earners
 4. Identify and display the top 5 and bottom 5 customers with the highest and lowest yearly increments, including cities, phones, and emails.

Addressing these questions will contribute to the development of a unified and streamlined financial analysis system, fostering transparency and data-driven decision-making within the organization.

## SKILLS AND CONCEPTS TO BE DEMOSTRATED

1. Data Retrieval and Display:
   - Demonstrating the ability to retrieve and display specific information from datasets.
   - Implementing queries or commands to showcase names, cities, education, and designations of high earners.
2. Data Aggregation and Calculation:
   - Employing skills to calculate and display the count of salaries by city.
   - Understanding and implementing aggregation functions to derive meaningful insights from the data.
3. Data Ranking and Analysis:
   - Demonstrating proficiency in ranking employee salaries.
   - Analyzing and presenting the bottom 10 salary earners for thorough examination.
4. Trend Analysis and Visualization:
   - Utilizing data analysis techniques to identify trends in yearly increments.
5. Data Interpretation and Decision-Making:
   - Interpreting the extracted data to derive meaningful conclusions.
   - Demonstrating the ability to make informed decisions based on the analyzed financial metrics.
6. System Integration:
   - Integrating data from multiple datasets, including employee, salary, and department data.
   - Ensuring seamless connectivity and interoperability between different parts of the system.
   
Effectively showcasing these skills and concepts will play a pivotal role in improving the organization's data-driven decision-making processes and fostering greater financial transparency.

## ANALYSIS, DISCUSSIONS AND RESULTS

### 1. Display names, cities, education, and designations of the top 7 customers with the highest salaries?

To extract and display information about the top 7 customers with the highest salaries, we utilize SQL with the SELECT function, INNER JOIN function, ORDER BY clause, and the LIMIT function. The syntax for this operation is as follows:

```sql
SELECT Name, Cities, Education, Designation, Salaries FROM Employee
INNER JOIN Department ON Employee.DepID = Department.DepID
INNER JOIN Salary ON Employee.EmpID = Salary.EmpID
ORDER BY Salaries DESC
LIMIT 7;
```

Breaking down the syntax:
- SELECT Name, Cities, Education, Designation, Salaries: Specifies the columns to be retrieved from the combined datasets.
- FROM Employee: Indicates the primary dataset to retrieve information from.
- INNER JOIN Department ON Employee.DepID = Department.DepID: Joins the Employee and Department datasets based on the common Department ID.
- INNER JOIN Salary ON Employee.EmpID = Salary.EmpID: Further joins the Salary dataset based on the common Employee ID.
- ORDER BY Salaries DESC: Orders the result set in descending order based on the Salaries column.
- LIMIT 7: Restricts the output to the top 7 records.
  
In this syntax, the Employee dataset contains information about names and cities, while the Department dataset provides details about education and designation. The Salary dataset contributes information about salaries. The use of INNER JOINs links these datasets based on common identifiers. The result of this query reveals Sarah, located in Pune, with a B.Tech education and ML Engineering designation, as the highest salary earner, with a total salary of 99,46,188.

![](Task5a.png)





























