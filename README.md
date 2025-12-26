# EU-voter-research
### An analysis of voter satisfaction and its effect on turnout in the 2024 European Parliament elections using 2024 Eurobarometer survey data

This research project was completed as coursework for my PS1702 - Visualizing and Understanding Social Data course. I used a .csv file from the Eurobarometer public survey data, cleaning it and narrowing it down to a handful of variables that were pertinent to my research. I used R Markdown along with the ggplot2 package to visualize and analyze the data, asking the question: **Does an EU resident's satisfaction with how democracy works under the EU have any effect on their likelihood of voting?** 

Among my analysis methods, I selected control variables and created a multivariate regression model to determine the statistical significance of my explanatory variable (voter satisfaction), using a coefficient plot to visualize predictors of voter turnout. I also examined the main relationship via a line plot, introducing third variables to explore any possible confounders. 

## Methods

Data sourced from Eurobarometer 2024 survey "Trust in National and International Institutions" (https://www.gesis.org/en/eurobarometer-data-service/overview/eb-trends-trend-files/list-of-trends/trust-in-institutions)

Cleaned and visualized using R Markdown with ggplot2, dplyr, and broom packages

Focused on 2024 survey data from all EU member states 

## Key Questions

Does voter satisfaction have an affect on likelihood of voting?

Are there any confounders? 

Are there any statistically significant predictors that have a stronger effect on turnout?

Do any relationships appear when aggregating the data for country-level analysis?

## Results & Findings

The analysis reveals that a statistically significant and positive relationship does exist between voter satisfaction and likelihood of voting, confirming my hypothesis. When accounting for third variables, I found that unemployed people, females, those with lower perceived social and economic status, and those who live in rural areas are all less likely to vote, but the relationship between satisfaction and turnout still exists in these groups.

The strongest negative predictor of turnout was unemployment, with the unemployment regression coefficient lying at roughly -0.11. The strongest positive predictor was satisfaction with democracy; the regression coefficient for this variable was 0.05 or so. 

One interesting exception to the rule appeared: The group of respondents who said that their country's EU membership was neither a good or bad thing showed no relationship between satisfaction and voting. This makes sense when we understand that those indifferent to the EU are most likely not concerned with elections at all despite how satisfied they may be with the democracy of the institution.

When aggregating the data at a country level, I find that the relationship is still roughly present when observing a heatmap of satisfaction vs. turnout across all countries, but other confounders make it unreliable. For example, Belgium and Luxembourg have consistently high turnouts across all satisfaction levels because of their compulsory voting laws. 

Overall, findings show a strong correlational trend between satisfaciton and turnout, but also trends among other variables and turnout. Soemone's decision to vote can be influenced by many things and it is difficult to pinpoint any one main reason. However, we can observe factors that might influence one's decision and draw generalized conclusions on voter behavior as a result.

## Technologies

R, R Markdown

broom, ggplot2, dplyr, socviz

Eurobarometer data (2024)

## Reproducibility

To reproduce this analysis, open `visualizationCode.Rmd` in RStudio and ensure the following packages are installed:
`broom`, `ggplot2`, `dplyr`, and `socviz`.

Data sources can be accessed through ZA8868_v1-0-0.csv and ZA8868_clean.csv via the main branch

## Sample Plot from Research

Below is a sample plot from my research:


![Coefficient Predictors of Change in EU Parliamentary Election Turnout Using 95% Confidence Intervals](https://github.com/DanielYoho/EU-voter-research/blob/35bbdde11a86378e9a569c9e77ccf4c35401efaa/turnoutPredictors.png)

![View the full PDF report here](https://github.com/DanielYoho/EU-voter-research/blob/35bbdde11a86378e9a569c9e77ccf4c35401efaa/Final%20Report.pdf)

## My Information

**Author:** Daniel Yoho 

**Affiliation:** Computational Social Science Student, University of Pittsburgh  

**Date:** December 2025
