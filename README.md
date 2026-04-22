# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 25/04/2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
   
# PROGRAM:
```py
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("apple.csv")
df['Date'] = pd.to_datetime(df['Date'])
monthly_volume = df.set_index('Date')['Volume'].resample('ME').sum()
plt.figure(figsize=(12, 6))
plt.plot(monthly_volume.index, monthly_volume.values, marker='o', linestyle='-')
plt.title('Yearly Volume Changes')
plt.xlabel('Date')
plt.ylabel('Volume')
plt.grid(True)
plt.show()
```
# OUTPUT:
<img width="1253" height="629" alt="image" src="https://github.com/user-attachments/assets/ccf761a2-ffbf-4fcb-9e78-e243ff1bc619" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
