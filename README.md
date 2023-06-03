# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE

NAME: DHIVYAPRIYA. R

REG.NO: 212222230032

import pandas as pd

df=pd.read_csv('/content/Encoding Data.csv')

df.head()

df['ord_2'].unique()

from sklearn.preprocessing import LabelEncoder,OrdinalEncoder

climate = ['Cold','Warm','Hot']

en= OrdinalEncoder(categories = [climate])

df['ord_2']=en.fit_transform(df[["ord_2"]])

df

le = LabelEncoder()

df['Nom_0'] = le.fit_transform(df[["nom_0"]])

df

!pip install --upgrade category_encoders

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data = be.fit_transform(df['bin_1'])

df = pd.concat([df,data],axis=1)

df

be = BinaryEncoder()

data = be.fit_transform(df['bin_2'])

df = pd.concat([df,data],axis=1)

df

df1 = pd.read_csv("/content/data.csv")

df1.head()

df1['Ord_1'].unique()

climate = ['Cold','Warm','Hot','Very Hot']

en= OrdinalEncoder(categories = [climate])

df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])

df1

df1['Ord_2'].unique()

cl = ['High School','Diploma','Bachelors','Masters','PhD']

en= OrdinalEncoder(categories = [cl])

df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])

df1

le = LabelEncoder()

df1['City'] = le.fit_transform(df1[["City"]])

df1

from category_encoders import BinaryEncoder

be = BinaryEncoder()

dat = be.fit_transform(df1['bin_1'])

df1 = pd.concat([df1,dat],axis=1)

df1

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data1 = be.fit_transform(df1['bin_2'])

df1 = pd.concat([df1,data1],axis=1)

df1

df2 = pd.read_csv("/content/titanic_dataset.csv")

df2.head()

be = BinaryEncoder()

data2 = be.fit_transform(df2['Sex'])

df2 = pd.concat([df2,data2],axis=1)

df2

df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])

df2

# OUPUT
![Screenshot from 2023-05-08 21-03-38](https://user-images.githubusercontent.com/119477552/236870818-f5bd80c8-2fb1-4853-b022-0ac7f65091cf.png)
![Screenshot from 2023-05-08 21-04-00](https://user-images.githubusercontent.com/119477552/236870902-9138ceba-5d13-44fa-b0b7-71e8faa398da.png)
![Screenshot from 2023-05-08 21-04-17](https://user-images.githubusercontent.com/119477552/236871095-4caf14ea-0059-4e85-8c3c-82a317121ef5.png)
![Screenshot from 2023-05-08 21-04-59](https://user-images.githubusercontent.com/119477552/236871149-31cc2315-5260-451e-b635-a9abf7922c87.png)
![Screenshot from 2023-05-08 21-05-11](https://user-images.githubusercontent.com/119477552/236871252-264fd16e-98a3-4d01-8f45-e215dc5b7aa7.png)
![Screenshot from 2023-05-08 21-05-47](https://user-images.githubusercontent.com/119477552/236871297-7c5c87d3-caf5-4ada-ad2c-cf986d36563c.png)
![Screenshot from 2023-05-08 21-07-31](https://user-images.githubusercontent.com/119477552/236871380-4c0d5e2f-abde-4196-8e8b-36b013f0fa6f.png)
![Screenshot from 2023-05-08 21-08-04](https://user-images.githubusercontent.com/119477552/236871416-b6d45569-6671-4fcc-a957-f8aabd2fb66c.png)
![Screenshot from 2023-05-08 21-08-26](https://user-images.githubusercontent.com/119477552/236871455-360b49bb-af8a-4ee2-b364-56de1f914f87.png)
![Screenshot from 2023-05-08 21-08-51](https://user-images.githubusercontent.com/119477552/236871604-9e4bf646-bb34-487e-be94-2a1ac77d289c.png)
![Screenshot from 2023-05-08 21-09-02](https://user-images.githubusercontent.com/119477552/236871693-8f17d89b-c11f-4ba2-9f77-8c47cdc03348.png)
![Screenshot from 2023-05-08 21-09-30](https://user-images.githubusercontent.com/119477552/236871910-5435d318-e8e6-4ca9-a0e2-4810c0c7bde4.png)
![Screenshot from 2023-05-08 21-09-57](https://user-images.githubusercontent.com/119477552/236871948-9fa7eba3-63b6-49c9-a58c-77dafb9e33e4.png)
![Screenshot from 2023-05-08 21-10-10](https://user-images.githubusercontent.com/119477552/236871980-a37f2238-7712-4449-b2cd-533df85a56f8.png)
![Screenshot from 2023-05-08 21-10-25](https://user-images.githubusercontent.com/119477552/236872072-b3248740-8a73-42b5-bb8e-972a61d56871.png)
![Screenshot from 2023-05-08 21-11-03](https://user-images.githubusercontent.com/119477552/236872121-d751a0d0-85d5-4ea8-ad77-c2e8da431af1.png)
![Screenshot from 2023-05-08 21-11-18](https://user-images.githubusercontent.com/119477552/236872185-98dbef63-0df3-43ca-8333-7ac0d782d126.png)

RESULT

Thus the Feature Generation process is performed.
