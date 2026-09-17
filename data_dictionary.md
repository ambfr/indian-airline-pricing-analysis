# Data Dictionary

## Dataset Fields

| Column | Description |
|---|---|
| Airline | Name of the airline operating the flight |
| DateofJourney | Date on which the journey takes place |
| Source | City where the flight originates |
| Destination | City where the flight ends |
| Route | Flight route between source and destination |
| Dep_Time | Scheduled departure time |
| Arrival_Time | Scheduled arrival time |
| Duration | Original flight duration |
| Total_Stops | Number of stops during the journey |
| Additional_Info | Additional information associated with the flight |
| Price | Ticket price |

## Derived Fields

| Column | Description |
|---|---|
| Journey_Month | Month extracted from the journey date |
| Journey_Day | Day of the month extracted from the journey date |
| Departure_Category | Departure time grouped into categories for analysis |
| Duration_Hours | Flight duration converted from text into numeric hours |

## Data Preparation

The original dataset was preserved as `Raw_Data`.

A separate `Clean_Data` sheet was used for transformations and analysis. The derived fields were added to support comparisons involving journey timing and flight duration.
