# Industry & Salary Data Analysis

## Project Overview
Built an end-to-end analysis project focused on Industrial Engineers using public labor market datasets. The project cleans and combines BLS OES 2023 wage/employment data with location-based wage benchmarks pulled from the CareerOneStop Compare Salaries API, then uses visualizations and baseline regression models to explore relationships between pay, industry, ownership, employment size, and geography.

## Key components include:
- Data ingestion and cleaning of large BLS Excel tables
- API-based wage collection by ZIP/location and JSON output generation
- Exploratory analysis + visualizations (industry and state comparisons)
- Baseline modeling with linear regression and logistic regression

## Data Sources
- BLS Occupational Employment and Wage Statistics (OES), 2023
- CareerOneStop API

## Data Cleaning & Feature Engineering
- Standardized column formats and numeric types (wages, employment counts)
- Handled missing values and removed rows that could not be analyzed reliably
- Filtered the dataset to *Industrial Engineers (SOC 17-2112) only
- Created/organized features for analysis such as:
  - NAICS sector/industry identifiers
  - Ownership type
  - Employment size (e.g., TOT_EMP)
  - Wage metrics
  - Geography fields for state-level comparisons
 
## Exploratory Data Analysis 
Explored wage and employment patterns across industries and states, including:
- Which NAICS industries employ the most / least Industrial Engineers
- Which NAICS industries have the highest / lowest average wages
- Which states pay Industrial Engineers the most / least (based on the available wage statistic)

Visualizations include:
- Wage distributions by NAICS sector (boxplots)
- Top industries by employment (bar/pie style summary)
- State-level wage comparisons (map/choropleth-style visualization)

## Model Building
To quantify relationships between pay and industry/employment factors, I built two baseline models:

### 1) Linear Regression (Salary)
Modeled Industrial Engineer salary as a function of:
- NAICS sector/industry
- Ownership type
- Employment size

Categorical features were converted to dummy variables. Model fit was evaluated using standard regression metrics.

### 2) Logistic Regression (Top 10% Pay Classification)
Created a binary label indicating whether a record is in the top 10% of pay within its industry group, then used logistic regression to test whether:
- NAICS sector/industry and employment size are associated with being in that top-pay bucket.





