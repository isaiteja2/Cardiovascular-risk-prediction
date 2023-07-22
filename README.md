# **Project Name**    - **CardioVascular Risk Prediction**
Verified Project: [Credentials]([https://github.com](https://certificates.almabetter.com/en/verify/89571777280666))

##### **Project Type**    - Classification
##### **Contribution**    - Individual
##### **Name** - Saiteja Ch

# **Project Summary -**

Overall Project Flow:

1. **Know Your Data**: Imported necessary libraries and loaded the dataset. Performed initial exploration to understand the structure of the data and identify any issues such as missing or duplicate values.
2. **Understanding Your Variables**: Described the variables in the dataset and checked their unique values. Performed data wrangling to clean and prepare the data for analysis.
3. **Data Visualization**: Used visualization techniques to understand the relationships between variables and identify patterns or trends in the data.
4. **Hypothesis Testing**: Tested assumptions about the data and confirmed findings through statistical tests.
5. **Feature Engineering & Data Pre-processing**: Handled missing values and outliers, encoded categorical variables, and selected important features. Transformed and scaled the data as needed, and reduced its dimensionality if necessary.
6. **Data Splitting**: Split the data into training and test sets for model development.
7. **ML Model Implementation**: Trained several machine learning models, including logistic regression, random forest, XGBoost, SVM, and Naive Bayes. Evaluated the performance of each model and selected the best one for final prediction.
8. **Conclusion**

# **GitHub Link -**

GitHub Link - https://github.com/isaiteja2/Cardiovascular-risk-prediction

# **Problem Statement**

The dataset is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes.
Each attribute is a potential risk factor. There are both demographic, behavioral, and medical risk factors.

### What did you know about your dataset?

The dataset has 3390 rows and 17 columns. There are no duplicate rows. The dataset contains information about various health-related factors such as age, education, sex, smoking habits, cholesterol levels, blood pressure, diabetes, BMI, heart rate, glucose levels and the risk of coronary heart disease in 10 years. The columns that have missing values are education (87 missing values), cigsPerDay (22 missing values), BPMeds (44 missing values), totChol (38 missing values), BMI (14 missing values), heartRate (1 missing value) and glucose (304 missing values).

### Variables Description 

- **id:** A unique identifier for each row in the dataset.
- **age:** The age of the individual in years.
- **education**: The level of education of the individual.
- **sex:** The sex of the individual.
- **is_smoking:** Whether the individual is a smoker or not.
- **cigsPerDay:** The number of cigarettes smoked per day by the individual.
- **BPMeds:** Whether the individual is on blood pressure medication or not.
- **prevalentStroke:** Whether the individual has had a stroke or not.
- **prevalentHyp:** Whether the individual has hypertension or not.
- **diabetes:** Whether the individual has diabetes or not.
- **totChol:** The total cholesterol level of the individual.
- **sysBP:** The systolic blood pressure of the individual.
- **diaBP:** The diastolic blood pressure of the individual.
- **BMI:** The body mass index of the individual.
- **heartRate:** The heart rate of the individual.
- **glucose:** The glucose level of the individual.
- **TenYearCHD:** The risk of coronary heart disease in 10 years for the individual.

### What all manipulations have you done and insights you found?


**Overview**
- The dataset contains information on 3390 individuals.
- **Target Variable:** 2879 individuals do not have heart disease and 511 have heart disease.

**Smoking Habits**
- Smokers are more likely to have heart disease than non-smokers.
- 275 smokers have heart disease compared to 236 non-smokers.

**Gender**
- Males and females are almost equally likely to have heart disease.
- 272 males and 239 females have heart disease.

**Hypertension**
- Individuals with prevalentHyp are more than twice as likely to have heart disease as those without prevalentHyp.
- The ratio of people with and without prevalentHyp prone to heart disease is 23.85% and 11.03%, respectively.

**History of Stroke**
- Individuals with prevalentStroke are three times more likely to have heart disease than those without prevalentStroke.
- The ratio of people with and without prevalentStroke prone to heart disease is 45.45% and 14.88%, respectively.

**Diabetes**
- Individuals with diabetes are more than twice as likely to have heart disease as those without diabetes.
- The ratio of people with and without diabetes prone to heart disease is 37.93% and 14.47%, respectively.

**Blood Pressure Medication**
- Individuals taking BPMeds are more than twice as likely to have heart disease as those not taking BPMeds.
- The ratio of people with and without BPMeds prone to heart disease is 33.00% and 14.51%, respectively.

**BMI**
- Underweight individuals have a higher risk of heart attack (19.5%) compared to normal weight (12.3%) and overweight individuals (16.9%).

**Age**
- Individuals in Late Adulthood have the highest risk of heart disease (39.4%) compared to those in Early Adulthood (0%), Early Middle Age (7%), and Late Middle Age (18.1%).

**Heart Rate**
- Heart rate appears to be related to the risk of heart disease.

**Cholesterol Levels**
- Cholesterol levels appear to be related to the risk of heart disease.

These insights suggest that factors such as smoking habits, hypertension, history of stroke, diabetes, use of blood pressure medication, BMI, age, heart rate and cholesterol levels may all play a role in an individual's risk of developing coronary heart disease in 10 years.

### ***Hypothetical testing Observations:***


* Statement 1:

 * Results:

    ***Chi-square statistic:*** 34.632

    ***p-value:*** 3.98 x 10^-9

  * Conclusion:

    Based on the p-value, which is much less than 0.05, we ***reject the null hypothesis*** and conclude that there is a significant association between smoking status and the risk of developing CHD in the next 10 years.

* Statement 2:

 * Results:

    ***t-statistic:*** -10.211

    ***p-value:*** 3.97 x 10^-24

  * Conclusion:

    Based on the p-value, which is much less than 0.05, we ***reject the null hypothesis*** and conclude that there is a significant difference in the mean BMI between smokers and non-smokers.

* Statement 3:
 * Results:

    ***Chi-square statistic:*** 22.161

    ***p-value:*** 6.04 x 10^-5

  * Conclusion:

    Based on the p-value, which is less than 0.05, we ***reject the null hypothesis*** and conclude that there is a significant association between prevalent hypertension and the risk of developing CHD in the next 10 years.
    
    #### What all missing value imputation techniques have you used and why did you use those techniques?
    
    In order to handle missing values in the dataset, I used several techniques. First, I dropped rows with missing values in all columns except for the education and glucose columns. This means that any row with a missing value in the cigsPerDay, BPMeds, totChol, BMI or heartRate column was removed from the dataset. This approach was taken to ensure that the remaining data was as complete as possible.

Next, I imputed missing values in the education column with the mode of that column. The mode is the most frequently occurring value in a column. I calculated the mode of the education column and used it to fill in any missing values in that column. This approach was taken because it is a simple and effective way to handle missing data in categorical columns.

Finally, I imputed missing values in the glucose column with the median of that column. The median is the middle value when all values in a column are sorted in ascending order. I calculated the median of the glucose column and used it to fill in any missing values in that column. This approach was taken because it is a robust measure of central tendency that is less sensitive to outliers than the mean.

These techniques were chosen because they are simple and effective ways to handle missing data. By removing rows with missing values in certain columns and imputing missing values in other columns with common statistical measures such as the mode and median, I was able to retain as much data as possible while minimizing the impact of missing values on my analysis.

##### What all outlier treatment techniques have you used and why did you use those techniques?

In order to handle outliers in the dataset, I used the Interquartile Range (IQR) method. For each column in the dataset, I calculated the first quartile (Q1) and third quartile (Q3) values. The IQR is then calculated as the difference between Q3 and Q1. Using the IQR, I calculated the upper and lower bounds for outlier detection as Q3 + 1.5 * IQR and Q1 - 1.5 * IQR, respectively.

Next, I used these upper and lower bounds to identify and treat outliers in each column. Any value in a column that was greater than the upper bound was replaced with the upper bound value, and any value that was less than the lower bound was replaced with the lower bound value.

The IQR method is a commonly used technique for identifying and treating outliers in a dataset. It is based on the assumption that data within a column follows a normal distribution, with most values falling within a certain range around the mean. Values that fall outside this range are considered outliers and can be treated by replacing them with more reasonable values, such as the upper or lower bounds calculated using the IQR method.

#### What all categorical encoding techniques have you used & why did you use those techniques?

In order to encode the categorical columns in the dataset, I used label encoding. I created label encoders for the sex and is_smoking columns using the LabelEncoder class. I then fit these encoders to the data in the respective columns and used them to transform the data. This replaced the original categorical values in these columns with numerical values that represent the different categories.

In addition to encoding the categorical columns, I also dropped the id column from the dataset because it has no effect on my model.

Label encoding is a simple and effective technique for encoding categorical data. It assigns a unique numerical value to each category in a column, allowing categorical data to be represented in a format that can be used by machine learning algorithms. I chose this technique because it is easy to implement and works well with many machine learning algorithms.

##### What all feature selection methods have you used  and why?

In order to prepare the dataset for further analysis or modeling, I performed several feature manipulations and feature selection methods. Here's a step-by-step description of what I did:

**Step 1: Feature Manipulations**
- First, I created a new feature called smoking_status based on the cigsPerDay column. This feature categorizes individuals as non-smokers, light smokers, moderate smokers or heavy smokers based on the number of cigarettes they smoke per day.
- Next, I created a new feature called Hypertension based on the diaBP and sysBP columns. This feature classifies individuals based on their blood pressure levels using a scale from 0 to 7, with higher values indicating higher blood pressure.
- I also created a new feature called cholesterol_category based on the totChol column. This feature categorizes individuals as having normal, borderline or high cholesterol levels based on their total cholesterol level.
- Finally, I encoded the smoking_status and cholesterol_category columns using ordinal encoding. This replaced the original categorical values in these columns with numerical values that represent the different categories in a specified order.

**Step 2: Feature Selection**
- After performing the feature manipulations, I removed several columns from the dataset that were either highly correlated with other columns or were not considered relevant for my analysis. These columns included is_smoking, sysBP, diaBP, cigsPerDay, totChol and prevalentHyp.
- Next, I created a heatmap to visualize the correlation between the remaining numerical columns in the dataset. This allowed me to quickly identify pairs of columns that were highly correlated or not correlated at all and make informed decisions about which features to include in my analysis or modeling.

Overall, these feature manipulations and feature selection methods were performed to enhance the dataset and improve the performance of any machine learning models trained on it. By creating new features, encoding categorical data and selecting relevant features, I was able to prepare the dataset for further analysis or modeling in a more readable and organized manner.

##### Which all features you found important and why?

In order to determine which features were most important for predicting the target variable, I used a feature importance plot from an XGBoost classifier. According to the plot, the features with an F-score above 100 were age, Hypertension, smoking_status, glucose, BMI, heart rate, sex and cholesterol.

These features were found to be important because they have a strong relationship with the target variable and provide valuable information for making predictions. For example:

- **Age** is a well-known risk factor for heart disease and is likely to be an important predictor in any model that aims to predict the risk of heart disease.
- **Hypertension** is a condition where an individual has high blood pressure. High blood pressure can damage the arteries and increase the risk of heart disease.
- **Smoking status** indicates whether an individual is a smoker or not. Smoking is a major risk factor for heart disease as it can damage the lining of the arteries and lead to a buildup of fatty material.
- **Glucose** levels indicate the amount of sugar in an individual's blood. High blood sugar levels can damage the blood vessels and increase the risk of heart disease.
- **BMI** is a measure of body fat based on an individual's height and weight. Being overweight or obese can increase the risk of heart disease as it can lead to high blood pressure, high cholesterol levels and diabetes.
- **Heart rate** is the number of times an individual's heart beats per minute. A high heart rate can indicate that the heart is working harder than normal and may be a sign of an underlying condition that increases the risk of heart disease.
- **Sex** can also play a role in the risk of heart disease. Men are generally at a higher risk of heart disease than women.
- **Cholesterol** levels indicate the amount of cholesterol in an individual's blood. High cholesterol levels can lead to a buildup of fatty material in the arteries and increase the risk of heart disease.

Overall, these results suggest that age, Hypertension, smoking_status, glucose, BMI, heart rate, sex and cholesterol are all important features for predicting the risk of coronary heart disease in 10 years.

### 1. Which Evaluation metrics did you consider for a positive business impact and why?

I considered several evaluation metrics to assess the performance of your model and its potential positive business impact. These metrics include accuracy, precision, recall, F1-score, and ROC AUC score.

***1. Accuracy:***

  Accuracy measures the overall correctness of the model's predictions. It is calculated as the ratio of correct predictions to the total number of predictions. A high accuracy indicates that the model is making correct predictions for a large proportion of the data.

***2. Precision:***

  Precision measures the proportion of true positive predictions among all positive predictions. In other words, it measures how many of the positive predictions made by the model are actually correct. A high precision indicates that the model is making few false positive predictions.

***3. Recall:***

   Recall measures the proportion of true positive predictions among all actual positive instances. In other words, it measures how many of the actual positive instances were correctly identified by the model. A high recall indicates that the model is making few false negative predictions.

***4. F1-score:***

  The F1-score is a measure that combines precision and recall to provide a single number that represents the balance between these two metrics. It is calculated as the harmonic mean of precision and recall. A high F1-score indicates that the model has a good balance between precision and recall.

***5. ROC AUC score:***

   The ROC AUC score measures the ability of the model to distinguish between the two classes. It is calculated as the area under the receiver operating characteristic (ROC) curve, which plots the true positive rate against the false positive rate at different classification thresholds. A high ROC AUC score indicates that the model is able to effectively distinguish between the two classes.

The choice of which evaluation metric to use depends on the specific business problem and the goals of the model. For example, if the cost of false positives is high, then precision may be an important metric to consider. If the cost of false negatives is high, then recall may be more important. In some cases, a balance between precision and recall may be desired, in which case the F1-score could be a useful metric.

# **Conclusion**

Overall conclusions from the whole project:

1. Heart disease is present in a significant number of individuals in the dataset.
2. Smoking is associated with an increased risk of heart disease.
3. Males have a higher risk of heart disease than females.
4. Certain medical conditions such as hypertension, stroke, diabetes, and the use of blood pressure medication are associated with an increased risk of heart disease.
5. The risk of heart disease increases with age, with the highest risk observed among people in Late Adulthood.
6. Heart rate does not appear to have a significant impact on the risk of heart disease.
7. High cholesterol levels are associated with an increased risk of heart disease.
8. The majority of people in the dataset do not have heart disease, regardless of their age, heart rate, or cholesterol levels.
9. Early Adulthood appears to be a low-risk age group for heart disease.
10. Finally, Random Forest Classifier is proven with the highet accuracy, f1-score and ruc-aoc score with 90% on test data.
