# Alcohol and Drug Use Impact on Health: Patterns and Risk Factor Analysis

## Project Overview
This project analyzes the effects of alcohol and drug use on individuals' health, examining patterns in consumption and identifying key risk factors. The study spans data from 2011 to 2018, providing a comprehensive view of trends and potential health impacts associated with these behaviors. Using machine learning models, we aim to predict the influence of drug and alcohol use on health outcomes and interpret the findings to offer insights into consumption patterns by demographic factors.

## Data Sources
We utilized data from various National Health and Nutrition Examination Survey (NHANES) datasets across the following years:
- 2011-2012
- 2013-2014
- 2015-2016
- 2017-2018

The following datasets were used:
1. **Demographics**: Detailed information on participants' age, gender, race, income, household composition, and other demographic variables.
2. **Questionnaire Data**: A collection of survey responses related to alcohol and drug use, health status, smoking, and cardiovascular health, segmented as follows:
   - **Alcohol Use**: Covers lifetime and recent alcohol consumption.
   - **Drug Use**: Tracks lifetime and recent use of marijuana, cocaine, heroin, and methamphetamine.
   - **Smoking - Cigarette Use**: Records history and frequency of cigarette use.
   - **Current Health Status**: Contains self-reported health status, recent illnesses, and HIV testing history.
   - **Cardiovascular Health**: Includes cardiovascular health metrics and angina pectoris data.

## Data Preparation and Cleaning
### Steps
1. **Demographics Dataset**: Cleaned and segmented demographic data, ensuring a clear structure for household composition, age, race, education, marital status, and military status.
2. **Questionnaire Datasets**: Consolidated key variables in alcohol use, drug use, smoking, current health status, and cardiovascular health, focusing on:
   - Lifetime vs. recent substance use
   - Health assessments and cardiovascular health indicators

### Merging
We merged these datasets to create a comprehensive dataset, allowing us to analyze the impact of substance use on health. This combined data was structured to use drug and alcohol usage metrics as predictors of health outcomes.

## Analysis and Modeling
We used various machine learning models to predict the health impact of alcohol and drug use and conducted feature importance analysis to interpret model findings.

### Models and Results
1. **Random Forest Classifier**:
   - **Accuracy**: 94.4%
   - **F1 Score**: 94.4%
   - Feature importance analysis highlighted critical features, indicating that certain demographic and consumption metrics heavily influenced predictions.

2. **AdaBoost**:
   - **Accuracy**: 91.2%
   - **F1 Score**: 91.1%

3. **Support Vector Machine (SVM)**:
   - **Accuracy**: 93.3%
   - **F1 Score**: 91.4%
   - Applied KFold cross-validation, with mean accuracy and F1 scores of 91.5% and 89.3%, respectively.

4. **XGBoost**:
   - **Accuracy**: 94.7%
   - **F1 Score**: 94.7%

### Additional Modeling (Alcohol Dataset)
We also analyzed alcohol data separately, using Random Forest, AdaBoost, SVM, and XGBoost to explore patterns in alcohol consumption and its health implications. Cross-validation confirmed stable performance, with an XGBoost model achieving the highest accuracy (85.6%).

## Visualizations
We created visualizations to examine patterns in alcohol and drug use by demographic factors, providing insights into consumption frequencies and their distribution across different health and demographic segments.

1. **Daily Joint Consumption**:
   - The “2 per day” category had the highest frequency.
   - Males reported higher consumption than females across all categories.
   - Education level analysis showed "high school/GED" individuals with higher frequencies of daily joint consumption than those with college degrees.

2. **Alcohol Consumption Patterns**:
   - Most individuals reported drinking four or five drinks on only a few days per year.
   - Individuals reporting "poor" health showed higher alcohol consumption than those with "excellent" health.
   - Alcohol consumption tended to decrease as education levels increased.

3. **Health and Joint Consumption**:
   - Those with "poor" self-reported health smoked more joints per day than those in better health categories.

## Conclusion
This project reveals significant patterns in alcohol and drug use, providing insights into how various demographic factors, such as gender, education level, and health status, relate to substance use patterns. The models demonstrate strong accuracy in predicting health impacts based on substance use data, with feature importance analysis highlighting key demographic and behavioral predictors. These findings contribute valuable insights for public health efforts aimed at understanding and mitigating the risks associated with alcohol and drug consumption.

## Code Implementation
### Libraries
- **Python Libraries**: pandas, numpy, sklearn, matplotlib, seaborn
- **Machine Learning**: Random Forest, AdaBoost, SVM, XGBoost
- **Feature Importance**: Feature importance plot using seaborn

### Steps to Run
1. Clone the repository.
2. Run data preprocessing scripts to merge and clean datasets.
3. Execute the analysis notebook to run models and generate visualizations.
4. Review results and model metrics for insights.

## Future Work
Future improvements could include:
- Incorporating additional demographic features for finer-grained predictions.
- Exploring time-series analysis for longitudinal trends in substance use.
- Implementing other ensemble methods to improve model interpretability and accuracy further.

### References
- NHANES Dataset Documentation
- Sklearn Documentation for Machine Learning Models
- University of Michigan
