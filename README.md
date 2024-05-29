# Gathering Data via SportRadar API
## Introduction
This program connects to the SportRadar API to gather depth chart data for runningbacks from 2006 through 2017. The depth chart data is from Week 1 of each season. Therefore, the depth chart value and team is from the start of the season. 

## Configuration
An API key for SportRadar will be needed to connect to the API.
This key needs to be inputted in the program at:
  - **"api_key = 'your_API_key_here'"**

All other parameters for the url are listed at this point. 

If a different week's data is sought after, the week can be changed. Currently, it is set to:
  - **"week_number = 1"**.

If a different position's data is sought after, it can be changed inside the loop that is parsing through the JSON data from the API:
  - **"if teams_dict[team]['offense'][x]['position']['name'] == 'RB':"** .

## Gathering Data
Once connected to the API, it will grab the player's ID, team, year, name, position, and number on the depth chart. This data will be outputted as a CSV file named *depth_chart_data.csv*.
