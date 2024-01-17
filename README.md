# 2024 Layoff Analysis

## Introduction
Fueled by economic uncertainty, businesses worldwide are facing difficult times, leading to significant layoffs. The tech sector alone has lost over 257,000 jobs, dwarfing pandemic-era losses. This summary examines the affected industries, geographic trends, and strategic considerations, offering a glimpse into the changing employment landscape.

## Overview
This dataset contains 2,738 rows and 12 columns, and was scraped from [Layoffs.fyi](https://layoffs.fyi/). Original dataset can be found on [Kaggle](https://www.kaggle.com/datasets/theakhilb/layoffs-data-2022/data).

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

### US Total Layoffs: 251,977, US Total Funds Raise: 806 billion USD
![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/layoffs_by_country.png)

### SF: 126,000, New York City: 24,000, Seattle: 36,000, 10,500, Los Angeles: 7,000
![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/top_locations_us.png)

### Amazon: 18,000, Google: 12,000, Meta: 11,000
![](https://github.com/MaxBoonjindasup/2024_layoffs_analysis/blob/main/top_companies_us.png)

## Predicting When Layoffs Would Occur : Random Forest Model

### Features: Company, Location_HQ, Industry, Layoffs, Funds_Raised, Stage, and Country
### Target: Month
### Optimization: Cross Validation, GridSearchCV

| Metric                    | Value |
|---------------------------|-------|
| R-squared                 | 1.000 |
| Mean Absolute Error       | 0.000 |
| Mean Squared Error        | 0.000 |
| Root Mean Squared Error   | 0.000 |
