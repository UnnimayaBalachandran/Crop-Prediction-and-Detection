# Crop Prediction and Detection

![image](https://user-images.githubusercontent.com/54531542/137821846-551bddc5-c71d-4f0e-a7b4-d7eec23ad969.png)

## Problem Definition

To determine the outcome of the harvest season, i.e. whether the crop would be healthy (alive), damaged by pesticides, or damaged by other reasons thus intensifying farming and agricultural systems

## Dataset and Description

We have two datasets given to train and test

* test_agriculture.xlsx - Test Data set
* train_agriculture.csv - Train Data set

## Feature Description

ID: UniqueID 

Estimated_Insects_Count: Estimated insects count per square meter 

Crop_Type: Category of Crop(0,1) 

Soil_Type: Category of Soil (0,1) 

Pesticide_Use_Category: Type of pesticides uses (1- Never, 2-Previously Used, 3-Currently Using) 

Number_Doses_Week: Number of doses per week 

Number_Weeks_Used: Number of weeks used 

Number_Weeks_Quit: Number of weeks quit 

Season: Season Category (1,2,3)

Crop_Damage: Crop Damage Category (0=alive, 1=Damage due to other causes, 2=Damage due to Pesticides)

## Data Preprocessing

* Checked Null Values:  Checked null values and found that there were 9000 missing values present in the Number_Weeks_Used variable.
* Checked Datatypes: Checked Datatypes of all columns, to see any inconsistencies in the data.
* Checked Unique Values: To understand unique values if present in columns, which will help to reduce dimensionality in future processing.
* Replaced missing values: As there are 9000 missing values in the Number_Weeks_Used column, replaced them by mode of the data

## Exploratory Data Analysis

### Checked Correlation

![Screenshot (310)](https://user-images.githubusercontent.com/54531542/137828235-e16ced42-8404-4e7e-90cc-afcff8983475.png)


* Estimated_Insects_count,Pesticide_use_category and Number_weeks_used are positively correlated with Crop damage.
* Number_weeks_used is positively correlated with Estimated_Insects_count and Pesticide_use_category.
* Number_weeks_Quit is highly negatively correlated with Pesticide_use_category and Number_weeks_used.

### Data Visualizations

#### Univariate Analysis



