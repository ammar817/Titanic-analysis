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
#visualizing count of survival wrt pclass
import seaborn as sns
sns.countplot(x=data['Pclass'], hue=data['Survived'])
#visualizing count of survival wrt gender
import seaborn as sns
sns.countplot(x=data['Sex'], hue=data['Survived'])
#survival rate by sex
df.group('sex')[['Survived']].mean()
#conclusion
females survived more then males 
