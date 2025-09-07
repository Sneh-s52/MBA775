# Board Governance and Financial Leverage Analysis

This project examines how Apple Inc.’s board composition influences its capital structure decisions, focusing on the debt-to-equity ratio and leverage ratio. It integrates corporate governance metrics with financial performance data, employs robust regression techniques, and visualizes marginal and partial effects.

## Project Overview

1. **Data Preparation**  
   - Merge annual financial statements with board governance metrics (e.g., total directors, independence ratio, gender diversity, expertise breadth, meeting intensity, average tenure).  
   - Clean and standardize variables; handle missing or infinite values.

2. **Exploratory Data Analysis & Sanity Checks**  
   - Time-series visualization of governance trends (diversity, independence, tenure).  
   - Distributional checks with aesthetic histograms.  
   - Correlation matrix heatmap to explore relationships among governance and financial metrics.  
   - VIF analysis to detect multicollinearity among candidate predictors.

3. **Regression Modeling**  
   - OLS with heteroskedasticity-robust (HC3) standard errors regressing log(debt_equity) on board variables.  
   - Robustness check using leverage_ratio as an alternative dependent variable.  
   - Interpretation of coefficients and overall model fit.

4. **Visualization of Effects**  
   - Partial regression plots to assess each board variable’s net effect.  
   - Marginal effects plots (with 95% confidence intervals) illustrating predicted changes in debt_equity across observed ranges of key predictors.

## Key Findings

- **Gender Diversity** exhibits the strongest, statistically significant positive association with leverage (p < 0.05), robust across both debt_equity and leverage_ratio models.  
- **Average Tenure** shows a moderate positive effect (p < 0.10), suggesting that board experience correlates with greater debt usage.  
- **Board Independence** and **Size** have no significant direct impact once diversity and tenure are controlled.  
- **CEO Duality** is omitted because Apple maintains separate CEO and Chair roles (all zeros), reflecting its governance principle of independent leadership.
