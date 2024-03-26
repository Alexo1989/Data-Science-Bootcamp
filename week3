import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from Ipython.core.interactiveshell import interactiveshell
InteractiveShell.ast_node_interactivity = "all"
url= 'https://data.cityofnewyork.us/api/views/6fi9-q3ta/rows.csv?accessType=DOWNLOAD'
df =pd.read_csv(url)

data['date'] = pd.to_datetime(data['date'])

data_weekdays = data[data['date'].dt.dayofweek < 5]

daily_pedestrian_counts = data_weekdays.groupby(data_weekdays['date'].dt.dayofweek)['pedestrian_count'].mean()

# Map day of the week to its name
days_of_week = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday']

# Plotting the line graph
plt.figure(figsize=(10, 6))
plt.plot(days_of_week, daily_pedestrian_counts, marker='o', linestyle='-')
plt.title('Pedestrian Counts for Each Day of the Week')
plt.xlabel('Day of the Week')
plt.ylabel('Pedestrian Count')
plt.grid(True)
plt.show()
