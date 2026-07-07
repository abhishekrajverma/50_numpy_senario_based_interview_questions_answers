# 50 Pandas Fresher-Level Scenario-Based Interview Questions

SOO 4 68%

5O Pandas Fresher-Level Scenario- Based

Interview Ques:

ons

@® \_. Reading a CSV 0: You received a sales.csv file from your manager
Question: How do you load it into Pandas?

Answer: import pandas as pd

df = pd. readcsv("sales. csv")

> The readcsv() function reads data from a CSV file

> It returns a DataFrame, which is a 2-dimensional table

with rows and columns

Records

You. want to check whether the data loaded correctly

How do you see the first 5 rows?

Answer : df. head (),

> The head() function shows the first 5 rows by default

> You can pass a number inside head(n) to see first n rows For example:
> df. head(10) will show first 10 rows

1)  

Explanation:

cords

@_ View Las! Scenario: You want to check the last records.

How do you see the last 5 rows?

df. tail ()

-   The toil() function shows the last 5 rows by default You can pass a
    > number inside tail(n) to see last n rows For example: df.tail(10)
    > will show lost 10 rows

@® Find Number of Rows and Columns 5 Your manager asks how big the
dataset is

How do you find the number of rows and columns? df. shape

Explanation: \> The shape attribute returns a tuple (rows, columns) \>
For example, if output is (100, 5), it means the dataset has 100 rows
and 5 columns.

Columns You forgot the column names. How do you List all the columns in
the dataset ? Af. columns \> The columns attribute returns an Index
object containing

all column names \> Tt helps you quickly understand what fields are
available She dataset

------------------------------------------------------------------------

50 Pandas Fresher-Level Scenario-Based

Data Types

Your manager wants to know the data type of each column to understand
the dataset better How do you check the data types of all columns? af,
dtypes on: The dtypes attribute returns the data type of each column

in the DataFrame. helps identify whether a. column is integer Float,
(string), boolean or datetime

is useful before doing calculations or conversions

Scenario want a. quick summary of the dataset including missing values
Question: How do you get a concise summary of the DataFrame? Answer df.
info ()

Explanation: The info() function prints a summary that. includes

> Total number of rows and columns

> Column names

> Non-null count (how many nen-missing values) Data types of each column

> Memory usage

> Te is very helpful for an overview of the dataset

Your manager needs min, max, mean, and other statistics of numeric
columns

tion: How do you get statistical summary of the dataset?

df. describe() The describe fi

> count, mean, std (standard deviation), min, 25%, 50%,

ction returns key statistics for numeric. columns

75th, max

> It helps in understanding the distribution of data One Column You.
> only need the "Employee Name" column for a report How do you select a
> single column from the DataFrame? 4f £" Employee -Name"\] This returns
> the specified column as a Series. A Series is a one-dimensional,
> labeled array.

Select Answer Explanation

Select Multiple Columns. ' seeee You reed the "Emplyte-Nane" and Salary"
cline fr onli Qusstion: How do you select multiple columns from the.
DataFrame? Answer? df CL" Employee Name", Salary"

tion: This returns a new DataFrame with only the selected Explanation:
ne use double brackets to. select ate eo a \> The result is stil a
DataFrame.

7 , I) Krishna Verma O Data Engineer @ Lowe's India \|\| Ex-Airtel
Digital \|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------

50 Pandas Fresher-Level Scenario-Based

Interview Que:

tions

Some employees did not provide their email or phone number

= do you find missing values in each column?

isnull(). sam () ae isnull() function returns a DataFrame of True/ False

indicating missing values. The sum() function then counts the total
number of missing values in each column

> This helps to identify which columns have missing data

and how much is missing

remove all rows that have any missing data a drop rows with missing
values ? df. dropna.()

The dropna() function removes rows that contain NaN

(missing) values

> By default, it removes rows where any column has a missing value (how
> ='any')

> This is useful when you want only complete records

for further analysis

(e) \
    For numerical columns, replace missing values with 0 How do you fill
    missing values with a specific value? df, fillna (0)

planation: The fillna (value) function replaces all NaN values with the
specified value \> Here, 0 is used, so all missing values are replaced
by 0 \> This is helpful when missing values can be treated as zero
(e.g., » Bonus, ete.) Gs) u g Ka)

The column name "EmpName" is not clear. You want to rename it to
"Employee Name"

How do you rename a column?

df. rename (colums = { "Emp_Name": "Employee Name" }, inplace =True) The
rename() function changes column names

> columns = {oldname: newaname} is used to specify the change

> inplace = Die applies the change to the original DataFrame.

| @) Add New Column

Scenario: You. want to add a new column called "Bonus" which is 10% of
the employee's Salar How do you create a new calloe ice 'existing data?
aft Bonus"\] = df \["Salary"\] \* 0.10 a new pluie, "Bor

Explanation

Question: Answer

Ex sities plonattion\> aL h

For

) Krishna Verma 9 \| Data Engineer @ Lowe's India \|\| Ex-Airtel Digital
\|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------

5O Pandas Fresher-Level Scenario- Based

tions

Interview Ques'

Column

The column "Temp" is no longer required in the dataset How do you delete
the "Temp" column from the DataFrame ?

df.drop( Temp', axis=1, inplace = True)

The drop() function removes a row or column

> oxis=1 specifies that we want to drop a column (axis=0 is for rows)

> inplace =True makes the change permanent in. the original DataFrame

> If inplace is not used, a new DataFrame is returned

\~ 4)

@ Filter Rows with Condition You want to find all employees whose salary
is greater than 50,000 How do you filter these records?

Answer df \[dF L"Salary'\] \> 50000\]

Explanation: We use square brackets \[\] to filter rows based on a.
condition \> dFL\*Salary'\] \> 50000 returns a Boolean Series (True/
False) \> Only rows where the condition is True are returned

@ Rows with Conditions Find employees from "IT" department who have
salary greater than 50,000 and age less than 30 How do you filter these
records? df \[ (df L"Department'\] == 'IT') & (dF L"Salary'\] \> 50000)
& (af L"Age'\] \< 30)\] We combine multiple conditions using the &
operator \> Each condition is written inside parentheses () \> All
conditions must be True for a row to be selected @) Sort

ario: You want to display the employees in descending order of salary
Question: How do you sort the DataFrame by "Solary" in descending orde:
? Answer df. sort-values ( 'Salary', ascending = False)

Explanation: The sort---values() function sorts the DataFrame by the
given column \> ascending =False means highest volues will appear first

> By default, ascending = True (smallest first)

Get Top N Records

Scenario: Find the top 5 highest paid employees Question: How do you get
the top 5 records based on salary? Answer: df. .nlargest (5, Salary') \|
Explanation: The nlargest(n, column) function returns the top 'n' rows
with the largest values in the specified column. ---\> It is more
efficient than sorting the entire DataFrame

) Krishna Verma 9 Data Engineer @ Lowe's India \|\| Ex-Airtel Digital
\|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------

50 Pandas Fresher-Level Scenario-Based Interview Questions

Values in a Column

ario: You want to know how many unique departments are there Question:
How do you count unique departments in the dataset? er:
dfL"Department™\]. nunique ()

Explanation: The nunique() function returns the count of unique
(distinct)

values in a column \> Tt ignores duplicate values

> This helps in understanding the variety in the data que Values in a
> Column

You want to see all the departments available in the company

How do you get the unique values from the "Department" column

Explanation: The unique) function returns an array of unique values
present in the specified column \> It shows which departments exist in
the dataset

> Useful for data exploration and validation

s in Each Category

You want to know how many employees are in each department How do you
count the number of employees in each department? AFL" Department"\].
value counts ()

nation: The value---counts() function returns a Series containing the
count

of each unique value in descending order

> Tt shows how many times each department appears

> Hel

ps in analyzing the distribution of employees

Values in ame In the "Gender" column ,

'Male' and 'Female'

"M! and 'F' need to be replaced with

How do you replace values in a column?

dfL"Gender'\] = df\['Gender'\]. replace ({'M': 'Male', 'F': 'Female'})
The replace() function replaces old values with new values \~\> It can
handle one or multiple replacements using a dictionary \> It does not
change other values @ \_\_ Map Values in a Column

Scenario: You want to map department codes to full department names
Codes: IT -\> Information Tetrelogy, Rs stator Rien rl Question: How do
you map values in a column? APL" Dept-Name'J = dfL\*Dept.. Code'\],map({
'IT': 'Information Technology',

HR': "Human Resources'})

The map () function substitutes values based on a given dictions. \> It
is used, for one-to-one

Answer:

Explanation:

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------

5O Pandas Fresher-Level Scenario-Based

Interview Questions

@ Find Maximum Salary Scenario: Your manager wants to know the highest
salary in the company

How do you find the maximum solary from the DataFrame? Answer: df
L"Salary"\].max() Explanation: The max() function returns the largest
value in the specified

column

> Tt scans all the values in 'Salary' and picks the highest one Useful
> for quick insights like top salary offered

Find Minimum Salar:

You need to know the lowest salary paid to any employee

How do you find the minimum salary?

AFL" Salary". min C)

The min() function returns the smallest value in the column

E. tion xplanatio

> Tk helps identify the lowest-paid employee Useful in salary analysis
> and fairness. checks

tment

ar

ry by D

You want to know the average salary for each department

How do you calculate the average salary department-wise ?

dF. groupby ("Department") L Salary'\]. mean )

Answer

Explanation: We use groupby() to group rows ty" Department" and. then
apply mean() on "Salary \> Tk returns the average salary for each
department

> Very useful for department performance comparison

laries by Department

Find the total. salary expense for each department

tion: How do you calculate the total salary paid in each department?

Answer: a#C.groupby ¢" Department" }L" Salary'. sum() Erolonation: The
sum() furction adds all salary values within each department . \> Tk
gives total payroll cost. per department

> Helpful for budgeting ond expense tracking @) Count Employees by
> Department

Scenario: You want to know how many employees work in each department

Guaction: Hew do you count employees in each department?

Answer: FC" Department" J. value counts ()

de E groupby "Department". size)

value---counts() counts how many times each department ce groupey( size)
gives the count of rows in each group

TSU CO Es PRS aT BE Se ine AY

> Useful for workforce distribution analysis.

Explanation:

fl Krishna Verma @

Data Engineer @ Lowe's India \|\| Ex-Airtel Digital \|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------

50 Pandas Fresher-Level Scenario-Based

Int

1)  | Reset

Scenario:

rview Questions

Index After deleting some rows, the index is no longer in order

How do you reset the index of the DoteFrame?

Q

df. reset index (drop = True)

Answer: (0, 4,2,3,.+.) and removes the old index \> drop=True removes
the old index column

> Very useful after filtering or dropping rows

2)  | Convert Data

The How do you convert the "Age" column to integer?

df \["Age"\] = dfL"Age"\] .astypeCint)

Explanation: The astype() method changes the data type of a column

> Here, we convert all values in "Age" to integer

> This helps in doing numeric operations and. calculations

63) 

```{=html}
<!-- -->
```
3)  You received an Excel file named "employees . xlsx How do you read
    it using Pandas ? df = pd. read excel ("employees xlsx") Explanation
    The read---excel() function reads an Excel file and returns a
    DataFrame \> Requires openpyxt library (pip install openpyst) \> You
    can also specify sheet name using sheet-name="Sheett"

4)  | Save Data to File

After cleaning the data, you want to sove it as a CSV file How do you
export the DataFrame t\> a CSV file?

df. to_csv("output.csv", index =False)

The to-csv() function writes the DataFrame to a CSV file

Answer

> index =False prevents writing row index in the file

> The file can be opened in Excel or any text editor

© Sove Data to Excel File You want to save the cleaned data into on
Excel file

Scenario: Question: How do you export the DataFrame to an Excel file?
Answer: df. to-excel ("output xlsx", index =False)

Explanation: The to-excel() function writes the DataFrame to an Excel
file

> index=False prevents index column from being written. Requires
> openpyxl or xlsxuriter library. Useful for sharing reports in. Excel
> format.

) Krishna Verma 9 Data Engineer @ Lowe's India \|\| Ex-Airtel Digital
\|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

The reset_index() function resets the index to the default

'Age" column is stored as text Cobject) but it should. be integer

¥

------------------------------------------------------------------------

50 Pandas Fresher-Level Scenario-Based

Interview Questions

You want to know the average salary for each department

How do you get the average salary department wise?

Answer: df. groupby(" Department") \[" Salary" \]..mean()

Explanation: The groupby() function groups the data by

> Then, mean lates the average of the "Sal

for each

i

> Returns a Series with department names as index and

average salary as values

department Question How do you count employees in each department?
Answer AFL" Department". value ---counts() Explanation: The
value-counts() function counts unique values in the

"Department" column

> Returns department names as index and counts as values

> Helpful for quick headcount reports

Dota by D

enario: You want to view employees sorted by department name and

within each department by highest salary

How do you sort the Data Frame

df, sort ---values(L\* Department", "Salary"\],

ascending =\[True, False\])

We sort first by "Department" in ascending order (Ato Z)

Explanation Exp

> For "Salary", we use False to get highest salary

le sorting helps in organized reporting

est Paid Employees

You need a list of top 10 employees based on salary 10 highest salary
records?

How do you select toy

af nlargest (10, "Solarg") inlargest (n, column) returns the first n
largest values, from

the specified column = Returns the top 10 rows with highest salary "\>
More efficient than sorting the whole Data Frame

@ Select Bottom 10 Lowest Paid Employees You need a list of bottom 10
employees based on salary

Scenario?

Question: How do you select bottom 10 lowest salary records? Answer: df
nsmallest (10, " Salary")

Explanation: namallest Cn, column) returns the First n smallest values
from

the specified column \> Returns the 10 rows with lowest salar

> Useful for identifying underpaid employees or interns.

) Krishna Verma O

Data Engineer @ Lowe's India \|\| Ex-Airtel Digital \|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------

50 Pandas Fresher-Level Scenario-Based

Interview Questions

Remove Di

Rows from DatoFrame

Your dataset contains duplicate rows and you need unique records

Q : How do you remove duplicate rows in Pandas? Answer df. drop
duplicates) Explanation: The drop---duplicates() function removes
duplicate rows

> By default

> Keeps the first occurrence and removes the rest

it considers all columns to identify duplicates

subset of columns and keep='first' or 'last

> You can specify Example: df. drop-duplicates (subset = \["Email'\],
> keep ='last")

This is very useful for cleaning real-world data.

Handle Missing Values by Filling with Mean

Scenario: Some numeric columns have missing values and you want to fil
them with the average 'of that column

es in a column with its mean?

Question: How do you fill missing er df \[ "Column" \]. fillna (dF L

inplace = True )

column" J .mean(

Explanation: The fillna() function replaces NaN values with a specified
value "\> We use mean() for numeric columns.

> inplace=True updates the DataFrame without creating a new copy

> This helps maintain data consistency

You have time-series data with missing values and want to Fill them with
the previous valid value

How do you forward fill missing values?

True)

df FFU Cinplace The \$filL() function propagates the last valid
observation forward \> Ideal for time-series data where next values
depend on previous ones Limit to Fill only a certain number of rows

> You can also specify Backward fill (fill) can be used to use next
> valid value

Columns in DataFi DataFrame has old column names and you want to

Scenario Your va rename them to new meaningful names NEED Question How
do you rename one or more columns? Pascee --- aferename Ceslumns
{"old-name': 'new aname"}, inplace = True)

The rename() function changes column names "\> Use a dictionary to map
old names to new names

"\> inplace=True modifies the original DataFrame

> Helps in better readability and understanding of data

Explanation: Expli

veate a New Column Based on Existing Columns See You want to create a
new ae "Total Salary' by adding Basic Salary' and 'Bonus' columns.
Question: How do you create a new column in Pandas? asi) df L Total
Salary\] = AFC' Basic---Salary'\] + df C°Bonus'\] premnation: We can
ereale new columns using arithmetic operations in \> Pandas performs
element-wise operations on columns S The new column is added to the
DataFrame. \> Useful for feature engineering and date analysis.

Scenario

) Krishna Verma 9 Data Engineer @ Lowe's India \|\| Ex-Airtel Digital
\|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------

50 Pandas Fresher-Level Scenario-Based Interview Questions

Filter Data Between Two Dates

cenario: You have sales data with a 'Date' column and you want data
between ist Jan 2024 and 31st Jan 2024

How do you filter the DataFrame for that date range?

df\[ (df \["Date'\] \>= '2024-01-01') & (dF L"Date'\] \<=
'2024-01-31')\] We use boolean indexing to filter rows where 'Date'
falls within

F Si

the given. range

> Comparisons are inclusive (\>= and \<=)

> Make sure 'Date' column is in datetime format (use pd.to-datetime())
> Very useful for reports and dashboards

a

Add a Percentage Column

Scenario: You have 'Sales' and 'Target' columns and want to add a column
"Achievement %' = (Sales / Target) \* 100. Question: How do you create
this new column?

Answer: df \[ "Achievement %"\] = (df \[\*Sales'\] / df \[ "Target" \])
\* 100 Explanation: We perform element-wise division and multiply by 100
\> Handle division by zero using replace or where if needed \> Round the
result using .round(2) if required "\> Useful for KPI and performance
metrics Pivot Data for Summary Report Scenario: You have sales data with
columns: 'Date', 'Product', 'Region', 'Sales' You want total sales of
each product in each region. Question How do you create a pivot table
for this? Answer: df. pivot table (values= 'Sales', index = 'Product',
columns = 'Region', aggfunc = 'surn') Explanation: pivottable() reshapes
data and aggregates values "\> index becomes rows, columns becomes
columns of the table. \> aggfune defines the aggregation (sum, mean,
count, etc.) \> Great for creating cross-tab reports Find Duplicate
Records Scenario: Your dataset may contain duplicate rows and you want
to identify them Question: How do you find duplicate rows in a
DataFrame? Answe' df \[ df. duplicated (keep = False) \] Explanation:
duplicated) marks duplicate rows \> keep=False shows all duplicates
(first + repeats) \> keep='first' (default) shows only duplicate rows
except first "\> Useful for data quality checks. Export Filtered Data to
Excel Scenas After filtering your data, you want to export it to an
Excel file Question: How do you save the filtered DataFrame to Excel? \|
Answer filtered df. to_excel 'filtered data.xlsx', index=False,
sheet_name="Report' \|

Explanation: toexcel()\_ writes the DataFrame to an Excel file \>
index=False prevents writing row index

These 50 scenario-based questions cover real-world Zip He uses easls
dota toealunt ter igi sb leernpantes Uae tiridas!

) Krishna Verma 9

Data Engineer @ Lowe's India \|\| Ex-Airtel Digital \|\| SQ...

50 Pandas Fresher-Level Scenario-Based Interview Questions for Data
Analytics, Data... more

------------------------------------------------------------------------
