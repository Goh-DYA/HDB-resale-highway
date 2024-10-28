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




