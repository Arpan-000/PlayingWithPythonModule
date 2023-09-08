

---

# Data Visualization with Python

This repository contains Python code for visualizing data using Pandas, Seaborn, and Matplotlib. The code is divided into several sections, each focusing on a specific aspect of data visualization.

## Prerequisites

Before running the code in this repository, make sure you have the following prerequisites installed on your system:

- Python (3.6 or higher)
- Pandas
- Seaborn
- Matplotlib

You can install these libraries using pip:

```bash
pip install pandas seaborn matplotlib
```

## Usage

### 1. Bar Plot of Rank by Branch

The code in this section generates bar plots to visualize the ranks by branch for two different datasets: 'REALANUR.csv' and 'SREYAS1.csv'.

To run this code, use the following commands:

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Read the data
df = pd.read_csv('REALANUR.csv')
df1 = pd.read_csv('SREYAS1.csv')

# Create bar plots
sns.barplot(x='Rank', y='Branch', data=df)
plt.xlabel('Rank')
plt.ylabel('Branch')
plt.title('Bar Plot of Rank by Branch of Anurag group of Institutions(ANRK)')
plt.show()

sns.barplot(x='Rank', y='Branch', data=df1)
plt.xlabel('Rank')
plt.ylabel('Branch')
plt.title('Bar Plot of Rank by Branch of Sreyas institute of engineering and technology(SIET)')
plt.show()
```

### 2. Comparing Closing Ranks

This section compares the closing ranks of two institutions, ANRK and SIET, using a bar plot with different colors.

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Create a bar plot to compare closing ranks
ax = plt.subplot()
ax = sns.barplot(x=df["Rank"], y=df["Branch"], color="b")
ax = sns.barplot(x=df1["Rank"], y=df1["Branch"], color="g")
ax.set(xlabel="Rank", ylabel="Branch")
plt.title('Bar Plot comparing closing ranks of SIET and ANRK. Green = SIET, Blue = ANRK')
plt.show()
```

### 3. Line Plot of Rank vs. Branch

This section creates a line plot of rank vs. branch for the dataset 'SREYAS1.csv'.

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Create a line plot
sns.lineplot(x="Rank", y="Branch", data=df1)
plt.show()
```

### 4. Count Plot of Gender

These sections create count plots to visualize the distribution of genders in the datasets.

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Create a count plot for gender distribution in df
plot = sns.countplot(x="Sex", data=df)
plt.show()

# Create a count plot for gender distribution in df1
plot = sns.countplot(x="Sex", data=df1)
plt.show()
```

## License

This code is provided under the [MIT License](LICENSE).

---

Feel free to modify this template to provide more detailed information or add any other relevant sections to your README file.
