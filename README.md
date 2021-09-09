# P3-Kafka-Streaming
##### By Devansh Sharma

### Project Description
Analysis of RSVPs from meetup.com using Kafka.

### Technologies Used
* Kafka [2.8]
* Spark[2.4.5]
* HDFS
* AWS S3
* YARN

### Features
* User can find out the current active cities in US which are scheduling Meetup Events.
* User can find out the trending topics in US Meetup Events.
* User can find out how many Big Data Meetup Events events are scheduled around the world.

#### TODOs for future development
This project can be extended to get the real time trending topics across the world or for a specific geography along with other business insights. By giving real time trends in topics like in twitter, users of meetup will be aware of the more popular and less popular topics in near real time. With minor modifications, this project can also be extended to process and analyze IoT data.

### Getting Started
Assuming Kafka and Spark of appropriate version is installed, the following commands are used to run the application.

Spark Streaming integeration with kafka 0.10.0.0 and above, is still in experimental status, Hence using Kafka 0.9 (http://spark.apache.org/docs/latest/streaming-kafka-integration.html)

Run Zookeeper to maintain Kafka, command to be run from Kafka root dir

  bin/zookeeper-server-start.sh config/zookeeper.properties
Start Kafka server, aditional servers can be added as per requirement.

  bin/kafka-server-start.sh config/server.properties
Start Producer.py to start reading data from the meetup stream and store it in '''meetup''' kafka topic.

Start Consumer.py to consume the stream from the '''meetup''' topic

Submit the spark job spark_meetup.py, to read the data into Spark Streaming from Kafka.

Spark depends on a external package for kafka integeration

  bin/spark-submit --packages org.apache.spark:spark-streaming-kafka-0-8_2.11:2.0.1 spark_meetup.py localhost:2181 meetup

### Contributors
* Sailash R
* Manaswini Agrawal
* Swati Pralhad Chavhan
* Pooja Kumari
* Divya Peddireddy
* Rajkumar K
* Ashish Kumar
* Aparna Sankarasetti
* Hemanth Ghosh
* Rohit Rawat
* Shubham Mishra
* Vaibhav Kant mishra
* Hemanth Soma
* Mallakunta Suresh
* Patrayadi Aditya Kumar
* Yusuf Ansari
* Jayashree C S

### Dataset Used
We can access the data stream through [meetup.com](https://stream.meetup.com/2/rsvps)

### License
This project uses the following license: [MIT License](https://github.com/devanshsharma-bigdata/P3-Kafka-Streaming/blob/main/LICENSE)

