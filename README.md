# DataEngineeringZoomcamp-HW
my Data Engineering Zoomcamp homeworks

Queries:

select count(1) from yellow_taxi_data where tpep_pickup_datetime > '2021-01-15' and tpep_pickup_datetime < '2021-01-16'

select tpep_pickup_datetime from yellow_taxi_data order by tip_amount desc limit 1

select DOLocationID, COUNT(DOLocationID) from yellow_taxi_data where PULocationID = 43 and tpep_pickup_datetime > '2021-01-14' and tpep_pickup_datetime < '2021-01-15' group by DOLocationID"order by 2 desc

select PULocationI, DOLocationID, count(1), SUM(total_amount), (SUM(total_amount)/count(1)) as avr from yellow_taxi_data ytd group by PULocationID, DOLocationID" order by avr desc
