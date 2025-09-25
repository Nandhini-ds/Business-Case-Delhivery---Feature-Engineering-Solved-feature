# Business-Case-Delhivery---Feature-Engineering

## About Delhivery
Delhivery is the largest and fastest-growing fully integrated player in India by revenue in Fiscal 2021. They aim to build the operating system for commerce, through a combination of world-class infrastructure, logistics operations of the highest quality, and cutting-edge engineering and technology capabilities.

The Data team builds intelligence and capabilities using this data that helps them to widen the gap between the quality, efficiency, and profitability of their business versus their competitors.

## How can you help here?
The company wants to understand and process the data coming out of data engineering pipelines:

• Clean, sanitize and manipulate data to get useful features out of raw fields

• Make sense out of the raw data and help the data science team to build forecasting models on it

## Tools Used 
* Python and
* Python Libraries and stats module.
  
## Project type 
* Data Cleaning and Preprocessing
* Handling Missing Values
* Column Standardization using MinMaxScaler
* Feature Engineering
* Encoding
* Performing Hypothesis Testing

## About Data 
**Dataset Link**: https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/551/original/delhivery_data.csv?1642751181

| Column                     | Description                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------|
| data                       | Indicates whether the row is part of testing or training data                                  |
| trip_creation_time          | Timestamp of trip creation                                                                     |
| route_schedule_uuid         | Unique ID for a particular route schedule                                                     |
| route_type                  | Transportation type                                                                            |
| FTL                        | Full Truck Load: shipments reach the destination faster as the truck makes no other pickups/drop-offs |
| Carting                    | Handling system consisting of small vehicles (carts)                                           |
| trip_uuid                   | Unique ID for a particular trip (may include different source and destination centers)        |
| source_center               | Source ID of trip origin                                                                       |
| source_name                 | Source name of trip origin                                                                     |
| destination_center          | Destination ID                                                                                 |
| destination_name            | Destination name                                                                               |
| od_start_time               | Trip start time                                                                                 |
| od_end_time                 | Trip end time                                                                                   |
| start_scan_to_end_scan      | Time taken to deliver from source to destination                                               |
| is_cutoff                   | Unknown field                                                                                  |
| cutoff_factor               | Unknown field                                                                                  |
| cutoff_timestamp            | Unknown field                                                                                  |
| actual_distance_to_destination | Distance in km between source and destination warehouse                                   |
| actual_time                 | Actual cumulative time taken to complete the delivery                                         |
| osrm_time                   | OSRM-calculated cumulative shortest path time (considers traffic and road types)              |
| osrm_distance               | OSRM-calculated cumulative shortest path distance (considers traffic and road types)          |
| factor                      | Unknown field                                                                                  |
| segment_actual_time         | Segment time: time taken by a subset of the delivery                                          |
| segment_osrm_time           | OSRM segment time: time for a subset of the delivery                                          |
| segment_osrm_distance       | OSRM segment distance: distance for a subset of the delivery                                   |
| segment_factor              | Unknown field                                              

## Recommendations 

* A significant volume of orders originates from top-performing states like Maharashtra. Additionally, most of the busiest delivery corridors connect major metro cities, suggesting that focusing operational efforts on these urban hubs can lead to higher efficiency and better resource allocation.

* For low-volume states like Nagaland (0.05%), consider minimal or on-demand support, given the low order volume and possible geographic or logistical challenges.

* Despite being short to moderate in distance, Bhiwandi - pune and Gurgaon - Sonipat corridors show unusually high delivery times. It's recommended to conduct a route audit, optimize hub operations, and adopt traffic-aware dynamic routing to improve efficiency.

* Most of the trips are created on Wednesdays (approximately 17%), it is recommended to ensure adequate staffing and resource allocation on this day to handle peak operational load efficiently.

* Since FTL routes are more challenging than Carting routes, it is recommended to analyze the FTL network for possible delays due to routing, loading/unloading, or long-distance planning. Route optimization and better scheduling can help reduce delivery time for FTL shipments.

* Since most delays are observed on long-distance routes (like Chandigarh - Bengaluru, Guwahati - Delhi, Kolkata - Bhiwandi), which likely pass through multiple hubs. it is recommended to reduce wait times and handover delays at high-traffic hubs like Bhiwandi, Bengaluru, and Gurgaon. Also Explore alternative routes or optimize dispatch based on real-time traffic conditions.

* The test results show a clear gap between predicted and actual delivery times, indicating that the current system does not fully capture real delivery conditions. It is recommended to enhance the time and distance predictions by incorporating real-world delivery data — such as traffic delays, wait times at hubs, and en-route stops. Also, improve how individual segment times are combined into a full trip. Avoid double-counting delays or overestimating time at each step, as this can lead to inflated total trip times.

These improvements will support better route planning, more accurate ETAs, and a smoother delivery experience overall.
