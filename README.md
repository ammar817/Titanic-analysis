# Titanic-analysis
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("tested.csv")
data.head()
x = data["Age"]
y = data["Survived"]
plt.scatter(x, y)
plt.savefig("scatter.png")
plt.show()
#if i want to check that the values are null or not
data.isnull().sum()
#by applying all the function
data.shape
data.describe()
# if i want to check that how many survived
data['Survived'].value_counts()


