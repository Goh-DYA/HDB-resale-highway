# Analysis of Proximity to Expressways & Influence on HDB Resale Prices

## Background
- HDB flats are home to >80% of Singapore’s population
- 10 expressways covering >170km island wide
- Many HDB flats are situated near expressways

![image](https://github.com/user-attachments/assets/21d7c2b4-3968-4d12-85bc-9211dbe8b1bb)

## Problem Statement
Amid conflicting claims of noise pollution versus unblocked views (at high floors) by netizens, **does proximity to expressways have any influence on HDB Resale Prices**?

## Core Objectives / Questions
1. How does proximity to expressways influence overall HDB resale prices?
2. Is the impact of expressway proximity on HDB resale prices different for lower floors compared to higher floors?
3. How do other factors, such as flat characteristics (eg. no. of bedrooms, age, town), interact with expressway proximity to influence resale prices?

## Datasets
- HDB Resale Flat Prices (Jan 2015 to 2024)
  - Source: [data.gov.sg](https://data.gov.sg/datasets?query=resale+flat+price&resultId=189&page=1)
- National Map Line (SLA)
  - Road coordinates of all 10 existing expressways
  - Source: [data.gov.sg](https://data.gov.sg/datasets?query=national+map+line&resultId=d_aa9129ea72a19af27998dd4c78b5fd28&page=1)
- OneMap Reverse Geocode: 
  - Identify HDB buildings located within a specified radius of a given coordinate along the expressway
  - Source: [onemap.gov.sg](https://www.onemap.gov.sg/apidocs/apidocs/#reverseGeocode)

## Methods
**Linear Regression** was applied to quantify the difference observed in resale flat prices based on distance to expressway.

| Regression     | Variables       |
|----------------|-----------------|
| Baseline (measure impact of expressway distance on resale price)  | `distance_from_expressway` |
| Interaction with Floor/Storey | Additional variables: `storey_range_category` & floor-proximity interaction terms |
| Interaction with Flat Characteristics | Additional variables: `flat_type` (eg. 3-room, 4-room), `floor_area_sqm` (flat size), `remaining_lease_years` (remaining duration of lease) & interaction terms for distance and various flat features |


## Key Findings
#### Insight 1: The value of resale flats are **lower if situated near to an expressway**.
  - This impact is most significant for flats right beside (<50m) an expressway.
    - Compared to flats far away from expressways (>500m), flats less than 50m from expressways have a lower average resale price of $54415.</br>
![image](https://github.com/user-attachments/assets/2961fd48-2d89-4c08-b25b-622cd6b62f56)
  - However, there appears to be a threshold of about 300m from an expressway, where beyond that resale prices are not significantly affected.
    - Compared to flats far away from expressways (>500m), flats 301-500m away have a lower average resale price of $4390, but this difference is not significant.

#### Insight 2: The value of resale flats are **negatively affected for higher floors that are near expressways**.
  - Notably, their value declines much more compared to lower floors, if they are situated near expressways (< 50m) as compared to far away (>500m).
  - The marginal negative impact of very high (>30) floors is more than $200,000 compared to low (1st to 6th) floors, if less than 50m from an expressway.</br>
![image](https://github.com/user-attachments/assets/9f4506be-45bf-4b3b-9b58-f5d4e93ac184)

#### Insight 3: Proximity to expressways disproportionately affects resale prices of larger flats
- For flats very close (< 50m) to an expressway, the marginal negative impact on resale price when being close to an expressway is much more pronounced for large flat types (eg. Executive or 5-Room) compared to a 3-room flat.</br>
![image](https://github.com/user-attachments/assets/b1b7f612-1479-4cff-9abe-819d9266d6b4)
