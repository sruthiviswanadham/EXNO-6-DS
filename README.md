# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

### Name: V.SAI SRUTHI
### Register Number: 212223100061

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
```

```
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
```

```
sns.lineplot(x=x,y=y)
```

![image](https://github.com/user-attachments/assets/b4275f1f-0c57-4c2b-83b0-9fe33f3e8342)

```
df = sns.load_dataset("tips")
df
```

![image](https://github.com/user-attachments/assets/f6e2c7dc-2ecf-42d1-8edd-de2537309513)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```

![image](https://github.com/user-attachments/assets/1b046b33-5d42-4f35-a24a-63dcf93c31e3)

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
```

```
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```

![image](https://github.com/user-attachments/assets/9c068fd4-5fcb-43f1-b42c-5d01e9c9783a)

```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

![image](https://github.com/user-attachments/assets/f031a3d6-7150-4ed1-90a2-3215685168bb)

![image](https://github.com/user-attachments/assets/0034f35a-02c6-46ee-b186-733a836f99fc)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

![image](https://github.com/user-attachments/assets/eb7509a8-ba57-4b74-8214-d86f67df1e81)

![image](https://github.com/user-attachments/assets/f6e35835-0823-4479-9d4c-fc3935865128)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```

```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```

![image](https://github.com/user-attachments/assets/71bb19f4-00ca-498b-9485-b5780fa28da7)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```

![image](https://github.com/user-attachments/assets/991b52dc-0316-44c4-963d-f1c6195467d5)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```

![image](https://github.com/user-attachments/assets/2ed50f22-4961-4d32-af43-147b1998b947)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```

![image](https://github.com/user-attachments/assets/c8d5abc4-9e74-431d-a3d8-3d2bd8ec720c)

![image](https://github.com/user-attachments/assets/8164e0cd-13bc-4937-aee6-d2f7ca2bddf7)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

![image](https://github.com/user-attachments/assets/0bd4acb1-c856-4003-84eb-3b29dffba43b)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/user-attachments/assets/f3a9b77d-74c5-4a6a-b075-61bae2d19a63)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

![image](https://github.com/user-attachments/assets/baa46404-22d8-42f5-abeb-2d9ba21e39ef)

```
sns.histplot(data = num_var, kde = True)
```

![image](https://github.com/user-attachments/assets/2c1cc438-6832-4f2c-9daa-aebd44f424e5)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

![image](https://github.com/user-attachments/assets/1e9128e4-f31e-494f-b122-5d7ff8fe0419)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

![image](https://github.com/user-attachments/assets/fb9b8027-deb5-4b26-9003-a69cda42c4df)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

![image](https://github.com/user-attachments/assets/1969428e-d06c-45fb-a192-db66772a24fa)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![image](https://github.com/user-attachments/assets/736cd172-2ba6-466e-8796-a1af25d59dc5)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

![image](https://github.com/user-attachments/assets/f01ac116-612e-4930-9277-36cdd46318fa)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```

![image](https://github.com/user-attachments/assets/dc2de28a-b79a-46f2-bc4c-3255d8894f1a)

```
sns.kdeplot(data=mart,x='PassengerId')
```

![image](https://github.com/user-attachments/assets/2de4830c-c4ad-4c62-aced-6993eb7dd6e5)

```
sns.kdeplot(data=mart,x='Age')
```

![image](https://github.com/user-attachments/assets/8ec04612-a157-4fdd-a303-7e2207a300a6)

```
sns.kdeplot(data=mart)
```

![image](https://github.com/user-attachments/assets/08d74171-e795-4db7-9701-5f6b23ed9185)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

![image](https://github.com/user-attachments/assets/9b038dd1-17b4-4372-b38c-4e9ec8aebbb9)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![image](https://github.com/user-attachments/assets/97e21c4c-287e-4809-845a-aba8122815bb)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

![image](https://github.com/user-attachments/assets/80ab6c32-d34b-4560-8c65-4262994ba4ff)

```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/3359be20-e995-41ef-82e5-1a120f80b7af)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
