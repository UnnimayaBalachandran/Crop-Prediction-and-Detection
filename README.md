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

#### countplot of Crop_Damage

![Screenshot (312)](https://user-images.githubusercontent.com/54531542/137831778-9cd579f0-2092-4bef-8b14-6e547864bc00.png)

* Crop damage due to pesticides is less in comparison to damage due to other causes.
* Crop type 0 has a higher chance of survival compared to crop type 1.

#### Countplot for Crop_Damage vs Insect count for Crop Type

![Screenshot (314)](https://user-images.githubusercontent.com/54531542/137832009-1321ae63-4807-4c3a-9ae5-8b59e4433949.png)

* Type 2 pesticide is much safer to use as compared to Type 3 pesticide
* Type 3 pesticide shows most pesticide-related damage to crops

#### Crop Damage Vs Number of Weeks Pesticide Used

![Screenshot (316)](https://user-images.githubusercontent.com/54531542/137834067-ca5e3347-8db9-4280-8488-cc2caef32cbf.png)

* From Graph 1 we can conclude that till 20-25 weeks damage due to pesticide is negligible.
* From Graph 3 we can see that after 20 weeks damage due to the use of pesticide increases significantly.

### Bivariate Analysis

#### Crop_Damage vs Estimated_Insects_Count

![Screenshot (318)](https://user-images.githubusercontent.com/54531542/137844075-5b835df2-4074-4d3e-ace5-69a3abb5af14.png)

Clearly observed from the above plot that Most insect attacked crop type 0

#### Crop_Type vs Number_Weeks_Used

![Screenshot (320)](https://user-images.githubusercontent.com/54531542/137844311-e73a2091-ab21-4c02-9601-ebcf6ca09a1f.png)

* Crop Type 0 is more vulnerable to pesticide-related and other damages as compared to Type1

* Avg. duration of pesticide-related damage is lower for Crop type 1

## Outlier Analysis

![Screenshot (322)](https://user-images.githubusercontent.com/54531542/137848685-6a7717bd-8a2e-459b-a8c8-d64fe7445ee2.png)

Clearly, some outliers are present in Insect_Count, doses_week, and number_weeks_quit columns

Now for removing these outliers I simply find the mean value of each column and replace it with an outlier value

## Feature Engineering












