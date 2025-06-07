# Standardized-Mortality-Ratio

Standardized mortality ratio (SMR) is a calculation that compares the number of deaths observed in a population over a given period of time to the expected number of deaths over the same period of time based on a standard population.

# Interpretation

+ SMR > 1 indicates that more deaths occurred than expected.
+ SMR < 1 indicates that fewer deaths occurred than expected.
+ Statistical significance can be interpreted based on p-values and confidence intervals, for example,
  * Whether P-value<0.05
  * Whether the 95% confidence interval include the null value of 1

# Challenge & Solution

+ CDC mortality rates by age group, sex, and year for all races are available for download. However, the dataset includes 113 individual causes of death, which need to be consolidated into broader categories by ICD code—such as subsequent neoplasms, cardiac, pulmonary, external, and other causes—for analysis. Using reference documentation and code, I compiled a consolidated CDC mortality rate dataset covering the years 1975 to 2022. Due to data limitation, mortality rates for 1975–1978 were substituted using 1979 values, and the 2017 rate was replaced with that of 2016.
+ While the concept of the Standardized Mortality Ratio (SMR) is straightforward, the complexity lies in accurately calculating the weighted distribution of age and calendar year during the cohort's follow-up period. This step is crucial for estimating the expected number of deaths. My colleague had implemented this using a SAS macro, and I adapted the same logic to develop a corresponding function in R. This allows us to perform the entire SMR calculation workflow within the R environment.

# Practice in R

# Reference

