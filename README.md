# Pandas Cheat Sheet for Developers

This cheat sheet contains the **most commonly used pandas methods** that every developer uses daily for data exploration, cleaning, transformation, and saving.

---

## 🔹 1. DataFrame Creation
```python
pd.DataFrame(data)
pd.Series(data)
pd.read_csv("file.csv")
pd.read_excel("file.xlsx")
pd.read_sql(query, conn)
pd.read_json("file.json")
```

---

## 🔹 2. Exploring Data
```python
df.head(n)         # First n rows
df.tail(n)         # Last n rows
df.info()          # Summary of DataFrame
df.describe()      # Statistical summary
df.shape           # (rows, columns)
df.dtypes          # Data types
df.columns         # Column names
df.index           # Row index
df.isnull().sum()  # Count missing values
```

---

## 🔹 3. Selection & Filtering
```python
df['col']                     # Select column
df[['col1','col2']]           # Select multiple columns
df.loc[rows, cols]            # Label-based selection
df.iloc[rows, cols]           # Index-based selection
df.query("Age > 25 & Gender == 'M'")   # SQL-like filtering
```

---

## 🔹 4. Modification
```python
df['new_col'] = df['A'] + df['B']         # Add new column
df.drop(columns=['col'])                  # Drop column
df.drop(index=[0,1])                      # Drop rows
df.rename(columns={'old':'new'})          # Rename columns
df.astype({"col": int})                   # Change datatype
df.fillna(value)                          # Fill missing values
df.dropna()                               # Drop rows with missing values
```

---

## 🔹 5. Aggregation & Stats
```python
df.sum(), df.mean(), df.median(), df.std()
df.min(), df.max()
df.value_counts()      # Frequency count
df.nunique()           # Unique values count
df.groupby('col').agg({'x':'mean','y':'sum'})
df.pivot_table(values='x', index='y', columns='z')
```

---

## 🔹 6. Sorting & Ordering
```python
df.sort_values(by='col', ascending=True)
df.sort_index()
```

---

## 🔹 7. Merging & Joining
```python
pd.concat([df1, df2])
pd.merge(df1, df2, on='key')
df.join(df2, on='key')
```

---

## 🔹 8. Exporting / Saving
```python
df.to_csv("file.csv", index=False)
df.to_excel("file.xlsx", index=False)
df.to_json("file.json")
df.to_sql("table", conn)
```

---

## 🔹 9. Utility & Transformations
```python
df.apply(func)               # Apply function to rows/cols
df.applymap(func)            # Apply element-wise function
df.map(func)                 # Apply function to Series
df.replace({old:new})        # Replace values
df.duplicated()              # Check duplicates
df.drop_duplicates()         # Remove duplicates
```

---

## 🔹 10. Visualization (Quick Plots)
```python
df['col'].plot(kind='hist')
df.plot(kind='scatter', x='col1', y='col2')
```

👉 For advanced plots, use **Matplotlib, Seaborn, or Plotly**.

---

## Quick Tips
- For **exploration** → `head()`, `info()`, `describe()`, `value_counts()`  
- For **cleaning** → `dropna()`, `fillna()`, `astype()`, `drop_duplicates()`  
- For **analysis** → `groupby()`, `agg()`, `pivot_table()`  
- For **saving** → `to_csv()`, `to_excel()`  

---

✨ Keep this handy as your **go-to pandas reference** 🚀
