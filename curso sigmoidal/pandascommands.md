https://towardsdatascience.com/a-quick-introduction-to-the-pandas-python-library-f1b678f34673

WORKING WITH PANDAS

LOADING AND SAVING DATA

pd.read_filetype( )

pd.read_csv('https://....')

pd.DataFrame( )

df.to_filetype(filename)   => to save a data frame you're working on

type (df) = what variable it is



VIEWING AND INSPECTING DATA

df.columns = returns the name of the columns

df.dtypes = returns the type of variables

df.index

df.T

df.head( ) => get the first n rows

df.shape  => give you the numbers of rows and columns

df.info( ) => give you the index, datatype and memory information

s.value_counts(dropna=False) => allow you to view unique values and counts for a series

df.describe( ) => inputs summary statistics for numerical columns

​	df.mean(  ) = returns de mean of all columns

​				df.high.mean( )

​	df.corr(  ) = returns de correlation between columns in a data frame

​	df.count( ) = returns the number of non-null values in each data frame column

​	df.max( ) = returns the highest value in each column

​	df.min( ) = returns the lowest value in each column

​	df.median( ) = returns the median of each column

​	df.std( ) = returns the standard deviation of each column



SELECTION OF DATA

df [col]  =>  df ['column name']

df [col1, col2]

s.iloc [0] = select by position

s.loc ['index_one'] = select by position

df.iloc [0, :] = select the first row 

df.iloc [0,0] = select the first element of the first column



FILTER, SORT AND GROUPBY

df [ df  [year ]  > 1984 ]

df. sort_values (col1) = to sort values in a certain column in an ascending order

df.sort_values (col2, ascending=False)

df.sort_values ( [col1, col2], ascending=[True, False])

df.groupby (col) = returns a groupby object for values from on column

df.groupby ([col1, col2]) = retuns a groupby object for values from multiple columns



DATA CLEANING

pd.isnull ( )  = check for missing values

pd.isnull( ).sum( ).pd.notnull( ) is the opposite of pd.isnull( )

df.dropna( )  = to drop the rows

df2 = df.drop('columnx', axis=1) = elimino a coluna 'columnx'

df.dropna(axis=1)  = to drop the columns

df.fillna(x)  = fills the missing values with x

s.fillna (s.mean ( ))  = to replace all null values with the mean

s.replace (1, 'one')  = to replace all values equal to 1 with 'one'

s.replace ([1,3], ['one', 'three'])   = to replace all 1 with 'one' and 3 with 'three'

df.rename (columns={'old _name': 'new_name'}) or use

df.set_index ('column_one')   = to change the index of the data frame



JOIN / COMBINE

df1.append (df2)  = add the rows in df1 to the end of df2 (columns should be identical)

df.concat ([df1, df2], axis=1)  = add the columns in df1 to the end of df2 (rows shoud be identical)

df1.join (df2, on=col1, how='inner')  = SQL-style join the columns in df1 with the columns on df2

where the rows for col have identical values. How can be equal to one of: 'left', 'right', 'outer', 

'inner'.

DATETIME

df.Date

df.Date = pd.to_datetime(df.Date, format = '%Y - %m - %d ')

df.Date.dt.year

df.Date.dt.month

df.Date.dt.day

```
df.sort_index(axis=1, ascending=False)
```

```
df.sort_values(by="B")
```

```
df.to_numpy()
```

```
df2.to_numpy()
```

```
df.loc[dates[0]]
```

```
df.loc[:, ["A", "B"]]
```

```
df.loc["20130102":"20130104", ["A", "B"]]
```

```
df.loc["20130102", ["A", "B"]]
```

```
df.iloc[3]
```