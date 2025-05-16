# Data Summary Report

## 1. Dataset Description

The dataset under analysis consists of monthly population data from January 2010 to December 2020 (Republic of China years 99 to 109), covering a total of 132 observations. Each observation represents population figures for a given month and year, including the total population and disaggregated counts for 21 age groups ranging from 0–4 years to 100 years and above. According to the codebook ("Population Analysis Codebook.markdown"), this dataset is suitable for evaluating demographic trends, analyzing age structure shifts, and identifying population growth patterns over the 11-year span.

All variables are integers, and there are no missing values according to the univariate summary file ("population_summary.json"). The variables of interest include two time variables (`年度`, `月份`), the overall population (`總計`), and population counts across age categories such as `年齡0-4歲人數`, `年齡25-29歲人數`, `年齡85-89歲人數`, and so on.

## 2. Descriptive Statistics

From the univariate summary, the average total population during the sample period is approximately 14,277 individuals, with a range from 13,575 to 15,230. The age group 30–34 years (`年齡30-34歲人數`) has one of the largest average populations (~1,117), while the 100+ age group (`年齡100歲人數以上`) represents the smallest, averaging just under 4 individuals. Standard deviations and quantiles reported in the summary JSON provide further insight into the distributional properties of each age group.

## 3. Multivariate Analysis Summary

To explore relationships between variables, several multivariate analyses were performed and saved as structured JSON outputs in the `multivariable_json_summary/` directory.

### 3.1 Correlation Matrix

A correlation matrix (`01_correlation_matrix_total_age.json`) reveals that total population is strongly and positively correlated with all major age groups, particularly those in the working-age brackets (25–49 years). This indicates that changes in the overall population are largely driven by fluctuations in the central age structure.

### 3.2 Linear Regression of Age Groups on Year

A set of simple linear regressions was estimated for each age group as a dependent variable regressed on calendar year (`西元年`). The results are stored in `02_regression_age_vs_year.json`. The age groups from 65 years and above generally exhibit positive slopes, suggesting growth in elderly population over time, while some younger cohorts such as 0–4 or 10–14 display slightly negative slopes, reflecting a potential decline in birth rates.

### 3.3 Total Population as a Function of Demographic Subgroups

A multivariate regression model, stored in `03_regression_total_vs_age_groups.json`, regresses total population on aggregated counts of working-age (`青壯年`, age 20–64) and elderly (`老年`, age 65+) individuals. The model indicates that both groups contribute significantly to changes in the total population, with a stronger coefficient on the working-age population.

### 3.4 Principal Component Analysis (PCA)

To reduce dimensionality and analyze structural variation, a PCA was conducted on standardized age group counts (`04_pca_age_structure.json`). The first few components explain the majority of variance, highlighting dominant patterns such as aging trends and shifts in younger demographics.

### 3.5 Age Group Proportional Trends

Finally, we examined proportional changes of each age group relative to the total population over time. The summary in `05_age_group_proportion_trends.json` shows increasing shares for elderly groups and declining proportions for younger groups, consistent with broader aging demographic trends.

## 4. Conclusion

This dataset provides a rich basis for studying demographic changes in a time-series context. The combination of univariate and multivariate summaries suggests a clear aging trend, stable working-age population, and moderate decline in youth cohorts. For further research or policy analysis, this data can support age-structured economic modeling and planning.

## References

- Codebook: *Population Analysis Codebook.markdown*
- Univariate Summary: *population_summary.json*
- Multivariate Summaries: Files in *multivariable_json_summary/* directory