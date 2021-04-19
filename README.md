# Architecture-for-real-time-video-streaming-analytics
This is an architecture to process video in real time using Kafka as a messaging service and Spark to process frames in real time, the architecture can be summarized in the image below.
![img](https://github.com/juan-csv/Architecture-for-real-time-video-streaming-analytics/blob/master/results/architecture.png)

# Start Zookeeper and kafka
To simplify the tedious task of building a kafka server, we will use Docker with Kafka and Zookeeper out of the box:
Go to the kafka-docker folder
<pre><code>$ cd kafka-docker </code></pre>

Start Kafka and Zookeeper with Docker Compose
<pre><code>$ docker-compose -f docker-compose_local.yml up </code></pre>

In the docker-compose_local.yml configuration file, the topics are defined, the url and the port through which our publisher and subscribers connected.

To stop Kafka uses
<pre><code>$ docker-compose stop </code></pre>
for more information Apache Kafka: Docker Container refer to this [post](https://towardsdatascience.com/kafka-docker-python-408baf0e1088)