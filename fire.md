
# Team Entrepreneur

---

# Exploratory Data Analysis on Fire Dataset

## About the Dataset

- Data is taken from [Fao website](https://www.fao.org/faostat/en/#data/GI). All countries available were selected and Year: 1990 to 2019.

## Steps performed

## 1. Import Libraries

- Import necessary libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

## 2. Import dataset

- Import dataset and check dataset

```python
df= pd.read_csv('fires_data_11-29-2021.csv')
df.head()
```

## 3. Shape of dataset

- Check Shape of data

```python
row, cols= df.shape
print("Number of rows:", row)
print("Number of columns:", cols)
```
Dataset has 47649 rows and 17 columns

## 4. Check data types

- Check data types of each column

```python
df.dtypes
```

## 5. Check missing values

- Check missing values in each column

```python
df.isnull().sum()
```

- Only one column (Note) has missing values

## 6. Dropping unnecessary columns

- Drop unnecessary columns and making changes in the dataset

```python
df.drop(['Note','Domain Code','Element Code','Item Code','Flag Description','Flag','Source Code'], axis=1, inplace=True)
```

## 7. Data Structure of dataset

- Check data structure of dataset

```python
df.info()
```

- Data has RangeIndex: 47649 entries, starting from 0 to 47648

- Data has total 10 columns

- dtypes of columns are one float64, two int64 and seven object

- Memory usage of the data is 3.6 MB

## 8. Summery of dataset

- Summery of dataset

```python
df.describe()
```

## 9. Unique values in each column

- Unique values in each column

```python
df.nunique()
```

- 238 Countries
- 30 Years
- 7 Items