# EX.NO-2 DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
Name : SURYANARAYANAN T
Register Number: 212224040341
```
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
dt = pd.read_csv("/content/titanic_dataset (2).csv")
dt
```
![image](https://github.com/user-attachments/assets/1060d834-730d-4915-9dc2-e42839c2ba6a)
```
dt.info()
```
![image](https://github.com/user-attachments/assets/8d7fb573-26a9-41fd-b04f-461127ceef48)
```
dt.shape
```
![image](https://github.com/user-attachments/assets/32156650-0ff4-44a8-b2aa-c7a9dc1041eb)
```
dt.set_index("PassengerId",inplace=True)
dt.describe()
```
![image](https://github.com/user-attachments/assets/909842ca-24bf-4196-ab19-08db28aa0cb1)
```
dt.nunique()
```
![image](https://github.com/user-attachments/assets/7420fb06-a8a7-4b7e-9963-068e2b8ffe34)
```
dt["Survived"].value_counts()
```
![image](https://github.com/user-attachments/assets/8ba9a30e-25f5-4c8d-aac8-42e64bd5575d)
```
per = (dt["Survived"].value_counts()/dt.shape[0]*100).round(2)
per
```
![image](https://github.com/user-attachments/assets/060c82aa-46ae-4d37-9bc3-9f999577ea33)
```
sns.countplot(data = dt,x="Survived")
```
![image](https://github.com/user-attachments/assets/28d7a87a-a0e3-464d-934e-21600406a427)
```
dt
```
![image](https://github.com/user-attachments/assets/4126790c-6278-48c4-b540-135293d88e8d)
```
dt.Pclass.unique()
```
![image](https://github.com/user-attachments/assets/4e5395eb-471a-4e35-bb81-7268dd4efaa3)
```
dt.rename(columns = {'Sex' : 'Gender'},inplace=True)
dt
```
![image](https://github.com/user-attachments/assets/1b97908e-606d-410f-9c8a-a56d4560a8f5)
```
sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5,aspect=.7)
```
![image](https://github.com/user-attachments/assets/ec4ad13e-a64b-45db-8958-c59c0ad6c54c)
```
sns.catplot(x='Survived',hue="Gender",data=dt,kind="count")
```
![image](https://github.com/user-attachments/assets/c8d06102-825c-4c9d-a764-3c36841ab633)
```
dt.boxplot(column="Age",by="Survived")
```
![image](https://github.com/user-attachments/assets/d7dff06a-e560-4b57-acd0-25f6ce512a47)
```
sns.scatterplot(x = dt["Age"],y=dt["Fare"])
```
![image](https://github.com/user-attachments/assets/0e8a74ba-3d4d-48fd-a656-86a7b7a7ed35)
```
sns.jointplot(x="Age",y="Fare",data=dt)
```
![image](https://github.com/user-attachments/assets/d8ab53f7-da92-42c8-a3fb-880e7c47cf73)
```
fig ,ax1 = plt.subplots(figsize=(8,5))
pt = sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=dt)
```
![image](https://github.com/user-attachments/assets/74a33e00-4afc-472e-b893-b09698ddc2fb)
```
sns.catplot(data=dt,col="Survived",x="Gender",hue="Pclass",kind="count")
```
![image](https://github.com/user-attachments/assets/284ab95d-9f92-41a0-9a93-7c6829b36c23)
```
data = dt[['Survived','Pclass','Age','SibSp','Parch','Fare']]
correlation = data.corr()
sns.heatmap(correlation,annot=True)
```
![image](https://github.com/user-attachments/assets/3bb0756d-ed10-4998-b928-2afba11497a4)
```
sns.pairplot(dt)
```
![image](https://github.com/user-attachments/assets/c93a0590-f2f0-43d7-b573-d826ca6a4c3c)

# RESULT
        The Exploratory Data Analysis is performed in the given dataset
