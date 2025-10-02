# python-1
import pandas as pd
import matplotlib.pyplot as plt

data = {
    'Month': ['07/2019', '08/2019', '09/2019', '10/2019', '11/2019', '12/2019'],
    'Searches': [120, 135, 150, 160, 170, 180],
    'Direct': [80, 85, 90, 95, 100, 105],
    'Social Media': [60, 65, 70, 75, 80, 85]
}

df = pd.DataFrame(data)
df.set_index('Month', inplace=True)
df.plot(kind='bar', figsize=(10,6), color=['blue', 'pink', 'yellow'])
plt.title('Visitors by Web Traffic Sources')
plt.ylabel('Visitors (Thousands)')
plt.xlabel('Month')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
