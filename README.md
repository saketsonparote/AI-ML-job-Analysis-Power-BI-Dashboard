🤖 AI & ML Jobs Market Analysis - Power BI Dashboard

📌 Overview

The AI & ML Jobs Market Analysis project is an interactive Power BI dashboard designed to explore global trends in Artificial Intelligence and Machine Learning job opportunities. It provides insights into job distribution, salary trends, company hiring patterns, geographic demand, and skill requirements.

This project helps job seekers, recruiters, and data enthusiasts understand the evolving AI & ML job market and make data-driven decisions.

🎯 Objectives

Analyze the distribution of AI & ML jobs across companies and roles.
Understand salary trends by experience level, job title, and location.
Identify the most in-demand skills in the AI & ML domain.
Examine the prevalence of remote, hybrid, and on-site work.
Provide geographic insights into job opportunities and compensation.
Enable interactive exploration through dynamic dashboards.

📊 Dashboard Pages

1️⃣ Overview

Total Jobs
Average Salary
Median Salary
Remote Job Percentage
Job Trends by Month
Experience Level Distribution

2️⃣ Company and Role Insight

Jobs per company by experience level.
Job titles vs. remote work type.
Company ratings and comparisons.
Remote ratio vs. salary by job title.

3️⃣ Location Insight

Job distribution by country and city.
Geographic visualization using maps.
Average salary by region and experience level.
Regional filtering for targeted analysis.

4️⃣ Skill and Hiring Insight

Skill demand by experience level.
Average salary by job title and seniority.
Remote work trends by skill.
Experience-wise skill distribution.
Total skill usage count.

🗂️ Dataset Description

The project follows a star schema data model for efficient analysis.

📁 Tables Used
Table Name	Description
Jobs.csv	Contains job postings, salaries, experience levels, remote types, and job titles.
Companies.csv	Includes company details such as name and ratings.
Locations.csv	Provides geographic information including city, country, and region.
Skills.csv	Lists all relevant AI & ML skills.
Job_Skills.csv	Bridge table mapping jobs to required skills.
⭐ Data Model
                Dim_Companies
                     |
Dim_Locations — Fact_Jobs — Bridge_Job_Skills — Dim_Skills

📈 Key Metrics & DAX Measures

-- Total number of job postings
Total Jobs = COUNTROWS(Jobs)

-- Average salary
Average Salary = AVERAGE(Jobs[Salary])

-- Median salary
Median Salary = MEDIAN(Jobs[Salary])

-- Remote job percentage
Remote Job % =
DIVIDE(
    CALCULATE(COUNTROWS(Jobs), Jobs[IsRemote] = "Remote"),
    [Total Jobs],
    0
)

-- Average salary by experience
Average Salary by Exp =
AVERAGEX(
    VALUES(Jobs[Experience_Level]),
    [Average Salary]
)

🔍 Key Insights

📊 Mid-level roles constitute the largest share of job postings.
💰 Senior positions command the highest salaries, reaching up to $132K.
🌎 North America, particularly San Francisco, offers the highest average salaries.
🏢 Leading employers include OpenAI, Google DeepMind, NVIDIA, Hugging Face, and DataCamp.
🧠 Python, Machine Learning, Deep Learning, and Cloud Computing are the most in-demand skills.
🏠 Hybrid and mostly remote roles are more prevalent than fully remote positions.

🎨 Features

✅ Interactive and user-friendly dashboards.
✅ Clean and consistent visual theme.
✅ Star schema data modeling.
✅ Advanced DAX calculations.
✅ Geographic analysis with map visuals.
✅ Skill demand and hiring insights.
✅ Slicers for region, experience level, and time.
✅ Drill-down and cross-filtering capabilities.

🛠️ Tools & Technologies

Tool	Purpose
Power BI Desktop	Data visualization and dashboard creation
DAX (Data Analysis Expressions)	Calculated measures and KPIs
Power Query	Data cleaning and transformation
CSV Files	Data storage and integration
GitHub	Version control and project sharing


🏆 Project Highlights

✔️ Real-world business problem.
✔️ End-to-end data analysis workflow.
✔️ Professional dashboard design.
✔️ Insightful storytelling.
✔️ Portfolio-ready for data analyst roles.

🔮 Future Enhancements

📅 Add a date dimension for advanced time intelligence (YTD, MTD, YoY).
🔐 Implement Row-Level Security (RLS).
📱 Create a mobile-optimized layout.
📈 Include forecasting for future job trends.
🌐 Publish the dashboard to Power BI Service for live access.

📜 License

This project is licensed under the MIT License. You are free to use and modify it with proper attribution.

⭐ If you found this project helpful, consider giving it a star on GitHub!