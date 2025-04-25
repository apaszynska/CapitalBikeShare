# Capital Bikeshare - E-Bike Infrastructure Planning with Open Data

## Overview

This project aims to expand the use of solar-powered charging stations for e-bikes in the Capital Bikeshare system. Currently, there are 4 stations with solar charging, and the goal is to identify additional high-demand areas where these stations can be implemented.

By replacing battery swapping with solar-powered charging, the project seeks to reduce reliance on the grid, lower operational costs, and minimize environmental impact, promoting a more sustainable and efficient bikeshare service. The expansion of solar stations will ensure better availability of e-bikes, especially in areas with the highest demand.



## Data Sources

### Trip Data

This project uses publicly available datasets from Capital Bikeshare, including:
- **Bike Usage Data**: Daily ridership data in years 2021-2023. The data includes:
  
| Column              | Dtype    |
|---------------------|----------|
| ride_id             | object   |
| rideable_type       | object   |
| started_at          | object   |
| ended_at            | object   |
| start_station_name  | object   |
| start_station_id    | float64  |
| end_station_name    | object   |
| end_station_id      | float64  |
| start_lat           | float64  |
| start_lng           | float64  |
| end_lat             | float64  |
| end_lng             | float64  |
| member_casual       | object   |
  
Source: https://capitalbikeshare.com/system-data

- **Elevation Data**: In addition to the trip data, this project incorporates elevation data sourced from the OpenRoute Service API. By assigning elevation values to each station based on its geographic coordinates, I was able to analyze the terrain of different areas. This allowed me to assess whether a station is situated on an incline or decline, which is crucial for understanding the impact of elevation on e-bike usage. The elevation data helps in identifying areas where e-bikes may be more or less desirable, and it supports infrastructure planning, such as determining optimal locations for hybrid charging stations.

## Key Insights
**Focus on members:** The analysis concentrated on member riders because their usage patterns are more consistent, making them easier to analyze. Additionally, as a more stable group, they are easier to target with specific offers or incentives to influence behavior.

**Station Usage Patterns:** By analyzing bike usage patterns, I identified which stations experience peak demand.

**Bike drop-off Near High Demand Station:** Bikes are often dropped near high-demand stations due to overcrowding, leading to availability issues for other riders.

## Recommendation

- **Expand Station Capacity:** Add more bike racks or increase the number of stations in high-demand areas to reduce overcrowding and improve bike availability.
- **Expand Solar-Powered Charging Stations:** Increase the number of solar-powered charging stations in high-demand areas to ensure e-bikes are readily available, while promoting sustainability and reducing dependency on the grid.
- **Increase Incentives for Proper Bike Return:** Consider offering incentives (e.g., discounts, loyalty points) for users who return bikes to stations during peak demand times. This can help reduce the number of bikes left outside stations.
- **Enhance Predictive Modeling for Bike Distribution:** Use data analytics to predict and optimize bike distribution, ensuring that high-demand areas always have enough bikes.
