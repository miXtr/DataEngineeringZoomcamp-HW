# DataEngineeringZoomcamp-HW
my Data Engineering Zoomcamp homeworks

Queries:

PGCLI:
select count(1) from yellow_taxi_data where tpep_pickup_datetime > '2021-01-15' and tpep_pickup_datetime < '2021-01-16'
select tpep_pickup_datetime from yellow_taxi_data order by tip_amount desc limit 1

DBeaver:
select ytd."DOLocationID", COUNT(ytd."DOLocationID") from yellow_taxi_data ytd where ytd."PULocationID" = 43 and ytd.tpep_pickup_datetime > '2021-01-14' and ytd.tpep_pickup_datetime < '2021-01-15' group by ytd."DOLocationID" order by 2 desc
select ytd."PULocationID", ytd."DOLocationID", count(1), SUM(total_amount), (SUM(total_amount)/count(1)) as avr from yellow_taxi_data ytd group by ytd."PULocationID", ytd."DOLocationID" order by avr desc
