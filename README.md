# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
import pandas as pd

data1=pd.read_csv('/content/Data_set.csv')

data2=pd.read_csv('/content/Loan_data.csv')

print(data1)

data1.head(10)


print(data2)

data2.head(10)


data1.info()

data2.info()


data1.isnull()

data2.isnull()


data1.isnull().sum()

data2.isnull().sum()


data1['show_name']=data1['show_name'].fillna(data1['aired_on'].mode()[0])

data1['aired_on']=data1['aired_on'].fillna(data1['aired_on'].mode()[0])

data1['original_network']=data1['original_network'].fillna(data1['aired_on'].mode()[0])

data1.head()


data2['LoanAmount']=data2['LoanAmount'].fillna(data2['LoanAmount'].mode()[0])

data2['Dependents']=data2['Dependents'].fillna(data2['Dependents'].mode()[0])

data2['Self_Employed']=data2['Self_Employed'].fillna(data2['Self_Employed'].mode()[0])

data2['Gender']=data2['Gender'].fillna(data2['Gender'].mode()[0])

data2.head()


data1['rating']=data1['rating'].fillna(data1['rating'].mean())

data1['current_overall_rank']=data1['current_overall_rank'].fillna(data1['current_overall_rank'].mean())

data1.head()


data2['Loan_Amount_Term']=data2['Loan_Amount_Term'].fillna(data2['Loan_Amount_Term'].mean())

data2.head()


data1['watchers']=data1['watchers'].fillna(data1['watchers'].median())

data1.head()


data2['Credit_History']=data2['Credit_History'].fillna(data2['Credit_History'].median())

data2.head()


data1.info()

data2.info()


data1.isnull().sum()

data2.isnull().sum()

# OUPUT
![data1-print](https://user-images.githubusercontent.com/87276633/226176406-1ba6ec94-e809-4251-a60a-a64733d78f47.png)
![data2-print](https://user-images.githubusercontent.com/87276633/226176455-600b37ee-23f2-4eb8-8154-da20d055a69f.png)
![data1-info](https://user-images.githubusercontent.com/87276633/226177223-2b9545a6-edb2-4df1-9e68-3e7961ecb4a8.png)
![data2-info](https://user-images.githubusercontent.com/87276633/226176719-24af8e3c-b1f8-441f-a7c3-cc91f9896110.png)
![data1-isnull](https://user-images.githubusercontent.com/87276633/226177234-3697b016-76e4-4ac2-94c9-1b19830242da.png)
![data2-isnull](https://user-images.githubusercontent.com/87276633/226176737-cb399615-63ae-43f2-9f8d-f683e2d11732.png)
![data1-mode](https://user-images.githubusercontent.com/87276633/226177264-df351645-cf94-4053-86d5-134879256a8b.png)
![data2-mode](https://user-images.githubusercontent.com/87276633/226177273-0952f6d2-5eb7-4fc0-a3a4-441dfe9ede06.png)
![data1-mean](https://user-images.githubusercontent.com/87276633/226177287-bfea14ce-46b4-4486-8fbf-0f88d44a7059.png)
![data2-mean](https://user-images.githubusercontent.com/87276633/226177295-b6e21b57-1133-4b43-bd63-48f3c8cce722.png)
![data1-median](https://user-images.githubusercontent.com/87276633/226177316-b20fa90c-99a7-4205-a0b0-057e320a3312.png)
![data2-median](https://user-images.githubusercontent.com/87276633/226177333-c6ed1cac-c42f-4bbf-87fd-b6f588bbf653.png)
![data1-after](https://user-images.githubusercontent.com/87276633/226177340-c79adb12-1dab-4c0b-bfac-5f439ea61449.png)
![data2-after](https://user-images.githubusercontent.com/87276633/226177352-67d16a46-35c3-4200-8e9a-cfcbf6237190.png)
![data1,2-after](https://user-images.githubusercontent.com/87276633/226177360-874eb2b2-b682-43c5-b89f-2d4792db6360.png)

# Result:

Thus the given data is read,cleansed and the cleaned data is saved into the file.





