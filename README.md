# NYC-Trip-Fare-Project
2024-2025 Project FOCS
Loreti-Pegoraro
## Project Description
This project analyzes taxi trip data in New York City, based on a provided dataset. The goal is to complete a series of analyses on the data, including extractions, clustering, and calculations on various attributes.

#Task
1. Extract all trips with trip_distance larger than 50
2. Extract all trips where payment_type is missing
3. For each (PULocationID, DOLocationID) pair, determine the number of trips
4. Save all rows with missing VendorID, passenger_count, store_and_fwd_flag, payment_type in a new dataframe called bad, and remove those rows from the original dataframe.
5. Add a duration column storing how long each trip has taken (use tpep_pickup_datetime, tpep_dropoff_datetime)
6. For each pickup location, determine how many trips have started there.
7. Cluster the pickup time of the day into 30-minute intervals (e.g. from 02:00 to 02:30)
8. For each interval, determine the average number of passengers and the average fare amount.
9. For each payment type and each interval, determine the average fare amount
10. For each payment type, determine the interval when the average fare amount is maximum
11. For each payment type, determine the interval when the overall ratio between the tip and the fare amounts is maximum
12. Find the location with the highest average fare amount
13. Build a new dataframe (called common) where, for each pickup location we keep all trips to the 5 most common destinations (i.e. each pickup location can have different common destinations).
14. On the common dataframe, for each payment type and each interval, determine the average fare amount
15. Compute the difference of the average fare amount computed in the previous point with those computed at point 9.
16. Compute the ratio between the differences computed in the previous point and those computed in point 9. Note: you have to compute a ratio for each pair (payment type, interval).
17. Build chains of trips. Two trips are consecutive in a chain if (a) they have the same VendorID, (b) the pickup location of the second trip is also the dropoff location of the first trip, (c) the 
    pickup time of the second trip is after the dropoff time of the first trip, and (d) the pickup time of the second trip is at most 2 minutes later than the dropoff time of the first trip.

Hint: Add a column chain to the dataset. A chain can have more than two trips.
