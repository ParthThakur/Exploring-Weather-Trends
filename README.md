
# Explore Weather Trends

In this project, I analyze local and global temperature data and compare the temperature trends of Pune, India to overall global temperature trends.

##### Gathering Data:

Using an SQL databast hosted on Udacity's server, I extracted data on global temperature average per year, and Pune city's temperature average per year.

The queries used to get the data were:

To find nearest city in the database:

```
SELECT city
	FROM city_list
    WHERE country = 'India'
```

To get Pune city's data:

```
SELECT year, avg_temp
	FROM city_data
    WHERE city = 'Pune'
```

To get global average data:

```
SELECT *
	FROM global_data 
```

The data was then downloaded in csv format and stored locally.

##### Preparing Data:

I used python to prepare the data for visualization. In python, using the `pandas` library, manipulating and charting data becomes easy.

As plotting all the datapoints in one graph whould make the graph very jittery, a 10 year moving average is calculated. Pandas has the rolling class which can be used to calculate rolling statistics on a dataset.

The rolling mean is claculated as:
```
pandas.Series.rolling(window).mean()
```

##### Design:

As we have time data, the best type of visualization is a line chart. Trends are very apparent in such a chart.

The global average has a range of 7&#2816C to 10&#2816C

Observations and Trends in the data can be found in the [`Exploring Weather Trends`](https://github.com/ParthThakur/Exploring-Weather-Trends/blob/master/Explore%20Weather%20Trends.ipynb) jupyter notebook.
