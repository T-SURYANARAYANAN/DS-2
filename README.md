# EXNO2DS
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
        <<import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv('/content/titanic_dataset.csv')
df

![Screenshot (96)](https://github.com/KayyuruTharani/EXNO2DS/assets/142209319/81451b23-08c5-45af-a00f-7e6a0d238a73)

df.info()

![Screenshot (97)](https://github.com/KayyuruTharani/EXNO2DS/assets/142209319/ba3c2652-9331-4ebe-be87-7d90e5248139)

df.shape

![Screenshot (98)](https://github.com/KayyuruTharani/EXNO2DS/assets/142209319/197c0a74-6bf8-49a5-8346-b4ec4a4fba20)

df.head(4)

![Screenshot (98)](https://github.com/KayyuruTharani/EXNO2DS/assets/142209319/5b03fe5c-b620-4a0e-b02d-ebc0aede1dec)

df.describe()

![Screenshot (99)](https://github.com/KayyuruTharani/EXNO2DS/assets/142209319/a070d1bf-2f77-4890-84b4-220fd511850b)

df.set_index("PassengerId",inplace=Tru)
df.describe()

![Screenshot (100)](https://github.com/KayyuruTharani/EXNO2DS/assets/142209319/1f744a40-6898-494c-ade2-8cb82fd20c3d)
>>

# RESULT
        Thus, the Exploratory Data Analysis on the given data set was performed successfully.
