# Predicting-Traffic


Project topic:
        The objective of this project is to investigate, model, and forecast traffic congestion patterns throughout the Atlanta metropolitan region by utilizing high-resolution vehicle trajectory data. GPS locations, vehicle speed, acceleration, and driving patterns over time are all included in the data. We hope to gain a deeper understanding of the fundamental reasons behind traffic jams and driving inefficiencies by looking at these dynamic variables in relation to time and space.
The increasing demand for intelligent transportation systems and urban traffic optimization is what motivates this study. Traffic congestion is becoming a bigger problem for commuters, planners, and legislators as Atlanta's population continues to grow and car usage increases. Our research offers a data-driven framework for determining trouble spots, assessing how drivers behave, and creating prediction models that estimate the volume of traffic.


Goals:
Examine driver behavior patterns, including acceleration, speed, and frequency of braking, to determine how these behaviors vary in high- and low-traffic areas.
Create simple predictive models using previous data to forecast future traffic volumes based on location, time of day, and normal vehicle behavior.
Using trajectory data analysis, pinpoint Atlanta's high-congestion areas and peak travel times to help illustrate the locations and times of traffic bottlenecks.
Create a foundation for future research or real-world applications in smart transportation systems, urban planning, or traffic predictions.
Data Overview:
To support our analysis and modeling of traffic patterns and driver behavior in the Atlanta metropolitan area, we utilized two primary datasets:
We used two main datasets to assist in our research and modeling of traffic patterns and driver behavior in the Atlanta metropolitan area:
1. Summary_to_publish.csv
High-level data regarding each driver's individual journeys is provided by this dataset. The following essential characteristics are included in each row, which represents a single trip:
trip_id: A special number assigned to every journey
driver_id: The driver's anonymized ID
city: The city in which the journey took place (filtered for Atlanta)
duration_seconds, our target variable, is the total trip duration in seconds.
Depending on the source, other performance indicators could include average speed, total distance, and other summary information.
We utilize this dataset as labels in our predictive algorithms to better understand the overall scope and outcome of each journey.
2. Trajectories_to_publish.csv.
This dataset includes comprehensive time-series data that records every trip's driving behavior second by second. One second of a journey is represented by each entry, which contains:
velocity: The car's current speed, usually measured in meters per second.
acceleration_mss: The square of the acceleration in meters per second
latitude and longitude: the vehicle's GPS coordinates
trip_id: This information is connected to the summary dataset.
Because it enables a detailed examination of driving dynamics and behavior, this trajectory data is essential for assessing traffic flow, spotting stop-and-go patterns, and computing performance indicators like average speed or driving consistency.
Merging Data:
We combined the two datasets using the trip_id key to get a single dataset fit for modeling and analysis. This made it possible for us to match the trip summary and target value (travel length) with each driving record, second by second.
A total of about 14,000 rows of records, reflecting multiple drivers' travels in multiple cities. A selection of the most informative features remained after the data was cleaned and preprocessed, including filtering for the Atlanta region, addressing missing or corrupted information, and standardizing units.
Atlanta-specific filter: For our research, only journeys inside the Atlanta area were kept.
Completed Feature Set:
speed (m/s)
velocity_mss (m/s2)
distance_metres (included or derived)
latitude and longitude (for mapping spatially)
bearing (movement direction)
Duration_seconds, the target variable for regression modeling and performance analysis,
