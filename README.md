# ML-model-_Titantic-data
competition project for Kaggle Titantic data

You have learned many DL knowledge from our wonderful course. Now, it is your time to 
show how well you can solve practical problems. Please visit Kaggle website 
(https://www.kaggle.com/c/titanic) to join the competition project for Titantic data. 

Use libraries and templates for dealing with input data you should implement at 
least one your own ML model, e.g., decision tree, KNN, LR, etc, from scratch, i.e., do not use any 
ML libraries at one model, only from numpy in python.

## 1. Exploratory Data Analysis
### 1.1 Target feature
From total 891 passengers in training set, around 350 survived. As the pie chart showed, Only
38.4% of the total training set survived after the crash

### 1.2 Feature Engineering
#### 1.2.1 PClass
We can see that Passenegers Of Pclass 1 have higher chance to secure. Although the the number
of passengers in Pclass 3 were higher, the number of survival from Pclass 3 is low.
#### 1.2.2 Sex
Sex is a categorical Feature with two type( male/female). We can found that female survived is
higher than male. Lets dive in to check survival rate with Pclass and sex together.
#### 1.2.3 PClass and Sex
Create two new column to mark female who in Pclass 1 & 2, who are indicate rich women. Also,
mark make who in Pcalss 3, who refer to poor men.
#### 1.2.4 Name
Use last name of name to check whether passanger in their family have survived.
#### 1.2.5 Embarked
We can see that the most common embarded type is S. Becasue there are 2 missing data in
Embarded feature, we will just fill the most common one which is S type
#### 1.2.6 Fare
By hist graph, Fare featrue is a left skew distribution. Fare is also a continous feature that need to
convert it into ordinal value.We use pandas qcut to splits to 4 bins.
#### 1.2.7 Age
As we had seen earlier, Age feature has 177(train)+ 86(test) null values. To replace these NaN
values, we need to observe age of max/min/mean to understand the range of age. From the
histrogrm graph, we can assume age feature is normal distribution. Then, we can assgin the
random value in within +1/-1 segma range. Becasue age is a continous feature, we need to use
binning to catergrize.
#### 1.2.8 Cabin
Since there are more than 60% of Cabin featrue is missing, we can't fill values by reference other. I
will only mark people who have cabin in this trip.
#### 1.2.9 SibSp and Parch
Create new columns called "Family_size" and "Alone". By calculate Parch and SibSp columns, we
can know family size of the passengers.

### 1.3 One hot Encoding - Categorical data

### 1.4 Create a sub-test group to test accuracy rate

## 2. KNN model
### 2.1 Create KNN class
### 2.2 Test KNN model
### 2.3 Predict test dataset

## 3. Logistic Regression
### 3.1 Create LR class
### 3.2 Test LR model
### 3.3 Predict test dataset

## 4. Submit Kaggle score - 0.787
