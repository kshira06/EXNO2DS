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
        <<INCLUDE YOUR CODING AND OUTPUT SCREENSHOTS>>
```
import pandas as pd
df=pd.read_csv("C:\\Users\\admin\\Downloads\\titanic_dataset.csv")
df
```
<img width="1430" height="623" alt="image" src="https://github.com/user-attachments/assets/06444c09-796e-4ec5-b92b-9c73afee9213" />

```
df.shape
```
<img width="1327" height="84" alt="image" src="https://github.com/user-attachments/assets/0e871600-8d45-4e61-9985-a6e843ab1614" />

```
df.set_index("PassengerId",inplace=True)
df
```
<img width="1323" height="587" alt="image" src="https://github.com/user-attachments/assets/c19a2eeb-aa3e-4299-bf02-3e0735b0fc9e" />

```
df.unique()
```
<img width="1147" height="314" alt="image" src="https://github.com/user-attachments/assets/445a6e49-6bc7-4cd4-9976-713c42de4a0c" />

```
df['Survived'].value_counts()
```
<img width="1191" height="134" alt="image" src="https://github.com/user-attachments/assets/bd2f722a-a0aa-4b7c-b6bc-16d92b1203b0" />

```
df.Pclass.unique()
```
<img width="1216" height="81" alt="image" src="https://github.com/user-attachments/assets/8190e488-5948-43a8-9fba-3b8f61472551" />

```
df.rename(columns={"Sex":"Gender"},inplace=True)
df
```
<img width="1333" height="587" alt="image" src="https://github.com/user-attachments/assets/dbbb406f-9014-4e94-a306-71ffb74002b9" />

```
import seaborn as sns
sns.countplot(data=df)
```
<img width="1376" height="674" alt="image" src="https://github.com/user-attachments/assets/2a3112c5-b324-42db-a190-22dbafeaa89f" />

```
sns.countplot(x="Survived",hue="Gender",data=df)
```
<img width="1167" height="637" alt="image" src="https://github.com/user-attachments/assets/3a8c0849-4f4f-49ff-bd5a-40232f61d324" />

```
sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
```
<img width="1290" height="704" alt="image" src="https://github.com/user-attachments/assets/db37945c-9e88-42c9-ac6f-5968b1cf248f" />

```
sns.boxplot(data=df)
```
<img width="1045" height="621" alt="image" src="https://github.com/user-attachments/assets/19fdcdd8-b61b-47da-bb10-a365af595b3f" />

```
df.boxplot(column="Survived",by="Gender")
```
<img width="1148" height="658" alt="image" src="https://github.com/user-attachments/assets/c4cf9a1a-0bd4-4f8c-9034-f8cc4c2ff617" />

```
sns.scatterplot(data=df)
```
<img width="1393" height="646" alt="image" src="https://github.com/user-attachments/assets/de0b9e6c-654e-402f-9c4a-082d0d33cded" />

```
sns.scatterplot(x=df['Age'],y=df['Fare'])
```
<img width="1389" height="645" alt="image" src="https://github.com/user-attachments/assets/4be635da-cc2d-468d-9cbf-b935206a5054" />

```
sns.jointplot(x='Age',y='Fare',data=df,kind='kde')
```
<img width="1315" height="822" alt="image" src="https://github.com/user-attachments/assets/36fd07b8-a701-453e-b0e3-0c426e0f69c8" />

```
sns.jointplot(x='Age',y='Fare',data=df,kind='hist')
```
<img width="1387" height="839" alt="image" src="https://github.com/user-attachments/assets/541f46c2-15e6-4924-8f95-179109cf7eaf" />


# RESULT
        Therefore result is successfully executed
