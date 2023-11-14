# Ex-08-Data-Visualization-
## AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

## Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## ALGORITHM
### STEP 1
Read the given Data

### STEP 2
Clean the Data Set using Data Cleaning Process

### STEP 3
Apply Feature generation and selection techniques to all the features of the data set

### STEP 4
Apply data visualization techniques to identify the patterns of the data.

## PROGRAM:
```
Developed By: BEJIN B
Reg No: 212222230021
```
### READING THE GIVEN FILES
```
import pandas as pd
df=pd.read_csv("/content/Superstore.csv",encoding='unicode_escape')
df.head()
```
### DATA VISUALIZATION USING SEABORN :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
- <B>_LINE PLOT:_</B>
```
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
![280221142-ebf5d018-c31c-4610-b26e-6395daeb5448](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/58cbf14b-be4c-4e0e-8dd8-1393eb433f38)
![280221177-f50bd4c8-8840-4d61-afa9-f090d98716d2](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/54d73697-f249-4ae3-9cb1-6f09e8097e71)
![280221197-dddc0ce1-5d37-463d-af9d-d9a39cf33def](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/012ffe0c-c37f-4b5b-9774-851c6c80262c)
- <B>_SCATTERPLOT:_</B>
```
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```
![280221332-23b30b9e-cb60-4dd5-a7a7-be941b7e291d](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/fe93555f-426e-4e6d-b1a5-0f66375667d7)
![280221367-e422342a-4fff-487e-9780-aa92e2db6b19](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/d3c5002e-1cd2-45c9-8ad0-151c3d374d48)
![280221405-8f9e780a-bcdd-47e0-a21e-25e8dca37cab](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/c790d92f-eb32-432c-ba1f-798cd998e6c1)
- <B>_BOXPLOT:_</B>
```
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```
![280221591-68af3f52-c256-452b-b987-afc6767d09ac](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/890d4930-dc09-4b3d-8321-93df6299501c)
![280221620-27f1e245-2725-436d-a68b-df3b3c5c1660](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/03767fc8-637f-4605-ba27-8fd864aa367e)
- <B>_VIOLIN PLOT:_</B>
```
sns.violinplot(x="Profit",data=df)
```
![280221737-19b590d7-641d-47ed-af0f-40e52df39587](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/68ad87ed-c7a8-4fd9-a037-110be1070835)
- <B>_BARPLOT_</B>
```
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```
![280221836-16ece634-b224-42df-82be-c4a731f908af](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/8f1ffd8f-61c0-4354-a4dd-5df43731b468)
![280221914-32fcf2ae-85be-4bfa-bacb-0839304efe5b](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/4a212715-041a-42d4-a79f-c9a44359b79a)
- <B>_POINTPLOT_</B>
```
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```
![280222052-cc5c01fb-bc88-4f6e-8f53-08e45f679e08](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/8a188b82-9665-411d-8349-206fcb44e3d0)
- <B>_COUNT PLOT_</B>
```
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```
![280222076-b6e8298d-0a6c-4a58-85b6-6a0e5c53508f](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/92647ef8-282a-4c15-91e0-05c449b491ad)
![280222110-a9e07021-4889-490c-8451-69864bf6f778](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/cfdb1596-13aa-4eff-a456-bb795da36da7)
- <B>_HISTOGRAM_</B>
```
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
```
![280222156-6e5a4fab-1cfd-4415-9a76-6e398571742b](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/e5387d84-19ef-4d5f-8348-9cd9541b37a0)
- <B>_KDE PLOT_</B>
```
sns.kdeplot(x="Profit", data = df,hue='Category')
```
![280222235-2129a043-381c-4b04-a0da-5b6745ba0adf](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/63050c7e-873e-49cf-b420-0af15b8d2942)
### DATA VISUALIZATION USING MATPLOTLIB :
- <B>_PLOT_</B>
```
plt.plot(df['Category'], df['Sales'])
plt.show()
```
![280224173-5f621aad-c520-4e01-96cf-1701acefa1e7](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/226ff664-ad3f-4f2a-afb5-176e4be6aa69)
- <B>_HEATMAP:_</B>
```
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
![280224277-d133809e-1704-4f91-8332-0041d7ca3e33](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/d6c2920b-ceee-4867-b306-9ca33733bbcf)
- <B>_PIECHART:_</B>
```
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
```
![280224381-09b81541-1b03-4017-bd64-e20c6894898b](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/b8c53d45-76c4-4eb4-8dca-c57ce32b9522)
![280224408-76eb96a0-0bec-4d40-af21-f906b45b9c16](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/9cf347af-a870-47cf-a6fd-38f86e558595)
- <B>_HISTOGRAM:_</B>
```
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
![280224500-5d549a00-18a3-4126-af87-1652098f826d](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/b7cb36ea-b329-434c-861c-9297b3e9ea33)
- <B>_BARGRAPH:_</B> 
```
plt.bar(df.index,df['Category'])
plt.show()
```
![280224538-bee209ed-e0f9-4968-94c7-babc9140edfb](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/d746ed3c-588f-4232-ad3f-8a82a5669018)
- <B>_SCATTERPLOT:_</B>
```
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
![280224583-82653e8a-3f2a-4a58-ae41-0631925cd402](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/b5759a19-e4c8-4be1-ba7f-92197d14c969)
- <B>_BOXPLOT:_</B>
```
plt.boxplot(x="Sales",data=df)
plt.show()
```
![280224625-9515bcd2-15ba-453a-a02e-e3e6e3ea875c](https://github.com/Aakash0407/ODD2023-Datascience-Ex-08/assets/118799103/656bcb93-988a-4d2e-905d-2ea362ed79d9)
## RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
