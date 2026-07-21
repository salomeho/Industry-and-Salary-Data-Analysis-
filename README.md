# Industry & Salary Data Analysis

## Business Question
For an Industrial Engineer, does industry or geographic location have more influence on maximizing salary, and which sectors offer the best odds of top-tier pay?

## Project Overview
This project analyzes wage and employment patterns for Industrial Engineers across U.S. industries and states. It combines public labor-market data from the Bureau of Labor Statistics with location-based salary data collected through the CareerOneStop API. The project includes data collection, cleaning, exploratory analysis, interactive visualizations, and baseline regression models.

## Data Sources
- BLS Occupational Employment and Wage Statistics, 2023
  - Industry-level employment and wage estimates
  - Ownership-level occupational data
  - Filtered to Industrial Engineers, SOC 17-2112
- BLS Industrial Engineers occupational webpage
  - Tables extracted using Requests and BeautifulSoup
- CareerOneStop Compare Salaries API
  - Annual wage percentiles for selected locations
  - API responses processed and stored as JSON

## Tools Used
Python, Pandas, Requests, BeautifulSoup, Plotly, scikit-learn, Matplotlib, Tableau

## Key Findings
- Web Search Portals had the highest reported average Industrial Engineer salary at approximately $200,000 per year.
- Radio and Television Broadcasting had the lowest reported average salary at approximately $60,000 per year.
- Architectural and Engineering Services employed approximately 23,000 Industrial Engineers, the largest employment total in the dataset.
- Footwear Manufacturing employed approximately 30 Industrial Engineers, the smallest reported total.
- Alaska had the highest state median salary at approximately $140,000.
- North Dakota had the lowest state median salary at approximately $80,000.

## Visualizations 
- Industrial Engineer wage distribution across NAICS industries
- Top 10 industries by Industrial Engineer employment
- State-level choropleth of median annual wages
- Actual versus predicted salaries from linear regression
- Logistic-regression confusion matrix

## Interactive Dashboard
The Tableau dashboard contains three views:
- Salary by Industry — ranked bar chart of avg IE salary across 143 NAICS industries
- Salary by State — choropleth map of median IE salary across all 50 states
- Employment vs Salary — scatter plot showing which industries hire the most IEs and at what pay

View notebook on Tableau Public:
https://public.tableau.com/views/IESalaryAnalysis/IndustrialEngineerSalaryAnalysis2023?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

View notebook on Google Colab:
https://colab.research.google.com/drive/1ooptts5-vuDlvjL_keIQg2XaSk1DB2gZ

Watch the Project Walkthrough:
https://www.youtube.com/watch?v=E3se3lQlEdA

## Methodology
Three public data sources were used: downloaded BLS OES 2023 employment and wage tables, a BLS Industrial Engineers occupation profile page, and CareerOneStop API results collected by ZIP code for geographic wage comparisons.

The BLS industry data was filtered to Industrial Engineers (SOC 17-2112). Wage and employment fields were converted to numeric formats, and records missing values required for each analysis were removed. CareerOneStop API results were processed, deduplicated, and filtered to annual state-level wage records.

The analysis examined five areas: the highest- and lowest-paying industries, the industries employing the most and fewest Industrial Engineers, the states with the highest and lowest median wages, a baseline linear regression relating salary to industry, ownership type, and employment size, and a logistic regression exploring whether industry and employment size could distinguish relatively high-paying observations.

Five supporting visualizations were produced: three exploratory (an industry wage-distribution boxplot, a top-employment industries chart, and a state choropleth of median wages) and two model-diagnostic plots (actual-vs-predicted salary from the linear regression, and a confusion matrix from the logistic regression).

## Limitations
The datasets contain aggregated labor-market estimates rather than individual employee records. Important salary factors such as experience, education, job level, employer, and cost of living are not included.

The regression models are exploratory baselines. The linear regression does not capture most factors affecting salary, while the logistic regression should not be interpreted as a precise prediction tool. Additionally, the state analysis uses median wage estimates, so individual salaries may differ substantially.
