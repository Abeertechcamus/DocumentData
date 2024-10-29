# DocumentData

This dashboard was built using this dataset [Ordersdataset](Orders.csv).

**Data:**
The file appears to contain 20,008 rows and 19 columns

**Data Cleaning :**
Python (pandas)

**Data Visualization**
PowerBI

## overview
Here’s an overview of the data structure:
- Row 3 (index 2) has the actual header labels.
- Columns contain various details such as order date, country, city, product category, quantity, unit price, discount, and status.
- Issues include extra headers, missing values, and a lack of consistent column names.

# clean the data
 I’ll clean the data by setting the correct headers, removing empty rows, and renaming columns for clarity.

 It includes headers spread across multiple rows, and many columns are labeled "Unnamed.

### correct headers
```
<!-- setting the correct headers for clarity by adding skiprows -->
import pandas as pd
df=pd.read_csv(r'Orders.csv', skiprows=4)
df
```

### Drop any completely empty rows

```
df.dropna(how='all', inplace=True)

```


### Display City names to capital titile where applicable
```
df['City']=df['City'].str.title()
```

### Remove "Tel:" from phone numbers and strip extra spaces
```
df['Phone Number']=df['Phone Number'].str.replace('Tel:','')
```
### Display a summary of the cleaned data
```
df.head(), df.info()
```


To view the dashboard enter this link  [employee dashboard](employee_dashboard.pdf).

