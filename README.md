# CapstoneProject
BrainStation Capstone Project - Heart Disease Prediction  
Yumemi Kinsella  
Github: https://github.com/Yuuuuume7/CapstoneProject  

Data source: https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease?select=heart_2020_cleaned.csv  

Included in Repository:
---
1. Notebooks  
2. Supplementary Files
3. Project Overview 
4. Project Oeganization and Flowchart


1.0 - Notebooks
--- 
Notebook '1.Capstone Project - EDA':
  - Includes data cleaning and EDA

Notebook '2.Capstone Project - Sampling imbaranced':
  - Includes sampling process
    Sampled the original dataset in 3 ways:
    * Under sampling
    * Over sampling
    * SMOTE

Notebook '3.Capstone Project - Feature Engineering':
  - Includes converting categorical value into numerical value
  - Includes Feature selecting
    Tried 3 ways
    * SelectKBest
    * RFE
    * RFECV


2.0 - Files
---
File 'heart_2020_cleaned':
  - An original csv file 
    * from Kaggle 
    * for Notebok 1

File 'capstone_clean_heart_disease':
  - A cleaned csv file. Removed unnecessary columns and rows
    * from Notebook 1
    * for Notebook 2, Notebook 3

File 'under_sampled_df':
  - An under sampled csv file which is only included the train set. Removed some of the "No" value of the target variable for balancing the data.
    * from Notebook 2
    * for Notebook 3

File 'over_sampled_df':
  - An over sampled csv file which is only included the train set. Increased rows to have the same number as the majority class by randomly selecting examples from the minority class.
    * from Notebook 2
    * for Notebook 3

File 'smote_df':
  - Sampled csv file by using SMOTE method, which is only included the train set. Increased rows to have the same number as the majority class by creating artificial examples based on the existing data.
    * from Notebook 2
    * for Notebook 3

File 'test_sampled_df':
  - A test set csv file for under sampled data and over sampled data
    * from Notebook 2
    * for Notebook 3

File 'test_smote_df':
  - A test set csv file for SMOTE data
    * from Notebook 2
    * for Notebook 3

File 'capstone_clean_heart_disease_fe':
  - An original cleaned dataset with features converted into numerical values
    * from Notebook 3
    * for Notebook 4

File 'under_sampled_df_fe':
  - An under sampled dataset with features converted into numerical values(train set only)
    * from Notebook 3
    * for Notebook 4

File 'over_sampled_df_fe':
  - An over sampled dataset with features converted into numerical values(train set only)
    * from Notebook 3
    * for Notebook 4

File 'test_sampled_df_fe':
  - A test set for under/over sampling data with features converted into numerical values
    * from Notebook 3
    * for Notebook 4


3.0 - Project Overview
---
the structure of your Areas of Interest Submission, explaining:
* **The Problem Area, including those affected**  
    Firstly, according to the Centers for Disease Control and Prevention (CDC), heart disease is the leading cause of death in the United States. About 695,000 people in the United States died from heart disease in 2021 — that’s 1 in every 5 deaths. This means that about 20% of Americans die from heart disease.

     Secondly, the official poverty rate in the US was 11% in 2020.
     
     Thirdly, about 22% of Americans have avoided some sort of medical care — including doctor visits, medications, vaccinations, annual exams, screenings, vision checks and routine blood work — because of the expense.

     Medical bills in the United Sates are very expensive. There may be some people died from heart disease without seeing a doctor because of medical expense, but those people might have still alive if they did go to see a doctor.

* **My proposed Data Science solution**  
    For reducing deaths from heart disease due to people's low-income, create a heart disease prediction model with personal information such as Body Mass Index (BMI), how do they feel mentally and physically recently, and so forth. This prediction is for people who can't afford to go see a doctor easily, which means the person who probably don't know about their health condition, so the personal information is not included medical information such as blood pressure or if you have diseases. For ordinary people use, create an application which tells you if you suspect that you have heart disease and gives you some advice for your lifestyle or habit based on the prediction model.   

* **The impact of my solution**  
  **The target user** : People who cannot afford medical care due to their low-income.  
  **Societal value**: People don’t have to spend extra money for medical expenses if you don’t suspect that you have heart disease. And People can change their lifestyle or habit to make the chances of getting heart disease lower if they need. 
  

4.0 - Project Oeganization and Flowchart
---
* **A description of my dataset**   
  I found this dataset from Kaggle, but it originally comes from the Behavioral Risk Factor Surveillance System (BRFSS), which conducts annual telephone surveys to collect data on the health status of the United States residents.  

  The cleaned dataset contains 319073 respondents' data. 
  Those dataset has 14 columns;  
   4 numerical variables:  BMI, PhysicalHealth, MentalHealth and SleepTime  
   10 categorical variables:  Smoking, AlcoholDrinking, DiffWalking, Sex, AgeCategory, 
                              Race, PhysicalActivity, GenHealth, Asthma, HeartDisease  
  Those dataset have no missing or invalid values.
  
  **Column Information**  
**HeartDisease** : Respondents that have ever reported having coronary heart disease (CHD) or myocardial infarction (MI) / categorical  
**BMI** : Body Mass Index (BMI) / numeric  
**Smoking** : Have you smoked at least 100 cigarettes in your entire life? (Note: 5 packs = 100 cigarettes) / categorical  
**AlcoholDrinking** : Heavy drinkers (adult men having more than 14 drinks per week and adult women having more than 7 drinks per week) / categorical  
**PhysicalHealth** : Now thinking about your physical health, which includes physical illness and injury, for how many days during the past 30 / numeric  
**MentalHealth** : Thinking about your mental health, for how many days during the past 30 days was your mental health not good? / numeric  
**DiffWalking** : Do you have serious difficulty walking or climbing stairs? / categorical  
**Sex** : Are you male or female? / categorical  
**AgeCategory** : Fourteen-level age category / categorical  
**Race** : Imputed race/ethnicity value / categorical  
**PhysicalActivity** : Adults who reported doing physical activity or exercise during the past 30 days other than their regular job / categorical  
**GenHealth** : Would you say that in general your health is... / categorical  
**SleepTime** : On average, how many hours of sleep do you get in a 24-hour period? / numeric  
**Asthma** : (Ever told) (you had) asthma? / categorical  

**4 datasets**
- Original dataset
  * Total rows: 319,073
    Train set: "Yes" value  19,091 rows
               "No" value  204,260 rows
    Test set: "Yes" value  8,178 rows
              "No" value  87,544 rows

- Under sampled dataset
  * Total rows: 133,904
    Train set: "Yes" value  19,091 rows
               "No" value   19,091 rows
    Test set: "Yes" value  8,178 rows
              "No" value  87,544 rows 

- Over sampled dataset
  * Total rows: 504,242
    Train set: "Yes" value 204,260 rows
               "No" value  204,260 rows
    Test set: "Yes" value  8,178 rows
              "No" value  87,544 rows 

- SMOTE dataset
  * Total rows: 504,242
    Train set: "Yes" value 204,260 rows
               "No" value  204,260 rows
    Test set: "Yes" value  8,178 rows
              "No" value  87,544 rows 

* **Liblaries**
 Basic
 - pandas
 - numpy
 - matplotlib.pyplot
 - seaborn

 For sampling
 - RandomUnderSampler from imblearn.under_sampling
 - RandomOverSampler from imblearn.over_sampling
 - SMOTE from imblearn.over_sampling
 - Counter from collections
 
 For modeling
 - train_test_split from sklearn.model_selection
 - StandardScaler from sklearn.preprocessing
 - LogisticRegression from sklearn.linear_model

 For feature selecting
 - SelectKBest from sklearn.feature_selection
 - f_regression from sklearn.feature_selection
 - RFE from sklearn.feature_selection
 - RFECV from sklearn.feature_selection

 For evaluation
 - classification_report from sklearn.metrics
 - ConfusionMatrixDisplay from sklearn.metrics

**Flowchart**
!Capstone Flow Chart.png
1. Data Collection
  * Download the data from Kaggle

2. Data Cleaning
  * Remove dupulicate rows
  * Remove unnecessary columns
      This project is for ordinaly people, who don't go see a doctor. Therefore, it's concidered that people don't know what diseases they have, so I removed disease infomation.

3. EDA
  * Check the relationship between heart disease existance and other features

4. Data Sampling
  The original data is imbalanced data. Therefore, I did sample in 3 ways.
  * Under sampling
  * Over sampling
  * SMOTE

5. Feature Engineering
  * Convert categorical value into numerical value
  * Feature Selection
    I used and compared the results of 3 methods for feature selecting
    - SelecrKBest
    - RFE
    - RFECV

6. Hyperparameter Tuning

7. Modeling
  * Logistic Regression
  * Decision Tree
  * Random Forest
  * SVM
  * Naive Bayes

8. Create an Application


    

