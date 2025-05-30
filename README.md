<H3>NAME       : MIDHUN S</H3>
<H3>REGISTER NO:212223240087</H3>
<H3>EX.NO:1</H3>
<H3>DATE</H3>
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
```py
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

data = pd.read_csv("Churn_Modelling.csv")
data
data.head()

X=data.iloc[:,:-1].values
X

y=data.iloc[:,-1].values
y

data.isnull().sum()

data.duplicated()

data.describe()

data = data.drop(['Surname', 'Geography','Gender'], axis=1)
data.head()

scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)

X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)

X_train

X_test

print("Lenght of X_test ",len(X_test))


```
## OUTPUT:
### Dataset:
![data](https://github.com/user-attachments/assets/83723510-3ed2-4a42-a05d-90f5b6654a4d)

### X Values:
![x_values](https://github.com/user-attachments/assets/9f1e438a-2b13-4061-b628-b647a57493cb)

### Y Values:
![y_values](https://github.com/user-attachments/assets/50e9d665-b603-4d1d-9e4e-8276e62128d5)


### Null Values:
![null_values](https://github.com/user-attachments/assets/a372d295-d19a-48c2-90dd-58bf2659c841)

### Duplicated Values:
![duplicated_values](https://github.com/user-attachments/assets/1bc4bce8-7a57-4d3c-8589-ec5926324f32)

### Description:
![describe](https://github.com/user-attachments/assets/59861376-1d40-4211-8b1b-18658d8f0988)

### Normalized Dataset:
![normalized](https://github.com/user-attachments/assets/5f3572a6-d0b1-45bb-98ae-0cd3f0624117)

### Training Data:
![training ](https://github.com/user-attachments/assets/c8b45564-ddeb-435a-b3f5-054aaa7322b1)

### Testing Data:
![test](https://github.com/user-attachments/assets/52830e9c-da76-4c7f-b2f4-a3f278a3fc2f)



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


