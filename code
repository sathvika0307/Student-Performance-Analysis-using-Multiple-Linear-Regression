import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import r2_score, mean_absolute_error

# Load and inspect data
df = pd.read_csv("D:\Documents\CBP's\Batch_6(22071A1073,81,B4,B5)\Student_Performance.csv")
df.head()
df.info()

# Convert categorical column
df['Extracurricular Activities'] = df['Extracurricular Activities'].replace({'Yes': 1, 'No': 0}).astype(int)
df.info()

# Visualize relationships
fig, axes = plt.subplots(3, 2, figsize=(20, 15))
axes = axes.flatten()
for i, column in enumerate(df.columns[:-1]):
    ax = axes[i]
    ax.scatter(df[column], df[df.columns[-1]])
    ax.set_xlabel(column)
    ax.set_ylabel('Performance Index')
plt.tight_layout()
plt.show()

# Correlation heatmap
sns.heatmap(df.corr(), annot=True)

# Filter columns with correlation > 0.2 with target
target_col = df.columns[-1]
corr = df.corr()[target_col].abs()
high_corr_cols = corr[corr > 0.2].index
new_df = df[high_corr_cols]
new_df.info()

# Split features and target
x = new_df.iloc[:, :-1]
y = new_df.iloc[:, -1]

# Scaling and split
scale = MinMaxScaler().fit(x)
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.3)
x_train = scale.transform(x_train)
x_test = scale.transform(x_test)

# Model training and evaluation
model = LinearRegression()
model.fit(x_train, y_train)
predictions = model.predict(x_test)

print("R2 Score : ",end="")
print(r2_score(y_test,predictions))
print("Mean Absolute Error : ",end="")
print(mean_absolute_error(y_test,predictions))
