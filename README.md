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
![image](https://github.com/user-attachments/assets/204a74cf-e858-40ad-955a-42dbe8e23f06)

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
![image](https://github.com/user-attachments/assets/9df11ea4-bc44-4d7f-a390-2ef27fa6de1a)
