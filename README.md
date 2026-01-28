# Predicting Traffic

OBJECTIVE: 
	This project aims to analyze and forecast traffic congestion in the Atlanta metropolitan area using high-resolution vehicle trajectory data, including GPS location, speed, and acceleration. By examining driving behavior across time and space, the study seeks to identify congestion causes, pinpoint problem areas, and support data-driven traffic optimization and intelligent transportation planning.

Goals:

-- Examine driver behavior patterns, including acceleration, speed, and frequency of braking, to determine how these behaviors vary in high- and low-traffic areas.

-- Create simple predictive models using previous data to forecast future traffic volumes based on location, time of day, and normal vehicle behavior.

-- Using trajectory data analysis, pinpoint Atlanta's high-congestion areas and peak travel times to help illustrate the locations and times of traffic bottlenecks.

-- Create a foundation for future research or real-world applications in smart transportation systems, urban planning, or traffic predictions.

## Data-Overview::

This project uses the **Next Generation Simulation (NGSIM) dataset**, which provides high-resolution vehicle trajectory data for the Atlanta metropolitan area, including GPS location, speed, acceleration, and driving behavior over time. The dataset was used to analyze traffic flow across time and space, identify congestion hotspots, and understand driving inefficiencies. These insights support the development of predictive traffic models and data-driven strategies for urban traffic optimization and intelligent transportation systems.

## Clean and Preprocessed Data:
<img width="425" height="227" alt="image" src="https://github.com/user-attachments/assets/6e560125-6a46-49e4-bba6-b84e16fb6ebf" />
<img width="514" height="305" alt="image" src="https://github.com/user-attachments/assets/1a236a0e-a2a6-4d59-85f9-66c3562a811b" />

The foundation of this study is this combined dataset, which enables us to investigate the relationships between dynamic vehicle behavior over time and overall trip results as well as congestion trends in various Atlanta neighborhoods.

## Regression Results and Analysis
<img width="618" height="342" alt="image" src="https://github.com/user-attachments/assets/8a028cf4-9769-44e0-b5d4-5c9158336f8e" />


Higher speeds reduce trip duration, with each 1 km/h increase lowering travel time by about 6.26 seconds. Increased acceleration lengthens trips, adding roughly 12.4 seconds per 1 m/s², likely reflecting stop-and-go traffic. Distance has the strongest effect, with each additional kilometer increasing duration by about 193.4 seconds. Spatial factors show smaller impacts: trips further north tend to be shorter, westward travel slightly reduces duration, and direction of travel has a minimal positive effect.

## Visualizations
<img width="721" height="547" alt="image" src="https://github.com/user-attachments/assets/1c8b8a81-f847-4e5f-9e20-62bc1a7fa040" />

<img width="721" height="547" alt="image" src="https://github.com/user-attachments/assets/661b63de-024d-421c-b4b4-9a6ceff0cb9b" />

## Assumptions

** Vehicle trajectory data accurately represents real-world driving behavior across Atlanta neighborhoods.

** Trip duration is primarily influenced by speed, acceleration patterns, distance, and spatial location.

** Stop-and-go behavior (higher acceleration variability) reflects congestion rather than driver preference.

** External factors such as weather, incidents, and special events are assumed to have a limited or uniform impact across trips.
Recommendations

Improve traffic flow consistency: Strategies that reduce frequent acceleration and deceleration (e.g., adaptive signal timing) may lower trip durations.

Target congestion hotspots: Focus infrastructure and policy interventions on areas associated with longer trips and high variability in distance–duration relationships.

Support speed management: Maintaining steady, safe speeds can improve trip efficiency without increasing congestion.

Enhance predictive traffic systems: Use trajectory-based models to forecast congestion and support real-time traffic management and urban planning decisions.
Duration_seconds, the target variable for regression modeling and performance analysis,
