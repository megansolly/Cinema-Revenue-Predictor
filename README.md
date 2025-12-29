# Cinema-Revenue-Analysis

## Overview
This project analyzes the factors that predict the **profitability of motion pictures**. Using data on approximately 100 movies from 30 directors, the goal is to model **worldwide gross revenue** based on key covariates such as budget, runtime, genre, director, and audience ratings.  

The project emphasizes creating a **simple, interpretable model** suitable for communication to studio executives who may not have statistical expertise. The focus is on providing actionable insights about the relationship between production budget and expected revenue, helping executives make informed funding decisions.

---

## Problem Statement
Studios invest significant amounts in film production. Being able to determine which factors predict a movie’s revenue and whether increased budgets are justified can provide **high-value guidance for decision-making**.  

The key research question:  
> How does production budget, along with other movie characteristics, influence box office revenue, and is additional spending justified?

---

## Dataset Description
The dataset includes approximately 100 movies, with the following variables:

| Variable | Description |
|----------|-------------|
| `movie title` | Name of the movie (index) |
| `production date` | Date of production |
| `genres` | Primary and secondary genres |
| `runtime minutes` | Length of the movie in minutes |
| `director name` | Name of the director |
| `birth year` | Year of the director’s birth |
| `movie averageRating` | Viewer rating (1-10 scale) |
| `budget` | Production budget in dollars |
| `gross` | Worldwide gross revenue in dollars |

---

## Methodology

### 1. Exploratory Data Analysis (EDA)
- Checked univariate distributions for all variables (budget, gross, ratings, runtime).  
- Examined bivariate relationships, especially **budget vs. gross**.  
- Cleaned and transformed variables as needed (e.g., converting runtimes to minutes, handling missing values, encoding genres).  

### 2. Model Selection
- Evaluated multiple linear regression models for simplicity and interpretability.  
- Considered transformations or log-scaling of skewed variables.  
- Checked correlations to avoid multicollinearity and grouped directors where necessary to reduce sparsity.  

### 3. Final Model
- Linear regression model predicting `gross` as a function of:  
  - Budget  
  - Runtime  
  - Movie rating  
  - Genre (primary vs. secondary)  
  - Director groupings  
- Model assumptions verified with residual diagnostics.  

---

## Key Findings
- **Budget** has a positive association with revenue, but the effect varies by genre and director.  
- Certain genres are associated with higher gross on average.  
- Director experience contributes to revenue but requires careful grouping due to limited data per director.  
- Increased spending is **sometimes justified**, but external factors (marketing, seasonality, cast) could refine estimates.  

---
