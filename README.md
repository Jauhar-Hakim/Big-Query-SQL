# Big-Query-SQL

Big Query SQL implementation task to finding insight from raw data.

# Citibike Station

```{python}
sample_count = 5
df_citibike_station = client.query('''
SELECT *
FROM bigquery-public-data.new_york_citibike.citibike_stations
LIMIT %d
'''%(sample_count)).to_dataframe()
df_citibike_station
```

# Citibike Trip

```{python}
df_citibike_trips = client.query('''
SELECT *
FROM bigquery-public-data.new_york_citibike.citibike_trips
WHERE start_station_id IS NOT NULL
LIMIT %d
'''%(sample_count)).to_dataframe()
df_citibike_trips
```

