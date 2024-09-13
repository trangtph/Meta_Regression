# Introduction
Example of data set to perform meta-regression on the effect of sex on the effect estimates of treatment on an outcome

# Data structure:
The data consists of the effect estimates and the characteristics of 10 studies. Each study contributed multiple effect estimates with varied sex proportions, age groups, and risk window lengths.

## Variables description:

- `study_id`, `effect_id`: the ID of each study and each effect estimate
- `log_effect`: the log-transformed of the effect estimates (incidence rate ratio)
- `var`: variance of the log-transformed effect estimates
-  `prop_male_guess`: proportion of males in the study sample. Five categories: 0%, <45%, 45%-55%, >55%, 100%
-  `prop_male_merge`: same as `prop_male_guess` but the level "<45%" and "45%-55%" were collapsed into "roughly equal"
-  `risk_window_cat`: Length of the risk window. Categorical variable.
-   `age_med_cat_guess`: the age group of the study sample. Categorical variable.
-   `prop_male_guess_0` to `prop_male_merge_roughly.equal`: the dummy variables of `prop_male_guess` and `prop_male_merge`
-   `prop_male_guess_0.c` to `prop_male_merge_roughly.equal.c`: the dummy variables centered around the study mean
-   `prop_male_guess_0_m` to `prop_male_merge_roughly.equal_m`: the study mean values of the dummy variables.
