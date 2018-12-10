## Big Data and Machine Learning (Beginner level + Intermediate Level)

For Video: Hadoop Intro, it takes 35 minutes to learn it. The video tutorial gives basic ideas of Hadoop framework. After 2000, the solution which uses the computation power provided by available computers to process data could not help. In recent years, there is an incredible explosion in the volume of data. IBM reported that 2.5 billion gigabytes of data was generated every day in 2012. 40000 search queries were done on Google every second. Therefore, we need computers with larger memories and faster processors or other more advanced solutions. The idea distributed system is using multiple computers to do the processing work which has much better performance. There are also challenges for this. There are high chances of failure since a distributed system uses multiple computers. There is also limit on bandwidth. Because it is difficult to synchronize data and process, the programming complexity is also high. The solution is Hadoop. Hadoop is a framework that allows for distributed processing of large data sets across clusters of commodity computers using simple programming models. The four key characters of Hadoop are economical, scalable, reliable and flexible. Compared to traditional DBMS, Hadoop distributes the data to multiple systems and later runs the computation wherever the data is located. The Hadoop has an ecosystem which is evolved from its three core components, data processing, resource management and Hadoop distributed file system. It is now comprised of 12 components including Hadoop distributed file system, HBase, scoop, flume, spark, Hadoop MapReduce, Pig, Impala, Hive, Cloudera Search, Oozie, Hue.  

For QwikLab: Analyze Big Data with Hadoop, it takes me more than one hour to learn and write up a summary. I have acquired how to create Amazon S3 bucket store my log files and output data, Launch a fully functional Hadoop cluster using Amazon EMR, define the schema, create a table for sample log data stored in Amazon S3, analyze the data using a HiveQL script and write the results back to Amazon S3. It is interesting to learn.

For QwikLab: Intro to S3, it takes 50 minutes. In this lab, I learned:
•	Create a bucket in Amazon S3 service
•	Add an object for example a picture to the bucket
•	Manage access permissions on an object: change from private to public and see the access difference
•	Create a bucket policy by using the AWS policy generator which require the Amazon Resource Name. 
•	Use bucket versioning to get access the picture with same name but uploaded at different time by changing the bucket policy
The bucket is a really useful service and the versioning feature is quite cool.

For QwikLab: Intro to Amazon Redshift, it takes me 60 minutes. In this lab, it covers
•	Launch a Redshift cluster: a cluster is a fully managed data warehouse that consists of a set of compute nodes; when launching a cluster, you have to specify the node type which determines the CPU, RAM, storage capacity and storage drive type.
•	Connect an SQL client called Pgweb to the Amazon Redshift cluster: we can write and run queries in Pgweb and also view the database information and structure.
•	Load sample data from an S3 bucket into the Amazon Redshift cluster which will hold the data for querying.
•	Run queries against data stored in Amazon Redshift: we could use SQL to query the data we need.


In regard to Video: Short AWS Machine Learning Overview, it takes me 10 minutes. it talks about the Machine learning on AWS. Machine learning has three layers, framework interfaces for expert, ML platforms for developers and data scientists and application services for machine learning API calls in the application. Amazon Deep Learning AMI is for the frameworks layer and Zillow uses it. Amazon SageMaker is a good for ML platform layer. 

For Video Tutorial: Overview of AWS SageMaker, it takes me 35 minutes. The AWS SageMaker has four parts, including the notebook instance, jobs, models and endpoints. Notebook instance is about using algorithms to create model via training jobs. Training jobs are instances to train the model. We create models for hosting from job outputs, or import externally trained models into Amazon SageMaker. Endpoints are for developers to use the SageMaker in production. The tutor elaborate on xgboost, kmeans, scikit . He talks about setting up the training parameters. We can train it on single or multiple instances. Then we import models into hosts. The last step is build endpoint configuration and create endpoint for developers to call.

For AWS Tutorial: Analyze Big Data with Hadoop, it takes me 80 minutes. I followed the following steps to finish the tutorial:
•	Step 1: Set Up Prerequisites: you have to have a personal AWS account; create an Amazon S3 Bucket and folder to store the output data from a Hive query; create an Amazon EC2 Key Pair to to connect to the nodes in your cluster over a secure channel using the Secure Shell (SSH) protocol.
•	Step 2: Launch The Cluster: user launches sample Amazon EMR cluster by using Quick Options in the Amazon EMR console and leaving most options to their default values; Amazon EMR is a managed cluster platform that simplifies running big data frameworks, such as Apache Hadoop and Apache Spark, on AWS to process and analyze vast amounts of data. By using these frameworks and related open-source projects, such as Apache Hive and Apache Pig, you can process data for analytics purposes and business intelligence workloads. Additionally, you can use Amazon EMR to transform and move large amounts of data into and out of other AWS data stores and databases, such as Amazon Simple Storage Service (Amazon S3) and Amazon DynamoDB.
•	Step 3: Allow SSH Connections to the Cluster From Your Client: Security groups act as virtual firewalls to control inbound and outbound traffic to your cluster. The default Amazon EMR-managed security groups associated with cluster instances do not allow inbound SSH connections as a security precaution. To connect to cluster nodes using SSH so that you can use the command line and view web interfaces that are hosted on the cluster, you need to add inbound rules that allow SSH traffic from trusted clients.
•	Step 4: Run a Hive Script to Process Data: The sample data is a series of Amazon CloudFront access log files; The sample script calculates the total number of requests per operating system over a specified time frame. The script uses HiveQL, which is a SQL-like scripting language for data warehousing and analysis
•	Step 5: Terminate the resources you do not need to save for the future: terminating your cluster terminates the associated Amazon EC2 instances and stops the accrual of Amazon EMR charges. Amazon EMR preserves metadata information about completed clusters for your reference, at no charge, for two months. The console does not provide a way to delete terminated clusters so that they aren't viewable in the console. Terminated clusters are removed from the cluster when the metadata is removed
There is more information on how to plan and configure clusters in your custom way, set up the security, manage clusters and trouble shoot cluster if it is performing in a wrong way.

For QwikLab: Intro to Amazon Machine Learning, it takes me 75 minutes. The lab tutorial consists of several parts: 
•	Part 1- Upload training data : we put restaurant customer reviews data into Amazon S3 bucket and save it for analyzing
•	Part2- Create a datasource: configure Amazon ML to use the restaurant data set; we set customer review data as the data source for Amazon ML model
•	Part3- Create an ML Model from the Datasource: we will use data source to train and validate the model created in this part; the data source also contains metadata, such as the column data types and target variable which will also be used by the model algorithm; the ML modeling process will take 5 to 10 minutes to complete and we can see that in message section
•	Evaluate an ML model: the Amazon Machine Learning service evaluate the model automatically as part of the model creation process; it takes 70 percent of the data source to train the model and 30 percent to evaluate it. 
•	Generate predictions from ML model: batch mode and real-time mode are two ways to generate predictions from ML model; batch mode is asynchronous while the real-time mode is real time.

For AWS Tutorial: Build a Machine Learning Model, it takes me 50 minutes. It is about using Amazon ML to Predict Responses to a Marketing Offer:
•	Step 1: Prepare Your Data: In machine learning, you typically obtain the data and ensure that it is well formatted before starting the training process; we use customer purchase history to predict if this customer will subscribe to my new product
•	Step 2: Create a Training Datasource using the Amazon S3 service
•	Step 3: Create an ML Model: After you've created the training datasource, you use it to create an ML model, train the model, and then evaluate the results
•	Step 4: Review the ML Model's Predictive Performance and Set a Score Threshold
•	Step 5: Use the ML Model to Generate Predictions

For Video Tutorial: Overview of AWS SageMaker, it takes me 40 minutes: The AWS SageMaker has four parts, including the notebook instance, jobs, models and endpoints. Notebook instance is about using algorithms to create model via training jobs. Training jobs are instances to train the model. We create models for hosting from job outputs, or import externally trained models into Amazon SageMaker. Endpoints are for developers to use the SageMaker in production. The tutor elaborate on xgboost, kmeans, scikit . He talks about setting up the training parameters. We can train it on single or multiple instances. Then we import models into hosts. The last step is build endpoint configuration and create endpoint for developers to call
For AWS Tutorial: AWS SageMaker, it takes me 80 minutes. 
Step 1: Setting Up
Step 2: Create an Amazon SageMaker Notebook Instance
Step 3: Train and Deploy a Model
Step 4: Clean up
Step 5: Additional Considerations

For Build a Serverless Real-Time Data Processing App, it takes 150 minutes, 

Cloud web application
For QwikLab: Intro to S3, it takes 50 minutes. In this lab, I learned:
•	Create a bucket in Amazon S3 service
•	Add an object for example a picture to the bucket
•	Manage access permissions on an object: change from private to public and see the access difference
•	Create a bucket policy by using the AWS policy generator which require the Amazon Resource Name. 
•	Use bucket versioning to get access the picture with same name but uploaded at different time by changing the bucket policy
The bucket is a really useful service and the versioning feature is quite cool.

