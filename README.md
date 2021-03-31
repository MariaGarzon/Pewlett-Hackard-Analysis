# Pewlett Hackard Analysis

## Overview

This analysis was performed to assess the aging worforce at Pewlett Hackard.

## Project Summary

First, the number of people who will be eligible for retirement in the next few years at Pewlett Hackard was calculated. This will assists the HR Department to determine:

    a) number of retirement packages to be delivered and 
    b) number of positions that will need to be filled in the near future 

Then, the analysis was used to determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program.

## Resources

- Data Source: 6 csv files where Pewlett Hackard currently stores employee and department information which were then updated to SQL.
- Tools: The data was then grouped into tables using postgresql and pgadmin.

The entity relationship of the databases is as follows:

![Employee db](https://github.com/MariaGarzon/Pewlett-Hackard-Analysis/blob/837707dc6c0450dcc1cf9d562363a169444dced5/images/EmployeeDB.png)

## Results

### The Number of Retiring Employees by Title

- A retirement titles table was created: - The data was organized by employee number, first name, last name, salary, and title. - Retirement eligibility was determined to be anyone born between 1952 and 1955.

- We had to consider the fact that over the years workers titles changed. These duplicates were removed using the DISTINCT ON statement to access only the most recent title of each employee.

- A unique titles table was created that contained the employee number, first and last name, and most recent title.

- A retiring titles table was created that contained the number of titles filled by employees who are retiring. It was evident that most roles that that will need to be filled in the near future are senior positions. For instance, only two manager positions will need to be filled.

### The Employees Eligible for the Mentorship Program

- The same approach was applied to create the mentorship-eligibility table that holds the current employees who were born between January 1, 1965 and December 31, 1965.The only thing changed were the dates because we were not looking for retirement aged employees.

## Summary

- According to the table below, 90,398 roles will have to be filled in the next few years. The HR department should intially focus on Senior Enginner and Senior Staff roles as 29,414 and 28,254 positions will need to be filled, respectively. 
- Additionally, 14,222 Engineer positions, 12,243 Staff positions, 4,502 Technique Leader positions, 1,761 Assistant Engineer positions and 2 Manager positions will need to be filled in the next few years.

![Unique_Titles_Retiring](https://github.com/MariaGarzon/Pewlett-Hackard-Analysis/blob/837707dc6c0450dcc1cf9d562363a169444dced5/images/unique_Titles_Retiring.png)

- It is important to note there are not enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees. Given the mentorship criteria given by HR, a query helped determine there are only 1,941 employees who are eligible. 
- It is also concerning that only 456 Senior Staff, and 380 Senior Engineers will be avaiable for 57,668 senior roles that will require training. This means each person would have to train approximately 70 people. Additionally, there are no managers available to provide training for the position.
