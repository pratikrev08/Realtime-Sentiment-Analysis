# Sentiment Analysis for E-Commerce Platform

- A big data analytics solution to analyze customer reviews using Kafka, Flink and Druid for businesses to make data driven decisions based on customer feedback on e-commerce websites. 
- The system tracks ```product_viewed```, ```product_added_to_cart``` and ```product_review``` events and have a sentiment analysis model in the background that provides the sentiment of the text review.
- Raw input events are converted into processed events in the Flink job and are stored back into Kafka. Druid's Kafka indexer directly picks the processed events from the Kafka queue. 
- The paper is attached as a pdf that talks in detail about the design in building this system. 
- In short, there is a Flink job, analytics service to query Druid, a Flask API to do sentiment analysis and a dashboard to track the events generated in the system.
