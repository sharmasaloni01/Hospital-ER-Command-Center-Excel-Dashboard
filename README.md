# Project overview
This dashboard analyses hospital emergency room (ER) visits for 2023 and 2024. It is designed to answer three questions:
1. When do patients arrive, and when is the ER busiest?
2. How long do patients wait compared with a 30-minute target?
3. Does a longer wait reduce patient satisfaction?
Dashboard features
• Year and Month slicers that filter every KPI and chart
• KPI cards: total patients, average wait time (minutes), average satisfaction score, admission rate
• Patients by time of day (3-hour blocks)
• Patient journey funnel: arrived, seen within target, satisfied
• Wait time vs target gauge
• Satisfaction by waiting-time band (does waiting hurt satisfaction?)
• Department referral (excluding none), age group and gender breakdowns
• Dark theme with a consistent teal and amber colour palette

# Key insights
Numbers are from the dashboard with no filter selected.
Metric Result
Total patients 9,216
Average wait time 35.3 minutes, above the 30-minute target
Average satisfaction score 4.99 out of 10
Admission rate 50% (admitted / total)
Gender split 49% female, 51% male
Age groups 15-29 is the largest group (about 1,800); 75+ is the smallest (about 560)
Department referral General Practice is the most common, followed by Orthopedics
Busiest time of day (21-24)
# Data
• Source: -[Hospital ER Data (Excel File)](Hospital_ER_dashboard.xlsx) - Anonymous sample data included in this repository.
-. This is a public / sample dataset and does not contain real patient information. Names and IDs in the shared file are anonymised.
• Main fields: admission date and time, age, gender, race, department referral, admission flag,satisfaction score, wait time.
• Records: 9,216 | Period: 2023 to 2024
• Satisfaction scores are missing for some visits, so the average uses the recorded scores only.
# How I built it:-
1. Organized the raw data as an Excel Table and cleaned inconsistent values (gender was entered as M, F, Male and Female).
2. Added helper columns with formulas: Year,Month,Weekday,TimeBlock,AgeGroup,WaitBand WithinTarget,AdmittedFlag ,SatisfiedFlag ,GenderClean
3. Built PivotTables for each metric: KPIs, time of day, wait band, department, age group and gender.
4. Linked the KPI cards to the pivots with GETPIVOTDATA so they update with the slicers.
5. Created PivotCharts, plus small helper tables for the gauge and the funnel.
6. Designed the layout on a cell grid with shapes, a custom colour palette and styled slicers.
# Tools and skills
Microsoft Excel: Tables, PivotTables, PivotCharts, Slicers, GETPIVOTDATA, IFS / TEXT / HOUR
formulas, dashboard layout and visual design.
# What I learned
• Why helper columns are needed and how to group raw data for analysis
• How to connect slicers to many PivotTables and charts
• How to keep numbers correct when filters change (GETPIVOTDATA)
• How to design a clean, readable dashboard with a consistent colour palette
• How to document a project so that others can understand it
# Challenges
• Making one set of slicers control every chart
• Cleaning inconsistent text values before analysis
• Placing shapes and charts accurately on a grid
• Choosing charts that stay readable inside small panels
# Limitations and next steps
• The 30-minute wait target and the satisfaction threshold are assumptions I set; a real hospital would
# Use its own targets.
• The Month slicer shows months in alphabetical order; I plan to add a month sort column.
• Some charts need more axis labels (the time-of-day and wait-time charts).
• The wait-time line chart shows no clear straight-line relationship with satisfaction, so I would need deeper analysis before drawing a conclusion.
• Next, I plan to rebuild the same analysis in Power BI and SQL.
# Credit
Inspired by a YouTube tutorial on a hospital ER dashboard. I redesigned the layout, theme, charts and analysis questions.
# Files
File Description
Hospital_ER_dashboard.xlsx The Excel workbook (anonymised data)
Dashboard.png Dashboard screenshot
Author
Saloni Kumari | Aspiring Data Analyst
LinkedIn: [www.linkedin.com/in/saloni-kumari-557139260]
