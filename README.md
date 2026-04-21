# Football Transfer Market Value Prediction

## Overview
This project builds a statistical model to estimate football players’ market values using performance metrics, demographic features, and contextual football data. The goal is to understand which factors drive player valuation in professional football using a linear regression framework.

## Data Sources
- FIFA 22 player dataset (`players_22.csv`)
- Football statistics dataset (2021–2022 season)
- Club ranking dataset
- FIFA country ranking dataset

Data preprocessing includes:
- Standardization of player names across datasets
- Mapping of clubs, leagues, and national teams to numeric rankings
- Feature engineering (position encoding, contract duration, etc.)
- Data cleaning and filtering (minutes played, value thresholds)

## Methodology
1. Data preprocessing and feature engineering in R
2. Merging multiple football datasets into a unified dataset
3. Encoding categorical variables into numerical form
4. Exploratory correlation analysis
5. Linear regression model:
   - Ordinary Least Squares (OLS)
   - Full multivariate regression using all predictors

## Model Evaluation
- Residual diagnostics (QQ plots, variance checks)
- Correlation analysis between predictors and target variable
- Visual comparison of fitted vs actual values
- Error analysis for model assumptions

## Prediction Examples
The model is used to estimate market values for:
- Elite players (e.g., Haaland-type profiles)
- Young prospects (e.g., Lamine Yamal-type profiles)
- Hypothetical players with custom attributes

Prediction outputs include:
- Point estimates
- Confidence intervals (95%)
- Prediction intervals (95%)

## Key Findings
- Player performance metrics (goals, assists, minutes played) strongly influence valuation
- Age and wage show significant correlation with market value
- Club and league context introduce meaningful valuation effects
- Linear models capture general trends but miss nonlinear scouting factors

## Limitations
- Linear model assumption may oversimplify real transfer market dynamics
- Missing hidden variables (scouting reports, injuries, reputation effects)
- Data quality depends on external datasets and name-matching accuracy

## How to Run
1. Install R dependencies:
```r
install.packages(c("dplyr", "stringdist", "rvest", "readr", "stringr", "stringi"))
