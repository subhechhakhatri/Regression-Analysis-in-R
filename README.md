# Campus Rentals: Rent Prediction Using Regression

**Tools:** R, tidyverse, ggplot2, Linear Regression

## Overview
Maple Street Property Management manages 120 apartments near a university campus. This project uses regression analysis to identify factors related to monthly rent, compare predictive models, and estimate rent for a new apartment.

## Dataset

`CampusRentals.csv` contains:

* Apartment size (`sqft`)
* Bedrooms
* Distance from campus (`dist_km`)
* Building age (`age_years`)
* Parking
* Monthly rent

## Analysis

The project follows six steps:

1. **Explore the data** using summary statistics, visualizations, and correlations.
2. **Split the data** into 70% training (84 apartments) and 30% validation (36 apartments).
3. **Build regression models** — a simple model using `sqft` and a full model using all predictors.
4. **Check residuals** using diagnostic plots and the Shapiro-Wilk test.
5. **Compare models** using validation RMSE and backward elimination.
6. **Make a business recommendation** using the selected model.

## Key Results

The Full model explained approximately **92.8% of the variation in rent** (R² = 0.928).

Important findings:

* Larger apartments were associated with higher rents.
* Apartments farther from campus tended to have lower rents.
* Older buildings tended to have lower rents.
* Parking was associated with higher rent.
* Bedrooms was not statistically significant after accounting for the other variables.

### Model Comparison

| Model    | Validation RMSE | Adjusted R² |
| -------- | --------------: | ----------: |
| **Full** |      **$65.12** |       0.923 |
| Step     |          $65.79 |       0.924 |
| Simple   |         $129.68 |       0.720 |

The Full model had the lowest validation RMSE and was therefore used for the final prediction.

## Business Recommendation

For a new **900 sq. ft., 2-bedroom apartment**, located **2 km from campus**, in a **10-year-old building with parking**, the model predicts:

**Estimated rent: $1,342/month**

**Prediction interval: $1,211–$1,473/month**

The analysis demonstrates how regression can support a more data-driven approach to apartment pricing.

## Skills

`R` `tidyverse` `ggplot2` `Linear Regression` `Model Selection` `Residual Diagnostics` `RMSE` `Data Visualization` `Business Analytics`

## Files

* `CampusRentals.csv` — Dataset
* `Campus_Rentals.Rmd` — R Markdown analysis
* `Campus_Rentals.html` — HTML report
* `README.md` — Project documentation


## Citations & Attribution

* R Core Team (2026), *R: A Language and Environment for Statistical Computing*
* Wickham et al. (2019), `tidyverse`
* Xie (2025), `knitr`
* Dataset: `CampusRentals.csv`
* Dataset and coding guidance provided through course materials and adapted for this analysis.



