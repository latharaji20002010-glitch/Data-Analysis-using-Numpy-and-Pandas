# Data-Analysis-using-Numpy-and-Pandas
This repository contains a comprehensive Jupyter Notebook demonstrating foundational concepts and practice tasks for data manipulation using **NumPy** and **Pandas**. It serves as a practical reference for array calculations, data exploration, indexing, slicing, and DataFrame modifications.

## 🚀 Key Learning Modules

### 1. NumPy Array Operations
* **1D & 2D Arrays:** Declaring and inspecting structural features (shape, data types, and dimensions).
* **Vectorized Math:** Broadcasting expressions to execute conversions over entire arrays simultaneously (e.g., Celsius to Fahrenheit formulas).
* **Statistical Methods:** Extracting metrics like `max()`, `min()`, and `mean()`.
* **Multi-dimensional Slicing:** Dynamic rows and elements subset selection.

### 2. Pandas Series Operations
* **Custom Indexing:** Initializing explicit labels for localized data rows.
* **Advanced Accessors:** Querying entries utilizing positional index arrays (`.iloc`) alongside programmatic labels (`.loc`).
* **Logical Filtering:** Leveraging boolean masks to dynamically capture target rows.
* **Mutable Modifiers:** Dropping indexes and mutating existing data points dynamically.

### 3. Pandas DataFrame Wrangling
* **DataFrame Construction:** Instantiating rows and columns from native dictionary mapping.
* **Descriptive Auditing:** Running diagnostic structural calls like `.head()`, `.tail()`, `.shape`, and `.info()`.
* **Categorical Summaries:** Utilizing aggregation expressions such as `.value_counts()`, `.unique()`, and `.groupby()` averages.
* **Data Cleansing:** Adding calculated discount features, dropping row-wise elements safely by dynamic index lookups, and removing obsolete columns.

## 📋 Code Snippets Showcase

### Dynamic Conditional Row Deletion
Instead of hardcoding index values, the notebook implements row deletion safely by targeting specific conditional values inside column attributes:
```python
# Drops rows by locating their matching column identifier index dynamically
transactions = transactions.drop(transactions[transactions['TransactionID'] == 109].index)
```

### Multi-Criteria Row Filtering
Combining logical expressions using explicit bracket encapsulation to safely avoid system evaluation errors:
```python
filtered_df = transactions[(transactions['Region'] == 'North') & (transactions['Amount'] > 200)]
```
