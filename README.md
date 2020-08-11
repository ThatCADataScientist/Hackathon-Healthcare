# Hackathon-Healthcare
Analytics Vidhya

# Problem Background

## Problem Statement -
MedCamp organizes health camps in several cities with low work life balance. They reach out to working people and ask them to register for these health camps. For those who attend, MedCamp provides them facility to undergo health checks or increase awareness by visiting various stalls (depending on the format of camp). 
MedCamp has conducted 65 such events over a period of 4 years and they see a high drop off between “Registration” and Number of people taking tests at the Camps. In last 4 years, they have stored data of ~110,000 registrations they have done.One of the huge costs in arranging these camps is the amount of inventory you need to carry. If you carry more than required inventory, you incur unnecessarily high costs. On the other hand, if you carry less than required inventory for conducting these medical checks, people end up having bad experience.

## Solution Offered -
Through this Machine Learning Algorithm we can predict the probability of a person attending the Health Camps. Thus the company can make inventory arrangements accordingly which in turn would lead to decrease in Inventory carrying costs effectively increasing our profits.

# About the Dataset
The dataset contains 7 files. There is one Test , one Train and 5 additional files. These files have detailed information and its summary is stated in the Train file. We have to merge these files into one on the basis of the key value provided in the dataset. Following are the details of the 5 additional files- 

1)Health_Camp_Detail.csv – File containing Health_Camp_Id, Camp_Start_Date, Camp_End_Date and Category details of each camp.

2)Patient_Profile.csv – This file contains Patient profile details like Patient_ID, Online_Follower, Social media details, Income, Education, Age, First_Interaction_Date, City_Type and Employer_Category

3)First_Health_Camp_Attended.csv – This file contains details about people who attended health camp of first format. This includes Donation (amount) & Health_Score of the person.

4)Second_Health_Camp_Attended.csv - This file contains details about people who attended health camp of second format. This includes Health_Score of the person.

5)Third_Health_Camp_Attended.csv - This file contains details about people who attended health camp of third format. This includes Number_of_stall_visited & Last_Stall_Visited_Number.

# Steps used during the project
1) Exploratary Data Analysis- 
  - Correlation with Target Variable
  - Countplot to know the Target Variables distribution
  - Stacked Bar plot to know the count of every Categorical Feature with respect to the Target Feature
  
 2) Preprocessing and Feature Engineering -
  - Dealing with different Date features by segregating the day, month and year into seperate columns
  - Filling missing values
  - Adding new Features to the Dataset
  - Label and One hot Encoding on the categorical columns
  
  3) Applying models-
  - The problem is a Classfication problem but instead of only predicting 0 and 1, we have to predict the probability of it. The Threshold is not changed thus indicating the default number of 0.5 (ie probability below 0.5 is represented as 0 and above 0.5 is represented as 1) 
  - Pycaret was initially applied to know the best classifiers.
  - Various models were used on the above data and even Stacking Ensemble was used to get the best outcome
  - The best two performing were the Catboost Classifier and the Stacking Ensemble Classification Method
  
  4) Evaluation Metric-
   
   - Model performance was evaluated on the basis of the probability of favourable outcome and the metric to judge it was ROC-AUC score.
   - Catboost Classifier ROC-AUC score was 0.7806047134774845
   - Ensemble ROC-AUC score was 0.7618747104459329
