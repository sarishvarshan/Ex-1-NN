<H3>ENTER YOUR NAME: SARISH VARSHAN V </H3>
<H3>ENTER YOUR REGISTER NO: 212223230196</H3>
<H3>EX. NO.1</H3>
<H3>DATE: 22/08/2025</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
TYPE YOUR CODE HERE
Import Libraries
```

from google.colab import files
import pandas as pd
import seaborn as sns
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
from scipy import stats
import numpy as np
```

Read the dataset

```
df=pd.read_csv("Churn_Modelling.csv")
```
Checking Data
```
df.head()
df.tail()
df.columns
```

Check the missing data
```
df.isnull().sum()
```

Check for Duplicates
```
df.duplicated()
```

Assigning Y

```
y = df.iloc[:, -1].values
print(y)
````
Check for duplicates

```
df.duplicated()
```
Check for outliers
```
df.describe()
```
Dropping string values data from dataset
```
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
data.head()
```
Normalize the dataset
```
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```
Split the dataset
```
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```
Training and testing model
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```



## OUTPUT:
#### Data checking:

<img width="966" height="208" alt="image" src="https://github.com/user-attachments/assets/4d0c90de-fbb7-48b1-a0aa-48be3e9d9515" />

### DUPLICATE IDENTIFICATION:
<img width="519" height="577" alt="image" src="https://github.com/user-attachments/assets/dc391ca2-7993-4ceb-b216-aecbf2a549d6" />


### Values of 'Y':
<img width="382" height="113" alt="image" src="https://github.com/user-attachments/assets/ebf6c200-d71f-46d1-afc6-86bc8bd55cca" />

### Outliers:
<img width="1466" height="395" alt="image" src="https://github.com/user-attachments/assets/1a7aaff3-7930-47af-9d7c-bbfca5184661" />


### Checking datasets after dropping string values data from dataset:
<img width="1202" height="331" alt="image" src="https://github.com/user-attachments/assets/2365646a-9719-4e28-9fa3-bbf748f2841a" />



### Normalize the dataset:
<img width="778" height="569" alt="image" src="https://github.com/user-attachments/assets/345a376c-c0af-4ce9-9459-956bda9ba9d2" />



### Split the dataset:
<img width="538" height="308" alt="image" src="https://github.com/user-attachments/assets/194b55f0-b989-4602-84ac-a6fbcef002c3" />


### Training and testing model:
<img width="668" height="633" alt="image" src="https://github.com/user-attachments/assets/c84f3140-54e0-4bde-bf03-00918df85b67" />



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


