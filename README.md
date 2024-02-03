# python-api-challenge
Module 6 Challenge Repo


Resources:

Help getting gridlines onto my scatter plot. If I understand corectly, I messed up the plt.grid functionality by trying out plt.grid=true in the notebook beforehand... which I admit I tried!

https://stackoverflow.com/questions/67378630/getting-error-while-using-grid-method-in-python

Xpert Learning Assistant help with date-time format so I could add it as desired to scatter plot title:

Student User Logo
convert unix UTC timecode to year-month-date format in a pandas dataframe
Xpert User Logo

To convert a column of Unix UTC timecodes in a Pandas DataFrame to the year-month-date format, you can use the pd.to_datetime() function and the .dt accessor. Here's an example:

import pandas as pd

# Assuming you have a DataFrame with a column of Unix UTC timecodes
df = pd.DataFrame({'unix_time': [1635724800, 1635811200, 1635897600]})

# Convert the Unix time column to datetime format
df['datetime'] = pd.to_datetime(df['unix_time'], unit='s')

# Extract the year, month, and date components
df['year'] = df['datetime'].dt.year
df['month'] = df['datetime'].dt.month
df['day'] = df['datetime'].dt.day

# Format the date in year-month-date format
df['formatted_date'] = df['datetime'].dt.strftime('%Y-%m-%d')

print(df)


In the example above, we assume that you have a DataFrame df with a column named 'unix_time' containing Unix UTC timecodes. We use the pd.to_datetime() function to convert the Unix time column to datetime format. The unit='s' argument specifies that the Unix timecodes are in seconds. Then, we use the .dt accessor to access the datetime properties of the column and extract the year, month, and date components into separate columns ('year', 'month', and 'day'). Finally, we use the .dt.strftime() method to format the date in the desired year-month-date format and store it in a new column named 'formatted_date'.

Please note that the column name and DataFrame variable in your case might be different, so make sure to replace them with your actual column name and DataFrame.

