
## Statistical Models for Electric Load and Electric Price Prediction for 5 Spanish cities.



**Introduction**

The rapid shift to an electrical infrastructure based on renewable
sources in Spain is one of the areas where statistical analysis has the
biggest leverage contribution. Data for Spain’s four years (2015-18) of
electricity use, generation, price, and weather are included in this
dataset. A public gateway for Transmission Service Operator (TSO) data
called ENTSOE was used to obtain consumption and generation
statistics. The Spanish TSO Red Electric España provided settlement
pricing. For the five major cities in Spain (Valencia, Madrid, Bilbao,
Barcelona, Seville), weather information was obtained from the Open
Weather API as part of a personal initiative and compiled into two
datasets. Here I used both of them which is also available in Kaggle.


**Data**

From the Kaggle dataset we got 2 csv files containing weather info and
electric data on 5 cities. So, after

1. Inner merging both tables
2. Removing 7 null columns
3. Combining redundant columns

I got data of 3 7 columns(attributes) with 178396 rows (parameters).

But these columns had following null values.

generation biomass 95

generation fossil brown coal/lignite 90

generation fossil gas 90

generation fossil hard coal 90

generation fossil oil 95

generation hydro pumped storage consumption 95

generation hydro run-of-river and poundage 95

generation hydro water reservoir 90

generation nuclear 85

generation other 90

generation other renewable 90

generation solar 90

generation waste 95

total load actual 180

generation wind 90

So, I filled them with their median values.


**Distribution of Data**

```
Fig: Histogram representation of all
numeric columns in the dataset.
```

**Dataset boxplots – To identify outliers and distribution**









**Correlation Plot:**

**Hourly Price of electricity with its weekly rolling mean**


**Statistics Analysis of all attributes:**


**Analysis: Simple Linear Regression**

So, I perform Ordinary Least Squares regression on actual

electricity price with dataset’s forecast price, but the results

were not much satisfactory.


Then, I did Ordinary Least Squares regression on actual

electricity price with dataset’s electric load


So, with
unsatisfactory
results, I grouped
this dataset by the
cities, and then
performed multiple
linear regression on
it.







**Statistical Analysis: Multiple Linear Regression**

Load Prediction Visualization and Parameters for Valencia

```
Mean Absolute Error:
1052.902664716613
```
```
Mean Square Error:
1953354.8347548505
```
```
Root Mean Square
Error:
1397.6247117001226
```

Price Prediction Visualization and Parameters for Valencia

```
Mean Absolute Error:
8.230964392297272
```
```
Mean Square Error:
115.1089008793 654
```
```
Root Mean Square
Error:
10.72888162295425
```

Load Prediction Visualization and Parameters for Madrid

```
Mean Absolute Error:
1067.3986 43815028
```
```
Mean Square Error:
1833561.0212909752
```
```
Root Mean Square Error:
1354.0904775128488
```

Price Prediction Visualization and Parameters for Madrid

```
Mean Absolute Error:
8.310743562696842
```
```
Mean Square Error:
117.06963239502228
```
```
Root Mean Square
Error:
10.819872106222988
```

Load Prediction Visualization and Parameters for Bilbao

```
Mean Absolute Error:
1052.883956648994
```
```
Mean Square Error:
1760538.623695371
```
```
Root Mean Square Error:
1326.8529020563549
```

Price Prediction Visualization and Parameters for Bilbao

```
Mean Absolute Error:
8.186147227315615
```
```
Mean Square Error:
111.90468597854891
```
```
Root Mean Square
Error:
10.57850112154595
```

Load Prediction Visualization and Parameters for Barcelona

```
Mean Absolute Error:
8.230964392297272
```
```
Mean Square Error:
115.1089008793 654
```
```
Root Mean Square Error:
10.72888162295425
```

Price Prediction Visualization and Parameters for Barcelona

```
Mean Absolute Error:
8.310743562 696842
```
```
Mean Square Error:
117.06963239502228
```
```
Root Mean Square
Error:
10.819872106222988
```

Load Prediction Visualization and Parameters for Seville

```
Mean Absolute Error:
1054.1179983221664
```
```
Mean Square Error:
1791182.334841933
```
```
Root Mean Square Error:
1338.3506023617028
```

Price Prediction Visualization and Parameters for Seville

```
Mean Absolute Error:
8.38514986264404
```
```
Mean Square Error:
117.95103877590937
```
```
Root Mean Square
Error:
10.860526634372265
```

