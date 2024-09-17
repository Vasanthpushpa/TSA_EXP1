# Ex.No: 01A PLOT A TIME SERIES DATA
# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
## PROGRAM DEVELOPED BY: VASANTH P
## REG NO: 212222240113

## PROGRAM:

```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df_filtered = df["2000":"2023"]
annual_mean = df_filtered.resample('Y').mean()
mean = annual_mean.plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population (in Thousands)")
plt.title("Average Annual Population (2000-2023)")
plt.show()
```
## MARKET PRICE:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
## TEMPERATURE:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```
## OUTPUT:
## POPULATION:

![pop](https://github.com/LokeshRajamani/TSA_EXP1/assets/120544804/5fe0a8f5-4301-451d-8129-d471a27595a4)

## MARKET PRICE:

![mark](https://github.com/LokeshRajamani/TSA_EXP1/assets/120544804/b24416ed-1054-442d-a20f-dd8aa6a19580)

## TEMPERATURE:

![temp](https://github.com/LokeshRajamani/TSA_EXP1/assets/120544804/c069ffc5-3b71-4226-808a-1481d6358813)





# RESULT:
Thus we have created the python code for plotting the time series of given data.
