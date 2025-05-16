# Codebook for Population Analysis Dataset

## Dataset Description
This dataset contains monthly population data for a region from January 2010 (Republic of China year 99) to December 2020 (year 109). It includes the total population and population counts for 21 age groups, ranging from 0-4 years to 100+ years. The data is suitable for analyzing demographic trends, age distribution changes, and population growth over time. The source is not specified, but it appears to be official demographic statistics, likely from a government or statistical agency.

## Dimensions
- **Rows**: 132 (one per month from January 2010 to December 2020)
- **Columns**: 24 (2 for time, 1 for total population, 21 for age groups)

## Variable Information
| Variable Name (Chinese) | Variable Name (English) | Description | Data Type | Range | Mean (Approx.) |
|-------------------------|-------------------------|-------------|-----------|-------|----------------|
| 年度 | Year | Year in Republic of China era (add 1911 to convert to Gregorian, e.g., 99 = 2010) | Integer | 99–109 | 104 |
| 月份 | Month | Month of the year | Integer | 1–12 | 6.5 |
| 總計 | Total | Total population across all age groups | Integer | 13,575–15,230 | 14,273 |
| 年齡0-4歲人數 | Age 0-4 | Population aged 0-4 years | Integer | 536–623 | 582 |
| 年齡5-9歲人數 | Age 5-9 | Population aged 5-9 years | Integer | 340–628 | 471 |
| 年齡10-14歲人數 | Age 10-14 | Population aged 10-14 years | Integer | 404–658 | 529 |
| 年齡15-19歲人數 | Age 15-19 | Population aged 15-19 years | Integer | 676–841 | 756 |
| 年齡20-24歲人數 | Age 20-24 | Population aged 20-24 years | Integer | 822–1,196 | 990 |
| 年齡25-29歲人數 | Age 25-29 | Population aged 25-29 years | Integer | 955–1,204 | 1,025 |
| 年齡30-34歲人數 | Age 30-34 | Population aged 30-34 years | Integer | 967–1,234 | 1,117 |
| 年齡35-39歲人數 | Age 35-39 | Population aged 35-39 years | Integer | 1,050–1,264 | 1,171 |
| 年齡40-44歲人數 | Age 40-44 | Population aged 40-44 years | Integer | 1,053–1,226 | 1,102 |
| 年齡45-49歲人數 | Age 45-49 | Population aged 45-49 years | Integer | 1,040–1,206 | 1,124 |
| 年齡50-54歲人數 | Age 50-54 | Population aged 50-54 years | Integer | 938–1,272 | 1,093 |
| 年齡55-59歲人數 | Age 55-59 | Population aged 55-59 years | Integer | 797–1,156 | 964 |
| 年齡60-64歲人數 | Age 60-64 | Population aged 60-64 years | Integer | 538–1,001 | 762 |
| 年齡65-69歲人數 | Age 65-69 | Population aged 65-69 years | Integer | 452–863 | 548 |
| 年齡70-74歲人數 | Age 70-74 | Population aged 70-74 years | Integer | 472–573 | 496 |
| 年齡75-79歲人數 | Age 75-79 | Population aged 75-79 years | Integer | 399–595 | 479 |
| 年齡80-84歲人數 | Age 80-84 | Population aged 80-84 years | Integer | 387–512 | 455 |
| 年齡85-89歲人數 | Age 85-89 | Population aged 85-89 years | Integer | 209–350 | 292 |
| 年齡90-94歲人數 | Age 90-94 | Population aged 90-94 years | Integer | 79–173 | 123 |
| 年齡95-99歲人數 | Age 95-99 | Population aged 95-99 years | Integer | 19–45 | 32 |
| 年齡100歲人數以上 | Age 100+ | Population aged 100 years and above | Integer | 1–8 | 4 |

## Summary Statistics
- **Total Population Trend**: The total population increased from 13,622 in January 2010 to 15,230 in December 2020, indicating steady growth (approximately 11.8% over 11 years).
- **Age Group Trends**:
  - Younger age groups (0-14) show slight declines or stability, with the 0-4 age group ranging from 536 to 623.
  - Middle age groups (20-49) are the largest, with populations often exceeding 1,000, reflecting a robust working-age population.
  - Older age groups (65+) show growth, especially in the 85+ categories, indicating an aging population.
- **Interesting Fact**: The population aged 100+ years, though small (1–8), doubled from 4 to 8 over the decade, reflecting improved longevity.

## Notes
- The year is recorded in the Republic of China (ROC) calendar. To convert to Gregorian years, add 1911 (e.g., 99 = 2010, 109 = 2020).
- The dataset is clean, with no missing values, and all variables are numeric (integers).
- For time-series analysis or visualization, consider reshaping the data to long format, where each row represents a year, month, age group, and population count.