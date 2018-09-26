
# Explore Weather Trends

In this project, I analyze local and global temperature data and compare the temperature trends of Pune, India to overall global temperature trends.

##### Gathering Data:

Using an SQL databast hosted on Udacity's server, I extracted data on global temperature average per year, and Pune city's temperature average per year.

The queries used to get the data were:

To get Pune city's data:

`
SELECT year, avg_temp
	FROM city_data
    WHERE city = 'Pune'
`

To get global average data:

`
SELECT *
	FROM global_data 
`

Observations and Trends in the data can be found in the [`Exploring Weather Trends`](https://github.com/ParthThakur/Exploring-Weather-Trends/blob/master/Explore%20Weather%20Trends.ipynb) jupyter notebook.
