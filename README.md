# Vehicle CO₂ Emissions — Statistical and Machine Learning Analysis

> Exploratory data analysis and regression model comparisons on a vehicle fuel-consumption and CO₂ emissions dataset.

**Domain:** applied statistics · supervised learning · exploratory data analysis  
**Core tools:** R · R Markdown · caret · randomForest · glmnet · gbm

## Research question

How well can vehicle attributes and recorded fuel-consumption measurements explain or predict reported CO₂ emissions?

The notebook explores data distributions, feature relationships and alternative regression approaches.

## Methods represented in the notebook

- Data exploration, summary tables, distribution plots and correlation analysis.
- Feature preparation and numerical transformations.
- Data splitting into estimation, validation and test partitions.
- Candidate models including linear regression, k-nearest neighbors, regression trees, random forest and boosted regression.
- Model comparison using **RMSE** and **R²**, with an original report preserving the results of the academic exercise.

These are methods found in the source notebook—not claims of externally validated model performance.

## Repository contents

| File | Purpose |
| --- | --- |
| `CO2 release prediction.Rmd` | Editable R Markdown analysis and model code |
| `CO2 Emissions_Canada.csv` | Included data file |
| `CO2 release prediction.pdf` | Original report |
| `CO2 release prediction( code & outputs).html` | Original rendered notebook |

## Reproduce locally

1. Install R and optionally RStudio.
2. Clone or download the repository.
3. Install packages used in the notebook as needed: `tidyverse`, `readr`, `tibble`, `dplyr`, `knitr`, `kableExtra`, `caret`, `rpart`, `rpart.plot`, `ggplot2`, `plotly`, `corrplot`, `gridExtra`, `randomForest`, `glmnet`, `gbm`, and `skimr`.
4. Open `CO2 release prediction.Rmd` and knit/run it from the project directory, so the local CSV file is found.

The legacy report may still require dependency/version adjustments. This documentation pass does not certify that every R Markdown chunk renders successfully.

## Interpretation and limitations

**High apparent accuracy is not sufficient evidence of generalizable forecasting ability.** Several recorded fuel-consumption variables are closely related to measured CO₂ emissions. Any production-oriented comparison should carefully define what inputs are actually available at prediction time.

Additional research-quality checks recommended:
- Move all fitted preprocessing inside the train/validation procedure to avoid leakage.
- Use consistent random splits and repeated or nested cross-validation.
- Separate model selection from final holdout evaluation.
- Report target units, confidence intervals where appropriate and a simple baseline.
- Document the dataset's provenance and redistribution permissions.

## Attribution

The original R Markdown report credits **Mohammad Jamalzehi and Kosar Ghazali**. Preserve that joint attribution when sharing or extending the work.

**Project status:** Academic regression study; not a production emissions forecasting service.
