# Hospital-Sql-Analytics-Project

This project demonstrates the use of SQL to perform comprehensive analytics on hospital data. It leverages common SQL functions and queries to extract meaningful insights about patients, doctors, departments, and medical expenses across multiple hospitals.

Features / Queries Implemented

1. Total Number of Patients 
or Write an SQL query to find the total number of patients across all 
hospitals. 
SELECT SUM(Patients_Count) AS Total_Patients 
FROM hospital; 
2. Average Number of Doctors per Hospital 
Or Retrieve the average count of doctors available in each hospital. 
SELECT Hospital_Name, AVG(Doctors_Count) AS Avg_Doctors 
FROM hospital 
GROUP BY Hospital_Name; 
3. Top 3 Departments with the Highest Number of Patients 
or Find the top 3 hospital departments that have the highest number of 
patients. 
SELECT Department, SUM(Patients_Count) AS Total_Patients 
FROM hospital 
GROUP BY Department 
ORDER BY Total_Patients DESC 
LIMIT 3; 
4. Hospital with the Maximum Medical Expenses 
or Identify the hospital that recorded the highest medical expenses. 
SELECT Hospital_Name, Medical_Expenses 
FROM hospital 
ORDER BY Medical_Expenses DESC 
LIMIT 1; 
5. Daily Average Medical Expenses 
or Calculate the average medical expenses per day for each hospital. 
SELECT Hospital_Name, 
AVG(Medical_Expenses) AS Daily_Avg_Expenses 
FROM hospital 
GROUP BY Hospital_Name; 
6. Longest Hospital Stay 
or Find the patient with the longest stay by calculating the difference 
between 
Discharge Date and Admission Date. --there is no patient name in the data provided . 
SELECT Hospital_Name, 
Department, 
Patients_Count, 
(Discharge_Date - Admission_Date) AS stay_length_days 
FROM hospital 
ORDER BY stay_length_days DESC 
LIMIT 1; 
7. Total Patients Treated Per City 
or Count the total number of patients treated in each city. 
SELECT Location AS City, SUM(Patients_Count) AS Total_Patients 
FROM hospital 
GROUP BY Location; 
8. Average Length of Stay Per Department 
or Calculate the average number of days patients spend in each department. 
SELECT Department, 
AVG(Discharge_Date - Admission_Date) AS Avg_Stay_Length 
FROM hospital 
GROUP BY Department; 
9. Identify the Department with the Lowest Number of Patients 
or Find the department with the least number of patients. 
SELECT Department, SUM(Patients_Count) AS Total_Patients 
FROM hospital 
GROUP BY Department 
ORDER BY Total_Patients ASC 
LIMIT 1; 
10. Monthly Medical Expenses Report 
or Group the data by month and calculate the total medical ex

Technologies Used

SQL: Core SQL functions including COUNT, AVG, SUM, MAX, MIN, GROUP BY, ORDER BY, and date calculations.

Purpose

This project is ideal for beginners to intermediate SQL users who want to practice real-world hospital data analytics scenarios, including aggregation, ranking, and date-based calculations.
