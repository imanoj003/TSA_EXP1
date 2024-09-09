
### DEVELOPER NAME: Manoj M
### REG NO:212221240027
# Ex.No: 01A PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data student mean scores.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt


data = {
    'Date': pd.date_range(start='2023-01-01', periods=365, freq='D'),
    'Scores': np.random.randint(50, 100, size=365)
}
df = pd.DataFrame(data)


df.set_index('Date', inplace=True)


monthly_mean = df.resample('M').mean()


yearly_mean = df.resample('Y').mean()

plt.figure(figsize=(10, 6))
plt.plot(monthly_mean, label='Monthly Mean Scores', color='blue')
plt.title('Monthly Mean Student Scores')
plt.xlabel('Month')
plt.ylabel('Scores')
plt.legend()
plt.show()


plt.figure(figsize=(10, 6))
plt.plot(yearly_mean, label='Yearly Mean Scores', color='green')
plt.title('Yearly Mean Student Scores')
plt.xlabel('Year')
plt.ylabel('Scores')
plt.legend()
plt.show()


```










# OUTPUT:
![image](https://github.com/user-attachments/assets/85b2002a-ff0c-46f9-80b9-aec46c2177e1)












# RESULT:
The program have created the python program to Plot a time series data student mean scores.
