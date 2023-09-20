# Solar Data Analysis
This Python script provided is used to process and analyze solar data from different buildings. It imports data from CSV files, processes it, and generates insights about the total energy produced.
Dependencies

#This script requires the following Python libraries:
pandas
os
datetime

#Usage

Before running the script, make sure you have Python installed and the necessary libraries mentioned above. You also need to have the data files in the correct directory on your system.

#The script contains several functions that process the data in various ways:

combine_dataset(building): This function takes a building name as input and returns a list of energy values (in kW) for that building, extracted from the relevant CSV files.

combine_buildings(Buildings,total=False): This function takes a list of building names as input and returns a pandas DataFrame with each building's energy values. If total=True, it also calculates the total energy values across all buildings.

sum_chunk(l,n): This function takes a list l and a number n as inputs and returns a list of average energy values (in kW), calculated over chunks of n values each.

combine_buildings_chunked(Buildings,n,total=False): Similar to combine_buildings, but uses sum_chunk to average the energy values over chunks of n values each.

date_time_series(length,time_step,time = True): This function generates a pandas DataFrame with a date and time series, starting from 01/01/2023 and with a time step of time_step minutes.

minutedataset(Buildings,total = False): This function generates a pandas DataFrame with energy data for the given buildings, averaged over 15-minute intervals.

hourdataset(Buildings,total=False): Similar to minutedataset, but averages the energy data over 1-hour intervals.

daily_dataset(Buildings,total = False): Similar to minutedataset, but averages the energy data over daily intervals.

date_converter(Date): This function converts a date in the format DD/MM/YYYY to a datetime.date object.

customdataset(time_gradation,start_date,end_date,Buildings,total = False): This function generates a pandas DataFrame with energy data for the given buildings, averaged over a custom time gradation (minutes, hours, or days), and within a custom date range.
At the end of the script, it calculates and prints the total energy produced in MWh.

#Note

Before running the script, make sure to replace the file paths and building names with those relevant to your data. The path and building names in the script are for illustrative purposes.

#Output

The script outputs a DataFrame with the energy produced per time gradation for each building and the total energy produced if total=True is passed. It also prints the total energy produced in MWh.
