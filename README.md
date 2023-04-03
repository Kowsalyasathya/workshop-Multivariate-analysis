# workshop-Multivariate-analysis
## AIM:

To perform multivarient analysis on the given data set.
## ALGORITHM:

1.Clean the data

2.Remove outliers

3.Apply the skew function and Kurtosis

4.Apply Bivariate analysis on numerical and categorical

5.Apply Multivariate analysis.
## CODE:
import pandas as pd
import seaborn as sns
df=pd.read_csv("/content/FlightInformation.csv")
df

df.info()

df.isnull().sum()

df['Route']=df['Route'].fillna(df['Route'].mode()[0])
df['Total_Stops']=df['Total_Stops'].fillna(df['Total_Stops'].mode()[0])
df.isnull().sum()

df.kurtosis()

df.skew()

sns.boxplot(x=df['Price'],y=df['Source'],data=df)

sns.scatterplot(x=df["Price"],y=df["Duration"],data=df)

sns.displot(df,x="Source",hue="Destination")

sns.barplot(x=df['Price'],y=df['Source'],data=df)

df.corr()

import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df= pd.read_csv("FlightInformation.csv")
df= np.random.randint(low = 1, high = 100, size = (10,10))
print("The data to be plotted:\n")
print(df)
hm = sns.heatmap(data=df)
plt.show()

## OUTPUT:
Bivariate Analysis:
DATA SET:
![Screenshot (182)](https://user-images.githubusercontent.com/118671457/229584571-227f82fe-5df2-4b40-8c8d-76c7879b0be2.png)
INFO
![Screenshot (183)](https://user-images.githubusercontent.com/118671457/229584653-afbcf031-ea37-4a2c-8323-a55e278351d3.png)
DETECTING NULL AS PD:
![Screenshot (184)](https://user-images.githubusercontent.com/118671457/229584672-79329203-e310-4032-9e8c-b40df0365eb0.png)
REMOVING NULL DATA:
![Screenshot (185)](https://user-images.githubusercontent.com/118671457/229584680-313841be-731b-421b-9217-af6b8a332a7c.png)

![Screenshot (186)](https://user-images.githubusercontent.com/118671457/229584720-ae0c0f5b-6a20-4f48-b163-8a6d92ecdc3d.png)
NUMERICAL & NUMERICAL:
SCATTER_PLOT:
![Screenshot (188)](https://user-images.githubusercontent.com/118671457/229584790-6083c861-0382-4e8c-afed-a3e86a12c671.png)
NUMERICAL & CATEGORIAL:
BOX PLOT

![Screenshot (187)](https://user-images.githubusercontent.com/118671457/229584759-21232ef2-991c-4a78-a232-6498a77e81f6.png)
![Screenshot (189)](https://user-images.githubusercontent.com/118671457/229584841-3f6f4dbb-f716-4d86-98b3-a07909907ba4.png)
![Screenshot (190)](https://user-images.githubusercontent.com/118671457/229584862-e8fbbc88-b386-4a1f-9f64-ffb758e151d6.png)
MULTIVARIENT ANALYSIS:
CORRELATION:
![Screenshot (191)](https://user-images.githubusercontent.com/118671457/229584876-0cdc786b-3ca1-49aa-ac2e-da961bbcce9f.png)
HEAT MAP:
![Screenshot (192)](https://user-images.githubusercontent.com/118671457/229584892-894ac220-279a-4e62-a651-a74c8788c2a8.png)

## RESULT:

Thus the Bivariate and Multivariate analysis is observerd for the given data set.
