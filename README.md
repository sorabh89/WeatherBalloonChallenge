# WeatherBalloonChallenge
generate the data to test weather baloon system

Ther requirement is as follows:
We are part of a global weather monitoring program. A lot of hydrogen weather balloons were released to flow around the globe to collect important weather data. The data was collected by on- ground observatory stations. The collected data includes timestamp, temperature, latitude, longitude, observatory site code, etc. The data looks like:
timestamp
temperature location observatory
2018-01-01 00:00:00
-8.967658 0.856758,-0.402343 NZ
2018-01-01 00:01:00
NaN NaN NaN
2018-01-01 00:02:00
-9.379569 1.268990,0.544460 US
2018-01-01 00:03:00
-8.894050 0.818152,0.060277 UK
2018-01-01 00:04:00
-9.024794 1.434172,-0.785993 AU
0 1 2 3 4
Timestamp is the time the data been collected; temperature is in Celsius degrees; location is the longitude and latitude of the balloon; observatory is the country code of the observatory site. As depicted in the sample data, the real-world data is full of imperfection. The sensor could be faulty, the data points could be missed completely, and the datapoints were not guaranteed to come in order.
At the first stage, we need a program (or set of programs) that can perform the following tasks:
- Given that it is difficult to obtain real data from the weather balloon we would first like to be able to generate a test file of representative (at least in form) data for use in simulation and testing. This tool should be able to generate at least 500 million lines of data for testing your tool. Remember that the data is not reliable, so consider including invalid and out of order lines.
- Use a Jupyter notebook to showcase how you do EDA on the simulated data.
- Showcase how you wrangle the data and generate insight from the simulated data.

There are two files the code is divided in:
1) weather_data_generator.ipynb  : generates the data in csv as per the requirement. The number of records required can be changed in the code.
2) weather_data_processor.ipynb  : Reads the generated csv and fetches different values from it also has few basic functionalities that can be applied on the data.

Steps to run:
1) The code is written in a docker container using 'jupyter/all-spark-notebook' image.
2) run the above image in docker and upload the 2 files and the code is ready.
