# Stat301-Group26
# Final Report 
#### Group Members: Ivan Tan, Ruohan Sun, Hiroshi Nasuno, Samin Intisar
## Introduction

Employee attrition is a key issue for organizations, resulting in increased costs, lost knowledge, and disruptions in operations. Understanding and anticipating employee turnover is critical for HR management and organizational planning. Previous studies have emphasized the necessity of using data-driven methods to uncover significant factors impacting attrition, such as compensation, employment tenure, and workplace environment. This study uses a dataset of 4,653 employee records, including factors such as education level, age, gender, payment tier, and job experience, to develop a predictive model for attrition.

We will be using this dataset:

https://www.kaggle.com/datasets/tawfikelmetwally/employee-dataset 

This is a sample dataset that includes data for employees in a company, notably their qualifications, time of joining, location, salary tiers, age, gender, if they have been without assigned work, experience, and a target column of whether they have left. The data is anonymized, it is real data that has been provided by someone with access to a company's HR data, however all the staff and the company is unknown for privacy reasons. There is missing context for some of the columns, notably salary tiers, where it is not known what each tier means, although there is speculation from users of the dataset that a higher tier means more pay, it is not confirmed whether it is true or false.

### Detailed Variable Descriptions

| **Variable Name**           | **Description**                                                          | **Type**         | **Example Values**        |
|-----------------------------|---------------------------------------------------------------------------|-----------------|---------------------------|
| `Education`                 | Educational qualifications (degree, field of study, etc.)                | Categorical     | "Bachelors"        |
| `Joining Year`              | Year the employee joined the company                                     | Numerical       | 2015, 2018                |
| `City`                      | Location where the employee works                                        | Categorical     | "New Delhi", "Pune"     |
| `Payment Tier`              | Employee’s salary tier (categorization of income levels)                 | Ordinal         | 1, 2, 3                   |
| `Age`                       | Age of the employee                                                      | Numerical       | 25, 34, 42                |
| `Gender`                    | Employee’s gender identity                                               | Categorical     | "Male", "Female" |
| `Ever Benched`              | Whether the employee was temporarily without assigned work               | Binary          | "Yes", "No"               |
| `Experience in Current Domain` | Number of years the employee has worked in their current field      | Numerical       | 2, 5, 7                  |
| `Leave or Not` (Target)     | Indicates if the employee left the company (attrition)                   | Binary          | 0 (No), 1 (Yes)           |

Data Distribution and Summary Statistics:
- Education: The majority of employees have a Bachelor’s degree (3,601), followed by Master’s (873) and PhD (179) qualifications.
- Joining Year: Employees joined between 2012 and 2018, with a median joining year of 2015.
- City: The largest number of employees are from Bangalore (2,228), followed by Pune (1,268) and New Delhi (1,157).
- Payment Tier: Payment tiers are distributed as 1 (243 employees), 2 (918 employees), and 3 (3,492 employees).
- Age: The age range of employees is from 22 to 41 years, with a mean age of approximately 29.4 years.
- Gender: The dataset includes 1,875 female and 2,778 male employees.
- Ever Benched: Most employees have not been benched (4,175), while 478 have experienced benching.
- Experience in Current Domain: The experience ranges from 0 to 7 years, with a mean of approximately 2.9 years.
- Leave or Not: 1,600 employees have left the company, while 3,053 have remained.

### Research Question

The dataset's target variable, Leave or Not, indicates whether an employee has left the company, while the remaining variables serve as predictors. To analyze these relationships, the study applies Lasso regression, a machine learning technique for feature selection and regularization. Tibshirani's (1996) introduction of Lasso regression demonstrated its ability to handle high-dimensional datasets by penalizing less relevant variables, making it an ideal choice for this analysis. Furthermore, previous studies' theoretical frameworks, such as those mentioned in the NIPS conference article on machine learning techniques, give a solid foundation for understanding how predictive analytics might be applied in organizational settings.

The research question guiding this study is: *What factors contribute to predicting whether an employee will leave the company or not?* By addressing this question, the study aims to identify the most significant predictors of attrition and provide actionable insights for improving employee retention strategies. The results are expected to inform human resource policies and contribute to the broader literature on predictive analytics in workforce management.
