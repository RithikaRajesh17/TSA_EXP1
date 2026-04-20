# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

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

Developed by: Rithika R


Reg.No: 212224240136
```python

from matplotlib import pyplot as plt
import pandas as pd


df = pd.read_csv("/content/POPH.csv")
df.head()

df['date'] = pd.to_datetime(df['date'])

df.set_index('date', inplace=True)

df_resampled = df['value'].resample('D').interpolate()

df_resampled.plot(kind='line', label='Population', color='black')

plt.title('Time Series Plot of Population (Daily Interpolated)')
plt.xlabel('Day')
plt.ylabel('Population')
plt.legend()
plt.grid(True)
plt.show()
```








# OUTPUT:
<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/f6ec77b7-30d2-478e-b71b-b4b18c678d70" />







# RESULT:
Thus we have created the python code for plotting the time series of given data.
