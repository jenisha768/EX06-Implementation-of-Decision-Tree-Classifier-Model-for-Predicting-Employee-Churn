# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Dataset: Use pandas to load the dataset (CSV, Excel, etc.) into a DataFrame.
2. Handle Missing Values: Identify and fill or drop missing values.
3. Encode Categorical Variables: Use label encoding or one-hot encoding for categorical data (e.g., department, gender).
4. Split the Dataset: Divide the dataset into features (X) and target (y), then split into training and testing sets.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: JENISHA TEENA ROSE F
RegisterNumber: 2305001010 
*/
import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data=df.copy()
data.describe()
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data
X=data.drop(['Departments','left'],axis=1)
Y=data['left']
clt=DecisionTreeClassifier()
clt.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clt,feature_names=X.columns,class_names=['LEFT','NOT LEFT'],filled=True)
plt.show()
```

## Output:
![decision tree classifier model](sam.png)
![11](https://github.com/user-attachments/assets/06d77169-9084-43b3-a9fe-ab488d9b7d45)
![Screenshot (91)](https://github.com/user-attachments/assets/ee24e946-f468-424a-9add-a1bbb433f620)
![Screenshot (92)](https://github.com/user-attachments/assets/014bf7f8-a1d2-4bef-86ee-cf541ca39fdb)
![Screenshot (93)](https://github.com/user-attachments/assets/a33adf6d-a76d-4c63-b3d2-b710989f4c2a)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
