# Predicting Heart Disease Mortality in the United States
According data from the National Center for Health Statistics (NCHS), which is overseen by the Center for Disease Control (CDC), the leading cause of death in the United States is heart disease. Reliable reporting of this data for all states goes back to 1999, and the most recent public data available is from 2016.

<img src='/images/CDC-logo-nchs.gif'>

Naturally, public health organizations stand to benefit from this data if they can use it to accurately predict heart disease mortality rates in various states. Such a model would allow them to plan and appropriate resources in future years. Given the lag time in public reporting, this project aims to build a model that predicts heart disease mortality rates 3 years into the future. 

The project will culminate in an analysis of risks deemed to be high-risk in 2019.

## Data Sources
### Target Variable
The primary source of data for this objective comes from the [NCHS](https://data.cdc.gov/NCHS/NCHS-Leading-Causes-of-Death-United-States/bi63-dtpu). This dataset contains information for the top 10 leading causes of death, and was used to identify heart disease as the leading cause.

<img src='/images/leading_causes.png'>

The trend in heart disease mortality can be reviewed in the infographic below. Green represents the lowest observed mortality rate for a state since 1999, and red represents the highest rate. As can be seen, the heart disease mortality rate has been dropping overall over the 17 year period.

<img src='/images/HD_Trend.gif'>

Hypothesis tests were performed to confirm that:

- Heart disease mortality is significantly greater than cancer mortality
- Heart disease mortality was significantly lower in 2016 than in 1999

<img src='/images/hd_vs_cancer.png'><img src='/images/hd_1999_vs_2016.png'>

In both instances, the p-values were found to be less than 0.01%.

### Independent Variables
Based on qualitative research, the following were considered viable as initial variables for this analysis:

- **[Age](https://wonder.cdc.gov/Bridged-Race-v2017.HTML)**
- **[Alcohol Consumption](https://pubs.niaaa.nih.gov/publications/surveillance110/tab4-1_16.htm)**
- **[Smoking Rate](https://www.americashealthrankings.org/explore/annual/measure/Smoking/state/ALL)**

It is important to note here that because age itself is a factor, the mortality rate was calculated as number of deaths per capita rather than using the age-adjusted rates provided by the CDC.