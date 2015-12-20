# weather-data-hadoop
Synopsis

This is an Hadoop Map/Reduce application for Working on weather data It reads the text input files, breaks each line into stations weather data and finds average for temperature , dew point , wind speed. The output is a locally sorted list of stations and its 12 attribute vector of average temperature , dew , wind speed of 4 sections for each month.

Installation

Since this a Map reduce Project , please install Apache Hadoop , Refere the below site for more details

https://hadoop.apache.org/docs/current/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html

Once you have installed the hadoop , download the project using git commands and install it.

$ git clone https://github.com/vasanth-mahendran/weather-data-hadoop.git
$ cd weather-data-hadoop
$ mvn install

Run

Add the sample input file given in the proect to the hdfs

hdfs dfs -put sample_weather.txt

and start the Map reduce application to submit the job to hadoop

hadoop jar ./target/weather-1.0.jar sample_weather.txt  dataOutput
