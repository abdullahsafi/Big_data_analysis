<p align="center">  
   <h1 align="center">Big Data Analysis:floppy_disk:</h1>
</p>

Aim :mag_right:
----------------
Writing a series of Apache Spark programs to analyze an air traffic data set in PySpark using RDDs and DFs, and then optimising the programs for scalability on increasing data volumes.

Data and Schema
------------
The tasks are based on an Aviation On-time data set which includes information about airports, airlines, aircrafts, and flights. The schema is seen below:

<p align="center">
<img src="/schema.PNG" alt="schema.PNG" width="700"/>
</p>

How to run the notebook files:
------------
Import the files into a service that supports Apache Spark such as [Databricks](https://databricks.com).

Run the Bootstrap file to download the dataset.

Create a cluster with spark 3.0.1 and install the `sparkmeasure` PyPi and maven `ch.cern.sparkmeasure:spark-measure_2.12:0.17` libraries.

Finally run the programs

Tasks
------------
1. Task 1: Top-3 Cessna Models
Write an Apache Spark program that determines the top-3 Cessna aircraft models with regard
to the number of flights, listed in descending order of number of flights. Output the Cessna
models in the form ”Cessna 123” as one string with only the initial ’C’ capitalised and the
model number having just its three digits. The output file should have the following tabdelimited format, ordered by number of flights in descending order:
Cessna XYZ \t numberOfDepartingFlights

2. Task 2: Average Departure Delay
In the second task, write a Apache Spark program that determines the average, min and max
delay (in minutes) of flights by US airlines in a given year (user-specified year). Only consider
delayed flights, i.e. a flight whose actual departure time is after its scheduled departure time,
and ignore any canceled flights. The output file should have the following tab-delimited format
(ordered alphabetically by airline name):
airline_name \t num_delays \t average_delay \t min_delay \t max_delay

3. Task 3: Most Popular Aircraft Types
In the third task, you shall write an Apache Spark program that lists per airline of a given
country (user-specified) the five most-used aircraft types (manufacturer, model). List the
airlines in alphabetical order, and show the five most-used aircraft in descending order of the
number of flights as a single, comma-separated string that is enclosed in ’[’ and ’]’ (indicating
a list). Format the name of an aircraft type as follows: MANUFACTURER ’ ’ MODEL (for
example, ”Boeing 787” or ”Airbus A350”).
The output should have the following tab-delimited format (alphabetically by airline name):
airline_name \t [aircraft_type1, aircraft_type2, ... , aircraft_type5]
