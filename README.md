# 2024 Layoff Analysis

## Introduction
Fueled by economic uncertainty, businesses worldwide are facing difficult times, leading to significant layoffs. The tech sector alone has lost over 257,000 jobs, dwarfing pandemic-era losses. This summary examines the affected industries, geographic trends, and strategic considerations, offering a glimpse into the changing employment landscape.

## Overview
This dataset contains 2,738 rows and 12 columns, and was scraped from [Layoffs.fyi](https://layoffs.fyi/).

| Field                        | Description                                      |
|------------------------------|--------------------------------------------------|
| Company                      | Name of the company                              |
| Location                     | Location of the company                          |
| Industry                     | Type of industry                                 |
| Layoffs                      | Total layoff count                               |
| Percentage                   | Percentage of layoff                             |
| Date                         | Date of layoff                                   |
| Source                       | Source of data                                   |
| Funds_Raised                 | Total funds raised                               |
| Stage                        | Stage of the company                             |
| Date_Added                   | Date added in database                           |
| Country                      | Country of company location                      |
| List_of_Employees_Laid_Off   | Link to Google Docs of employee list             |

## EDA - Cleaning
1. Inspected for and removed missing data: 1,164 (35.5%)
2. Checked for duplicate data: 0%
3. Removed outliers: 147 (10.6%)

## EDA - Visualizations

![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/layoffs_over_time_us.png)

| Month-Year       | Total Layoffs in the Month |
|------------------|----------------------------|
| April 2020       | 17,708                     |
| May 2020         | 13,790                     |
| November 2022    | 43,185                     |
| January 2023     | 57,745                     |
| February 2023    | 14,717                     |

![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/layoffs_by_country.png)

| Metric                    | Amount            |
|---------------------------|-------------------|
| Total US Layoffs          | 251,977           |
| Total US Funds Raised     | $806 billion      |

![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/top_industries_us.png)

| Industry        | # of Layoffs |
|-----------------|--------------------------|
| Consumer        | 38,487                   |
| Retail          | 32,231                   |
| Transportation  | 23,062                   |
| Other           | 22,332                   |
| Finance         | 15,582                   |

![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/top_locations_us.png)

| City              | # of Layoffs |
|-------------------|--------------|
| San Francisco     | 126,000      |
| New York City     | 24,000       |
| Seattle           | 36,000       |
| Boston            | 10,500       |
| Los Angeles       | 7,000        |

![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/top_companies_us.png)

| Company | # of Layoffs |
|---------|--------------|
| Amazon  | 18,000       |
| Google  | 12,000       |
| Meta    | 11,000       |

## Predicting When Layoffs Would Occur : Random Forest Model

#### Features: Company, Location_HQ, Industry, Layoffs, Funds_Raised, Stage, and Country
#### Target: Month
#### Optimization: Cross Validation, GridSearchCV

| Metric                    | Value |
|---------------------------|-------|
| R-squared                 | 1.000 |
| Mean Absolute Error       | 0.000 |
| Mean Squared Error        | 0.000 |
| Root Mean Squared Error   | 0.000 |
