# Company Attendance Report Dashboard

Project: Company Attendance Report Dashboard
Description: Interactive Power BI dashboard that visualizes employee attendance, overtime hours, permission time, and salary metrics. Includes KPIs, monthly comparisons, OT trend analysis, and detailed employee profiles.

# Files

Dataset (XLSX): /mnt/data/Attendance_Report_365Days_2025.xlsx
Dashboard preview image: /mnt/data/Screenshot 2025-11-21 113841.png
When uploading to GitHub, move these into folders like:
data/Attendance_Report_365Days_2025.xlsx
images/attendance_dashboard.png

# How to open & reproduce (Power BI)

Open Power BI Desktop
Get Data → Excel → select dataset
Clean in Power Query:
Promote Headers
Change data types
Create Month, Status, OT buckets

# Create visuals:

Employee KPIs
OT By Day (Line Chart)
Attendance Donut Chart
Employee Info Cards
Add filters: Name, Month
Format with theme, borders, and conditional colors

# Power Query notes

Common M-steps used:
Promote Headers
Trim / Clean Text
Group By for summaries
Create custom date columns
Remove null/blank entries

# DAX Measures
Total OT Hours = SUM('Attendance'[OT_Hour])
Permission Time Total = SUM('Attendance'[Permission_Time])
Attendance % = DIVIDE(COUNTROWS(FILTER('Attendance','Attendance'[Status]="Present")), COUNTROWS('Attendance'))
OT Allowance = [Total OT Hours] * 125

# Key Insights

Highest OT contributing employees
Attendance consistency pattern
Permission-time trend
Salary vs OT Allowance
Monthly attendance distribution

# Repo Structure

/ (root)
├─ README.md
├─ data/
│  └─ Attendance_Report_365Days_2025.xlsx
├─ images/
│  └─ attendance_dashboard.png
└─ pbix/
   └─ Attendance_Report.pbix

# License

MIT License — open for use and modification.
