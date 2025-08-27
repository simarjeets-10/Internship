# Internship
import  matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
import numpy as np
pd.set_option("display.width",None)
df=pd.read_csv(r"C:\Users\DELL\Downloads\Housing_data.csv")
print(df.head())
df["date"]=pd.to_datetime(df["date"])
df.insert(1,"year",df["date"].dt.year)
df.insert(2,"month",df["date"].dt.month)
#print(df.head())
df.drop(["month","year"], axis=1,inplace=True)
print(df.groupby(df["no_of_crimes"]==0))
df["year"]=df["date"].dt.year
min_price=df.groupby("year")["average_price"]
max_price=df.groupby("year")["average_price"]
print(max_price.max())
print(min_price.min())
print("minimum no. of crimes in an area",df.groupby("area").no_of_crimes.min().sort_values(ascending=True))
# Show the total count of records of each area where average price is less than 100000
price=df[df["average_price"]<100000]
print(price.groupby("area").size())
