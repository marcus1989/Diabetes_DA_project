# Diabetes prediction dataset

Diabetes prediction dataset is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. It is intended to support healthcare professionals, data analysts, and decision-makers in understanding trends, predicting risks, and improving patient outcomes. This document outlines key business user requirements for the dataset.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
The dataset contains 10,000 records with 9 columns that capture demographic, clinical, and lifestyle factors related to diabetes. The data is cleaned and ready for analysis.
* Age Range: 0.08 – 80 years
* Hypertension and Heart Disease
* BMI:
        Ranges from 10.64 to 87.7
        Mean: 27.34
* HbA1c Level:
        Ranges from 3.5 to 9.0
        Mean: 5.55
* Blood Glucose Level:
        Ranges from 80 to 300 mg/dL
        Mean: 138.2 mg/dL
Diabetes Prevalence: ~8.69% of individuals have diabetes

## Business Requirements
* Identify high-risk patients based on clinical and lifestyle factors.
* Provide predictive insights for early diagnosis and intervention.
* Enable healthcare providers to make data-driven treatment decisions.
* Improve patient monitoring and risk assessment over time.
* Support research and policy development in diabetes prevention.


## Hypothesis and how to validate?
1.	Higher BMI is associated with an increased risk of diabetes.
        •	Patients with a BMI > 30 are more likely to be diabetic than those with a normal BMI.
2.	Higher HbA1c levels are associated with diabetes progression.
        •	Patients with HbA1c levels above 6.5% are more likely to develop complications.
3.	Higher blood glucose levels are correlated with diabetes diagnosis.
        •	Individuals with fasting glucose levels above 120 mg/dL have a higher probability of diabetes.
 

## Project Plan
- Data collection was done using kaggle API. The dataset used was (https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)
- For data cleaning step, I first selected 10000 rows from the original csv file.
- The age column is changed from float to int and stored in a column called AGE.
- Using the standard diviation method, drop outliers from the bmi(std div +- 4 iqr) and blood_glucose_level(std div +- 3 iqr) collumns.
-  Used data cleaning effect and feature engineering using numerical, ordinal and outlier_winzorizer
* Why did you choose the research methodologies you used?
- the pearson correlation between each feature used like 'bmi', 'HbA1c' and 'Blood glucose level' with diabetes and plotting through different plots like scatter plots, bar plots, pie charts etc helped me to prove the hypthosis was right or wrong.


## The rationale to map the business requirements to the Data Visualisations
* Diabetes prevalence by BMI, HbA1c and Blood glucose levels
* Correlations between high BMI (BMI > 30) and diabetes
* Correlations between high HbA1c (HbA1c ≥ 6.5) and diabetes
* Correlations between high blood glucose level (blood glucose level > 120 mg/dL) and diabetes

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
 - ETL pipeline
    - extract the data from kaggle repository using the kaggle API
    - data cleaning and transformation done through pandas and ML feature engineering.
 - data visualization using Matplotlib, Seaborn and plotly
* How did you structure the data analysis techniques. Justify your response.
- I had three cleaning steps. Each cleaned data is then stored to a .csv file, which is then used for the encoding/transformation step and also for the data visualization step.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
- The data I used was already cleaned version.
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?
- I used chat GPT to check if my approach was correct. I also used chatGPT to optimize my code.

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Unfixed Bugs
* I didnt have any bugs to fix

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
-I had more outliers in the bmi and blood_glucose_level features which I removed most of it. I used the standard diviation method to identify the outliers and box plot to view the outliers. I then droped them from the columns.
- I also also used feature engineering to view the differences between original dataset and the cleaned dataset from datacleanup2.
* What new skills or tools do you plan to learn next based on your project experience?
- I want to improve my data analytics skills, more time management and documentation. I also want to improve my understanding of ML- feature engineering, the ETL pipeline and more data visualization and explainations.

## Main Data Analysis Libraries
* I have used python numpy and pandas library for data cleaning and ETL steps. 
* For data visualization, I have used matplotlib, seaborn and plotly libraries.
* For transformation and encoding, the scikit learn was used

## Credits 

* code institute LMS material
* stackoverflow  
* chatGPT
* google searches

### Content 

- The etl and data visualization code where taken form the code institute LMS content. 
- The data cleaning effect and feature engineering code was taken from the LMS material  - Feature Engine Topic 9:  Custom    Data Cleaning and Feature Engine Workflow
- stackoverflow
- used chaptGPT for some predictions

### Media

- The code institute logo from (https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)
- github for version control - (https://github.com/marcus1989/Diabetes_DA_project)


## Acknowledgements (optional)
* I wish to thank my facilitator Vasi, technical head Niel, our data coach John for the support during the project development.
* I wish to thank my class coleagues Dani, Raihan, Saoni, Mohammad and Bruno for their support.