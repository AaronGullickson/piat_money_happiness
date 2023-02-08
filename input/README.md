# Data Source Description

The data we will use for this project come from the [General Social Survey](https://gss.norc.org/About-The-GSS) (GSS) waves of 2006, 2008, 2010, 2012, and 2014. The GSS is a nationally representative survey of US adults conducted every two years by the National Opinion Research Council. It is a major source of data on political attitudes in the US. We use the years between 2006-2014 because this data provides the most detailed income data to address our question of interest.

From the full data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.Rmd R Markdown document. The name of the dataset in R is `gss`. 

* **happiness**: Respondents were asked whether they felt "Very happy", "Pretty happy", or "Not too happy." To simplify our analysis, I have scored these values respectively as 1, 0, and -1. This is the key dependent variable.
* **fam_income**: The reported family income of the respondent. This is not reported in exact dollar amount but rather in income brackets and is thus an ordinal variable. I have collapsed some income brackets to create 10 separate categories that roughly correspond to the deciles of the distribution (deciles are like quartiles but for 10% increments rather than 25%). Thus, moving up one bracket here roughly corresponds to moving up to the next 10% of the income distribution. This is the key independent variable.
* **gender**: The self-reported gender of the respondent as male or female.
* **age**: The age of the respondent in years. Youngest respondents are 18 years of age.
* **race**: The self-reported race of the respondent in the categories of White, Latino, Black, Asian, American Indian, Pacific Islander, Multiracial or Other.
* **educ**: The respondent's total years of education.
* **marstat**: The respondent's current marital status in the categories of never married, married, divorced, separated, or widowed.
* **region**: The respondent's region of the country in the categories of the northeast, midwest, south, and west.
* **year**: year of the survey.
