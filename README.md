# SF-Opioid-Crisis

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

![San Francisco](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/sf-crisis.png)

San Francisco (SF) has a long history of pushing the envelope on progressive public health solutions, including medical cannabis and needle exchange, before either was legal or broadly embraced. It is so out of proportion, that California passed a bill allowing SF to open Safe Injection Sites (SIS).

### Safe injection sites (SIS):

Safe injection sites are medically supervised facilities designed to provide a hygienic and stress-free environment in which individuals are able to consume illicit recreational drugs intravenously and reduce nuisance from public drug use. They are part of a harm reduction approach towards drug problems. North America’s first SIS Insite opened in the Downtown Eastside (DTES) neighborhood of Vancouver in 2003.

## Potential Questions:

1. Comparing types of crime across different neighborhoods. What are the top 5 neighborhoods, where you can get assaulted? Do certain “pairs” of crime frequently co-occur together in a certain neighborhood?
2. Identifying potential neighborhoods for installing SIS for San Francisco government

## Target Variables:

1. Correlation between types of crime and neighborhoods from 2003 to 2018
2. Do certain types of crime co-occur together frequently, or co-occur together in particular neighborhoods (i.e. association rule mining)
3. Correlation between types of drugs used and neighborhoods from 2003 to 2018
4. Identify potential neighborhoods/areas for San Francisco’s government to build safe injection sites
5. Predict the type/category of crime-based on spatial and temporal features provided

## Data:

Our data is collected from the San Francisco police department’s database. It is his- torical data regarding crimes from 2003 to May 2018. The dataset has 13 columns.

![Dataset](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/Dataset-information.png)

## Analysis Approach:

1. Perform data profiling using frequent statistics, and detect any outliers. For example, EDA/visualizations, null analysis. Semantic profiling to identify ho- mogeneous columns - to eliminate extraneous features
2. Create cluster-maps between crime type/category and neighborhoods - perform data normalization/standardization as necessary. Cluster-maps i.e. unsuper- vised learning, will help us to find the correlation between different neighbor- hoods and type of crime.
3. Since this is a classification problem, we are using algorithms like XGBoost, CatBoost, Naive Bayes and Random Forest classifier with the response/target variable as the category/type of crime, and predictors as spatial-temporal columns. Hyperparamater tuning using k-folds cross-validation
4. Preprocess data to filter out crimes that involved Drugs/Narcotics. Perform Step 1 on this subset again. Perform aggregations as necessary to get granu- lar information i.e. Narcotics based crimes categorized by types of drugs i.e. opioids, marijuana, etc.
5. Create cluster-maps between different types of drugs and neighborhoods. Normalize or standardize data as required
6. Encode the data to a transactional form - execute Apriori and FP-growth to find interesting patterns (i.e association rules). Comparative study : FP- Growth vs Apriori

## Results:

### Distribution of categories of crimes from 2003 to 2018:

![Picture-1](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture1.png)

**After Normalization**

![Picture-2](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture2.png)

### Cluster-maps b/w categories of crimes vs neighborhoods:

![Picture-3](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture3.png)

![Picture-4](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture4.png)

### Cluster-maps b/w different opioids & neighborhoods:

![Picture-9](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture9.png)

![Picture-5](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture5.png)

### Specific Opioid Distributions across time:

![Picture-6](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture6.png)

![Picture-7](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture7.png)

### Opioid Distributions across years:

![Picture-8](https://github.com/gandalf1819/SF-Opioid-Crisis/blob/master/results/Picture8.png)

## Team:

* [Kartikeya Shukla](https://github.com/kart2k15)
* [Chinmay Wyawahare](https://github.com/gandalf1819)
* [Hao Shu](https://github.com/hs3812)

## References:

1. [https://www.kqed.org/news/11766169/san-francisco-fentanyl-deaths-up-almost-150](https://www.kqed.org/news/11766169/san-francisco-fentanyl-deaths-up-almost-150)
2. [https://www.sfchronicle.com/bayarea/article/Bay-Briefing-Fentanyl-epidemic-worsens-in-San-14032040.php](https://www.sfchronicle.com/bayarea/article/Bay-Briefing-Fentanyl-epidemic-worsens-in-San-14032040.php)
3. [https://www.businessinsider.com/san-franciscos-dirtiest-street-has-a-drug-market-and-piles-of-poop-2018-10](https://www.businessinsider.com/san-franciscos-dirtiest-street-has-a-drug-market-and-piles-of-poop-2018-10)
4. [https://www.sfchronicle.com/bayarea/article/California-bill-allowing-San-Francisco-safe-13589277.php](https://www.sfchronicle.com/bayarea/article/California-bill-allowing-San-Francisco-safe-13589277.php)
5. [https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-Historical-2003/tmnf-yvry/data](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-Historical-2003/tmnf-yvry/data)
6. [https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-2018-to-Present/wg3w-h783/data](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-2018-to-Present/wg3w-h783/data)
7. [https://data.sfgov.org/d/wkhw-cjsf](https://data.sfgov.org/d/wkhw-cjsf)
