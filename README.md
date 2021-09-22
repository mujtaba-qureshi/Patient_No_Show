# Patient_No_Show
# ML - Supervised Learning
Building a Supervised Learning Model to predict patients being no_show to their doctor's appointment

## Introduction

This project is aimed to build a machine learning model which predicts:

**whether or not patients show up for their appointment.** 

The dataset includes information from 100k medical appointments in Brazil. A number of characteristics about the patient are included in each row. 
* `ScheduledDay` tells us on what day the patient set up their appointment.
* `Neighborhood` indicates the location of the hospital.
* `Scholarship` indicates whether or not the patient is enrolled in Brasilian welfare program _Bolsa Família_.
* It is important to be mindful about the encoding of the last column: it says `No` if the patient **showed up** to their appointment, and `Yes` if they **did not show up.**

The data was downloaded from [Kaggle](https://www.kaggle.com/joniarroba/noshowappointments)

### Two Stages of the Project:
#### 1. **Explore and clean the data**: `investigate-a-dataset-project.ipynb`

No machine learning or modelling in this step. The data was cleaned and efforts were made to make _elementary sense_ of the variables.
 _(Note: This notebook was created **before** I learnt any ML concepts. While the code and commentary in this notebook is extremely rudimentary and borderline comical, 
it was useful for creating a **cleaned version** of the data which was used for building ML models.)_

**Input**: `no_show_data_2.csv`
**Output**: `no_show_data_clean.csv`

#### 2. **Building different ML models**: `No_Show_Parameter_Testing_Model_Selection.ipynb`

Different machine learning models were created in this step to better _predict whether patients will show up to their doctor appointments after booking them._

**Input**: `no_show_data_modelling.csv`

### Conclusion:
After tuning the _Hyper Parameters_ of multiple machine learning algorithms, **AdaBoost Classifier** (with learning rate of 1.5 and n_estimators of 50) was found to provide the highest accuracy of **79.8%**

### Files Included in the Repo
* `No_Show_Parameter_Testing_Model_Selection.ipynb` - Final notebook that has the hyper parameter testing and model selection of most accurate model
* `Patient_No_Show_Cross_Val_Ceck.ipynb` - Notebook containing cross validation checks to decide the best performing ML model. _No hyper testing was performed in this_
* `Patient_No_Show_Decision_Tree.ipynb` - Notebook containing building a _Decision Tree_ to classify no-show patients
* `investigate-a-dataset-project.ipynb` - The very first notebook which was used to explore and clean data. It output the cleaned dataset which was used for creating ML models
* `no_show_data_2.csv` - Original csv file downloaded from the link. This was used to investigate the dataset and cleaning exercises
* `no_show_data_clean.csv` - Cleaned dataset - used as an input for modelling notebooks
* `no_show_data_modelling.csv` - Dataset containing dummy codes for categorical variables. The final data file for Modelling

#### Imp Note:
(22 Sept '21) This repo is a bit of a mess at the moment, especially with multiple notebooks, each mentioning a separate ML concept. I am planning on tidying it up in my next available opportunity 
