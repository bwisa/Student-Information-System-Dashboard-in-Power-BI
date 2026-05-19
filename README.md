# Student-Information-System-Dashboard-in-Power-BI
An interactive Realtime KPI-based dashboard developed to track and analyze student academic performance and attendance trends.

## Building a complete automated dashboard for a student academic system 
This ensures that as grades, attendance, or enrollment data are updated in your SQL database, the Power BI dashboard reflects those changes automatically without manual intervention.

## The Architecture of an Automated DashboardData Source (SQL): 
- A relational database (MySQL or SQL Server) where student information is stored in normalized tables (e.g., Students, Courses, Grades, Attendance).
- Transformation (SQL Views/Queries): Instead of loading raw tables, I created SQL views or queries that pre-calculate metrics like GPA, pass rates, or attendance percentages.
## Visualization (Power BI)
- Connect Power BI to the SQL database. Using the "Scheduled Refresh" feature to keep the data current.

## Key Performance Metrics (KPIs) to TrackAn effective academic dashboard typically focuses on three main areas:
- Category Metric Examples Decision Supported Academics 
- Average GPA by Grade, Subject Pass Rates, Top/Bottom, 10th Percentile, Curriculum adjustments or targeted tutoring. Attendance: Daily Attendance Trends, Chronic Absenteeism, Rates Identifying students at risk of dropping out. 
- Admissions Enrollment Growth (MoM), Conversion Rates from Inquiry to Admission Budgeting, staffing, and marketing focus.

# Implementation - Steps
### Step 1: SQL Data Preparation - Used SQL window functions or aggregations to prepare your data. 

For example, to rank students by performance within their province:SQLSELECT 
    Student_Name, 
    Subject, 
    Score, 
    RANK() OVER(PARTITION BY Province ORDER BY Score DESC) as Performance_Rank
FROM Student_Scores;

### Step 2: Power BI Visualization
- Filters/Slicers:
Used slicers for "Term," "Subject," or "Grade Level" to allow users to drill down into specific data points.

- Conditional Formatting: Use red/green color-coding for pass/fail rates to instantly alert school leadership to issues.
- 
### Executive View: 
Create a "Super Admin" dashboard that shows high-level trends across the entire institution.

### ...
