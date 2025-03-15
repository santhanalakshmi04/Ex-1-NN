<H3>NAME: SANTHANA LAKSHMI K</H3>
<H3>REGISTER NO: 212222240091</H3>
<H3>EX. NO.1</H3>
<H3>DATE: 15.03.2025</H3>
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
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```

```
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df
```

```
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df
```

```
df.isnull().sum()
```

```
df.duplicated()
```

```
df.describe()
```

```
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1
```

```
x=df1.iloc[:,:-1].values
x
```

```
y=df1.iloc[:,-1].values
y
```

```
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```

## OUTPUT:
## DATASET:
![Screenshot 2025-03-10 154144](https://github.com/user-attachments/assets/a35e4788-9992-4790-b149-8ff8eba05b67)

## DROPPING THE UNWANTED DATASET:
![Screenshot 2025-03-10 154200](https://github.com/user-attachments/assets/7529e14c-021c-44e0-b686-e2db15804ead)

## CHECKING NULL VALUES:
![Screenshot 2025-03-10 154208](https://github.com/user-attachments/assets/51983d5f-602f-491d-a82c-793a68658267)

## CHECKING FOR DUPLICATION:
![Screenshot 2025-03-10 154240](https://github.com/user-attachments/assets/888daf01-95f4-4c83-ad80-7465cc4cfe7b)

## DESCRIBING THE DATASET:
![Screenshot 2025-03-10 154249](https://github.com/user-attachments/assets/1a633ece-a020-487c-9187-f1ed5607ddba)


## SCALING THE DATASET:
![Screenshot 2025-03-10 154259](https://github.com/user-attachments/assets/e6025ef5-f15f-468c-b124-535417f6ca23)

## X FEATURES:
![Screenshot 2025-03-10 154308](https://github.com/user-attachments/assets/6a279396-d46c-4299-9dcd-02c2a1d638d1)

## Y FEATURES:
![Screenshot 2025-03-10 154314](https://github.com/user-attachments/assets/49cf7fe8-f7e8-4253-829b-23ca374dd9a1)

## SPLITTING THE TRAINING AND TESTING DATASET:
![Screenshot 2025-03-10 154330](https://github.com/user-attachments/assets/e04487b2-f0d5-4ed8-9cf5-13f08887687d)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.
