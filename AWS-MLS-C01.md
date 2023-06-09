# AWS Machine Learning Specialty Cheatsheet
2023/6/19 Passed

## Table Of Contents
* [Day 1](#day-1)  
* [Day 2](#day-2)  
* [Day 3](#day-3)  
* [Day 4](#day-4)  
* [Day 5](#day-5)  
* [Day 6](#day-6)  
* [Day 7](#day-7)  
* [Day 8](#day-8)
* [Day 9](#day-9)
* [Day 10](#day-10)
* [Day 11](#day-11)
* [Day 12](#day-12)
* [Day 13](#day-13)
* [Day 14](#day-14)
* [Day 15](#day-15)
* [Day 16](#day-16)
* [Day 17](#day-17)
* [Day 18](#day-18)
* [Day 19](#day-19)
* [Day 20](#day-20)
* [Day 21](#day-21)
* [Day 22](#day-22)
* [Day 23](#day-23)
* [Day 24](#day-24)
* [Day 25](#day-25)
* [Day 26](#day-26)
* [Day 27](#day-27)
* [Day 28](#day-28)

---

## Day 1
`Apache Spark` -> An open-source unified analytics engine for **large-scale** data processing.  
`Object2Vec` -> A general-purpose neural **embedding** algorithm that is highly customizable. It can learn **low-dimensional** dense embeddings of *high-dimensional* objects, can find semantically **similar** objects.    
`Semantic segmentation` -> Supervised, Categorize each **pixel** in an image into a class or object.   
`Elasticsearch(Amazon)` -> A distributed, RESTful *search* and *analytics* engine capable of addressing a growing number of use cases. Individual **server** required.   
`SageMaker Ground Truth` -> A data **labeling service** that makes it easy to label data(option: *Amazon Mechanical Turk*)   
`Sparkmagic` -> A set of **tools** for interactively working with remote *Spark clusters* through Livy, a Spark REST server, in Jupyter notebooks.  
`SageMakerEstimator` -> Tight integration between *Spark* and *SageMaker* for several models including XGBoost, and offers the **simplest** solution  
`MLLib` -> Built on top of *Spark*, MLlib is a scalable **machine learning library** consisting of common learning algorithms and utilities, including classification, regression, clustering, collaborative filtering, dimensionality reduction, and underlying optimization primitives.  

[Top](#aws-machine-learning-specialty-cheatsheet)

---

## Day 2
`Qualitative data` -> **Non-numeric** forms of data.  
`Histogram` -> A graph used to represent the frequency **distribution** of a few data points of one variable.  
`Scatterplot` -> Uses dots to represent values for **two different** numeric variables. Spot **outliers**.  
`Seaborn distribution plot(distplot)` -> Depicts the variation in the **data distribution**.  
`Amazon Personalize` -> A fully managed machine learning service that uses your data to generate item **recommendations** for your users.  
`SMOTE(Synthetic Minority Oversampling Technique)` -> A technique to **over-sample** the minority classes while avoiding overfitting.  
`One-class SVM` -> unsupervised, learns a decision function for **novelty** detection.  
`Breadth-first search(BFS)` -> An algorithm for searching a tree *data structure* for a node that satisfies a given property.  
`Random Search(RS)` -> A technique where random combinations of the **hyperparameters** are used to find the best solution for the built model.  
`Grid Search` -> A tuning technique that attempts to compute the optimum values of **hyperparameters**.  
`Depth-first search` -> An algorithm for searching a graph or tree *data structure*.  
`Amazon EBS(Amazon Elastic Block Store)` -> Provides block level storage volumes for use with EC2 instances.  
`Amazon Lex` -> Enables you to build applications using a speech or text interface powered by the same technology that powers **Amazon Alexa**.  
`Amazon Polly` -> Use deep learning technologies to synthesize natural-sounding **human speech**. *Speech Marks*: starts and ends, *SSML*: control, *Lexicons*: customize  
`Amazon Transcribe` -> Converts **audio input into text**, which opens the door for various text analytics applications on voice input.  
`Xavier Initialization` -> An attempt to improve the *initialization* of neural network **weighted inputs**, in order to avoid some traditional problems in machine learning.  

### Scaler
| Name | Explanation |
| --- | --- |
| MinMaxScaler | No-Gaussian distribution |
| StandardScaler | Gaussian distribution,  the features need to be standardized to ensure that they contribute **equally** to the analysis.

### Optimizer
| Name | Explanation |
| --- | --- |
| Mini-batch gradient descent | Split the dataset into small subsets (batches) and compute the gradients for each batch. |
| Gradient descent | An optimization algorithm that's used when training a machine learning model. |
| **Adagrad** | An algorithm for gradient-based optimization. | 
| **Rmsprop** | An *extension* of gradient descent and the **AdaGrad** version of gradient descent that uses a decaying average of partial gradients in the adaptation of the step size for each parameter. |

### Note
* SageMaker, to update an `Endpoint`, you must create a new `EndpointConfig`
* **Parquet** is faster then *csv*. 
* To use SageMaker training, the data should be split into *training*, *validation*, and *test* sets.
* Correlation: Feature1(0.64) >(**stronger**) Feature2(-0.85) 
* SageMaker, "Data download failed." -> Check IAM role of **encrypt** and **decrypt** the data

[Top](#aws-machine-learning-specialty-cheatsheet)

---

## Day 3
`ROC(Receiver Operating Characteristic Curve)` -> A graph showing the performance of a **classification model** at all classification *thresholds*. A good ROC: (0, 1)   
`AUC/ROC(Area Under the ROC)` -> AUC measures the ability of the model to predict a higher score for positive examples as compared to negative examples. For **binary classification model**.  
`LDA(Latent Dirichlet Allocation)` -> **Unsupervised**, **classification**, a **topic** modelling technique that can classify text in a **document** to a particular topic. Same as `NTM`, "bag-of-words" model, the **order** of words does **not** matter.  
`Apache Flink` -> A **streaming** dataflow engine that you can use to run real-time stream processing on high-throughput data sources.  
`Amazon SageMaker BlazingText` -> Provides highly optimized implementations of the **Word2vec(relationships)** and **text classification** algorithms.  
`Amazon SageMaker NTM(Neural Topic Model)` -> **Unsupervised**, used to organize a corpus of **documents** into topics that contain word **groupings** based on their statistical distribution. Same as `LDA`.  
`AWS DeepRacer` -> An autonomous 1/18th scale race **car** designed to test **RL** models by racing on a physical track.  

### EC2 Types
| Option | Discount |
| --- | ---|
| On-Demand | 0% |
| Reserved | 40%-60% |
| Spot | 50%-90% |

### Note
* SageMaker `endpoints` are not targets for `Application Load Balancers`.
* `AWS Glue` cannot run **SQL** queries on the data.
* `Amazon Lex` top choice, `Slot Value`

[Top](#aws-machine-learning-specialty-cheatsheet)

---

## Day 4 
`Kinesis Producer Library (KPL)` -> Simplifies producer application development, allowing developers to achieve high write **throughput** to a *Kinesis Data Stream*.   
`Data Augmentation` -> A set of techniques to artificially **increase** the amount of data by generating **new data** points from existing data.  
`Image localization` -> Aims to locate the main **single** (or most visible) **object** in an image.  
`Instance Segmentation` -> Deals with detecting instances of objects and demarcating their **boundaries**.  
`Weight Decay` -> A **regularization** technique by adding a small penalty, usually the L2 norm of the weights (all the weights of the model).  
`Anaconda` -> An open-source distribution of the Python and R programming languages for **data science** that aims to simplify package management and deployment.  
`DescribeTrainingJob(SageMaker)` -> Returns information about a job you previously initiated, check **FailureReason**.  
`AWS CloudWatch` -> A **monitoring** service for AWS resources and applications.  
`AWS CloudTrail` -> A web service that records **API** activity in your AWS account.  
`Amazon RDS` -> Amazon Relational Database Service (Amazon RDS) is a web service that makes it easier to set up, operate, and scale a **relational database** in the AWS Cloud.  
`Pair plot` -> Plot **pairwise relationships** in a dataset.  
`Box and Whisker plot` -> Shows how the data is **distributed** and it also shows any **outliers**.  
`Tree map` -> An alternative way of visualising the hierarchical structure of a **Tree Diagram** while also displaying **quantities** for each category via area size.  
`Multilayer Perceptron (MLP)` -> A fully connected **multi-layer** neural network.  
`Autoregressive Integrated Moving Average (ARIMA)` -> A method for forecasting or predicting *future* outcomes based on a historical **time series**.  
`AutoML` -> Choose the *best model* for your time-series data. (including **DeepAR**, **ARIMA**, etc)  
`Service Control Policies (SCPs)` -> A type of **organization policy** that you can use to manage permissions in your organization.  
`Organizational Unit (OU)` -> A logical **grouping of accounts** in your organization, created using AWS Organizations.

### Data Distribution
| Name | Explanation |
| --- | --- |
| Normal distribution | Also known as the *Gaussian distribution*, Data near the **mean** are more frequent in occurrence than data far from the mean.|
| Poisson distribution| Independent events that occur at a **constant** rate within a given *interval* of time. |
| Binomial distribution | The discrete probability distribution that gives only **two possible results** in an experiment, either success or failure. |
| Bernoulli distribution | **n = 1**, the binomial distribution is a Bernoulli distribution. |

### Note
* `DynamoDB Stream` can only be used in `DynamoDB`, `SQL queries` are **not** supported.
* Fraud Detection(*positive: fraud*), false **negative**: incorrectly identifying fraudulent transactions as **non-fraudulent**.

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 5
`Custom inference container` -> *Amazon SageMaker*, port **8080**, requests under **2s**, compress in **tar** format.  
`Incremental learning` -> A machine learning method where **new data** is incrementally added to a model, and the model is retrained on the new data.  
`ResNet-50` -> A convolutional neural network(**CNN**) that is 50 layers deep.  
`Boosting` -> A method used in machine learning to **reduce errors** in predictive data analysis.  
`Binning` -> Binning is the process of converting numeric data into categorical data.  
`Interval Binning` -> The process of transforming **numerical** variables into their **categorical** counterparts.  
`Horovod` -> A **distributed deep learning** training framework for TensorFlow, Keras, PyTorch, and Apache MXNet. **Multiple GPU**  

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 6
`Amazon Aurora` -> A fully managed relational database engine that's compatible with *MySQL* and *PostgreSQL*.  
`AWS Step Functions` -> A visual **workflow service** that helps developers use AWS services to build distributed applications, automate processes, orchestrate microservices, and create data and machine learning (ML) **pipelines**.  
`Amazon Simple Workflow Service` -> A fully managed **workflow service** for building scalable, resilient applications. More complex then *AWS Step Functions*.  

### Note
* A Spot interruption on the **Master node** will *terminate* the entire *cluster*, and on a **Core node**, it can lead to HDFS *data loss*(`Amazon EMR`).
* **Vanishing gradient** results from small derivates of the **sigmoid** activation function, try **ReLU**.  
* `BlazingText`: Labels must be prefixed with `__label__`, and the tokens within the sentence - including punctuation - should be `space` separated.
* **XGBoost 1.0/1.1**: CPU-only algorithms, **XGBoost 1.2/newer**: GPU, Accelerated Computing(EC2, `P3`)
* **Bring Your Own Containers**: Set `ENV SAGEMAKER_PROGRAM` for `train.py` in the Dockerfile.
* `SageMaker inter-container traffic encryption`, secured in-transit of private VPC.
* A large *learning rate* will **overshoot** the true minima, while a small will **slow down** convergence.
* A large *batch size* will **get stuck** in localized *minima*.
* SageMaker **default IAM role**, buckets' name with "sagemaker" is accessible.

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 7
`AWS PrivateLink` -> Establish connectivity between **VPCs** and AWS services without exposing data to the internet.  
`Beta Testing` -> Acceptance Testing, the end users evaluate its performance.  

### Note
* **SSE-KMS** is used for the Amazon **S3** service. 

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 8
`Linear Discriminant Analysis (LDA)` -> **Dimensionality** reduction.  
`AWS Glue crawler` ->  A program that **connects** to a data store (source or target) such as Amazon S3, used for automated collection and maintenance of **metadata** in the Glue Catalog.  
`Batch Transform` -> To get inferences for an **entire dataset**.  
`Precision-Recall Area-Under-Curve (PR AUC)` -> For **imbalanced** datasets, focus on the **positive** class.  
`Inference pipeline` -> Preprocessing, predictions, and post-processing on **real-time** and **batch** inference requests. Containers: **2-15**.  

### Note
* `Python Shell` supports `AWS Glue` jobs.
* `number_of_shards = max (incoming_write_bandwidth_in_KB/1000, outgoing_read_bandwidth_in_KB/2000)`
* `Amazon SageMaker` supports authorization based on **resource tags**.
* When a model is **underfitting**, then adding **more features** to the model or **removing regularization**.

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 9
`SageMaker built-in algorithm` -> Target variable should be in the **first column**; It should **not** have a *header record*. Content-type: `text/csv`, for unsupervised, `label_size=0`.   
`Data Lake` -> Primarily store raw, **unprocessed** data.  
`Data Warehouse` -> Structured data that has been cleaned and **processed**, ready for strategic analysis.  
`Mindmap` -> A diagram used to visually organize *information* into a hierarchy, showing relationships among pieces of the whole.  
`Hashmap` -> A data structure that is used to *store* and *retrieve* values based on keys.   
`Identity federation` -> Manage user identities **outside of AWS**.  

### Note
* ML first step: **Shuffle** the dataset.  
* `CloudTrail` does **not** monitor calls to *InvokeEndpoint*, captures **API calls**.
* `SageMaker` monitoring metrics are available on `CloudWatch` at a **1-minute** frequency.

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 10
`Inference pipeline model` -> Amazon SageMaker handles invocations as a sequence of **HTTP** requests.  
`Kinesis Data Streams PutRecord API` -> Uses **name** of the stream, a partition **key** and the data **blob**.  
`Kinesis Data Firehose PutRecord API` -> Uses the **name** of the delivery stream and the data **record**.  
`N-grams` -> A sequence of N words.  
`Levenstein distance` -> A string metric for measuring the *difference* between two sequences.  
`Recursive Feature Elimination(REF)` -> A **feature selection** method that fits a model and removes the weakest feature (or features). Use for **overfitting**.  
`Bar Chart` -> A pictorial representation of data that uses bars to compare different **categories** of data.  
`Bubble Chart` -> Show relationships between **numeric** variables.  
`Root Mean Square Error (RMSE)` -> Distance measure between the predicted numeric target and the actual numeric answer (ground truth).   
`Mean Absolute Error (MAE)` -> The absolute values of each prediction error on all instances of the test data-set.  

### Note
* There are **no inter-node** communications for **batch** processing.
* `SageMaker incremental training`: **Object Detection**, **Image Classification** and **Semantic Segmentation** are supported.
* Mandatory hyperparameter `mode` for **Word2Vec** (unsupervised) and **Text Classification** (supervised) of the `SageMaker BlazingText`.
* `SageMaker Console`, `SageMaker API` and `SageMaker Notebook` can be used to train a SageMaker model.
* `Validation Set` for hyperparameter tuning. 
* Remove *stop words* for nlp. 
* `Automatic model tuning`, linear learner **internal tuning mechanism** will be *turned off*, `num_models`, to **1**.
* For aged training data, retrain the model using the **historical data** along with the **new data**.
* Replicate a *subset* of the data in S3, Set the `S3DataDistributionType` field to `ShardedByS3Key`.
* **Network Isolation not support**: `Amazon SageMaker Reinforcement Learning`, `Chainer`, as *outside* data are required. 
* Data saved within `/home/ec2-user/SageMaker` folder persist between notebook instance sessions. 
* Feature engineering for `cyclical features`, represent features to `(x,y)` coordinates on a circle using *sin* and *cos* functions. 

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 11
`unigram transformation` -> Each unique word is a *feature*.  
`Speech Synthesis Markup Language (SSML)` -> Control aspects of **speech**, such as pronunciation, volume, pitch, speed rate for `Polly`.  
`Vault Lock` -> Set **immutable policies** to enforce compliance controls for `S3`.  
`Label encoding` -> Convert **categorical** variables into **numerical** format.  
`AWS shared responsibility model` -> A concept of dividing **responsibilities** between AWS and a Customer. The Customer is you. AWS's responsibilities are the security of the cloud.  
`Translate` -> Can **auto-detect** source language and **convert** it to a target language.  

### Note
* Increase **batch size** would result in **less-frequent** weight adjustment.
* **Duplicated data** should be **cleaned up** before processing, **validation** guides the **tuning** exercise.
* Use the **validation data** to tune the *model* performance.
* **Tree-based** algorithms like *decision tree*, *random forest*, and *xgboost* have a lower and upper **bound** it can predict for regression.
* For **time-series** prediction, you need to split the dataset based on **time**, *random shuffling* is **not** recommended for time series forecasting.
* *Best* possible error represents for **human-level performance**. 
* With `Lambda`, based on the **memory** configuration, proportional *CPU* capacity is allocated. 
* **Batch size** and **learning rate** should be adjusted by the same factor. 

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 12
`Cost Function` -> Measures the **performance** of a machine learning model for given data.  
`Canary Deployment` -> In the beginning, the **current** version receives **100%** of user traffic.  
`Mapping technique` -> For **ordinal**, **categorical** data.  
`Stratified K-fold cross validation` -> For **unbalanced** data to evaluate the model performance.  
`Principal component analysis(PCA)` -> A learning algorithm that **reduces** the **dimensionality** (number of features) within a dataset, can also **visualize** data directly.  

### Note
* Selete the model has less **penalties**.
* `Softmax activation` predicts for **one class** among other classes, whereas `sigmoid activation` predicts for **each class** independent of one another.
* `SageMaker Estimator`, `local mode: instance_type='local'` can quickly experiment with the models without having to wait for the training data to be **loaded**.

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 13
`cyclical features` -> Hours of the day, days of the week, months in a year, and wind direction.  
`Rolling deployment` -> A deployment strategy that slowly **replaces previous** versions of an application with new versions.  
`Nvidia jetson edge` -> AI computing platform for GPU-accelerated parallel processing in mobile embedded ... Robotics and **Edge** Computing.  
`XGBoost`  -> An *Extreme Gradient Boosting algorithm* that is optimized for boosted **decision trees**, can **not** be used for **recommending system**, **no scaling** is required. **LibSVM** or **CSV** format are required.  
`ImageNet` -> A large visual **database** designed for use in visual object recognition software research.  
`MapReduce(Amazon EMR)` -> A big data analysis model that **processes data** sets using a parallel algorithm on computer clusters.  
`EMR File System (EMRFS)` -> An implementation of HDFS that all `Amazon EMR` clusters use for **reading and writing** regular files from Amazon EMR directly to `Amazon S3`.  
`Random Cut Forest` -> unsupervised, detect **anomalous** data points within a data set, works in `Kinesis Data Analytics`.   
`K-means` -> Unsupervised, A **cluster** refers to a collection of data points aggregated together because of certain *similarities*. Mandatory parameters: `feature_dim(number of features)` and `k(number of clusters)`, can use for **dimensionality reduction**.  
`Amazon Quicksight` -> **Anomaly detection**, **forecasting**, **auto-narrative**: customize(personalized dashboard), don't need `SageMaker` for forecasting.  
`Quantile Binning` -> The process of assigning the **same** number of observations to each **bin**, using for **unevenly** distributed data.   

### Note
* `Hyperparameter tunning`: Run only **one** training **job** at a time.
* `Amazon EMR`, **master node**, **core node**, **task node**(can be used in *Spot instance*).
* Enable **inter-container** encyption for training in **privat VPC**.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty 2023 - Hands On! `OK`
* Udemy -> AWS Certified Machine Learning Specialty Full Practice Exam `(Practice Test2)`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 14
`Support Vector Machine(SVM) with RBF kernel` -> Supervised, for **classification** and **regression**, can also be used for **dimensionality reduction**. Can classify for **non-linear** problem.  
`AWS Glue's FindMatches` -> A way to perform **de-duplication** as part of *Glue ETL*.  
`Line Chart` -> A graph that uses lines to connect individual data points. Can **not** be used to **spot outliers**.   
`PCA in randomized mode` -> For datasets with a *large* number of **observations** and **features**. (*regular mode*)  
`SageMaker Elastic Inference` -> Allows you to attach a **low-cost GPU** to your instance. Using to improve the inference **throughput**, can **not** replace `Auto Scaling`.    
`Robust Standardization` -> Reduces the effect of the **outliers** in the features.  

### Merics
1. Accuracy
$$Accuracy=\frac{TP+TN}{TP+TN+FP+FN}$$
* **Overall** performance

2. Precision
$$precision=\frac{TP}{TP+FP}$$
* Minimize **false positives**

3. Recall
$$recall=\frac{TP}{TP+FN}$$
* Minimize **false negatives**, describes positive records that predicted correctly.

4. Specificity
$$specificity =\frac{TN}{TN+FP}$$
* Minimize **false positives**, used for **substance abuse**.

5. F1 Score
$$F1=2*\frac{precision*recall}{precision+recall}$$
* **Balancing** between Precision and Recall

Where `TP/FP` - `True/False Positive`, `FP/FN` - `False Positive/Negative`, respectively.  

### Note
* `Kinesis Data Firehose` + `built-in lambda` is eaiser than `Kinesis Data Streams` + `Glue ETL`, as a `Glue` script is required.(for *near real-time*)
* `BlazingText Word2Vec mode`: The *order* of words **doesn't** matter, skip-gram and continuous bag of words(**CBOW**) architectures. Find *relationships* between **words**.
* `SageMaker Training Task built-in Algorithm`, 1. **ARN** and **IAM role**, 2. compute **instance**, 3. *model* output path of **S3**. 
* `Cost function`, **low positive** data -> penalize **false negative**.
* Add **more training data** for **overfitting**.
* Config **network isolation** for `SageMaker` `training jobs` and `models`, through **interface endpoint**.
* Use *S3* `COPY` loads large amounts of data to `Amazon Redshift`, efficient.
* **Constant variance** is required for `linear regression`.
* ML should have fair sampling with **even distribution** of outcomes.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty: 3 PRACTICE EXAMS `(Practice Test1 & Practice Test2)`


[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 15
`Amazon Rekognition` -> Offers pre-trained and customizable computer vision (CV) capabilities to **extract** information(*metadata*) and videos. **Celebrity** detection, `Pathing`: track of the **path** people take in videos.  
`Categorical Encoding` -> Converting *categorical* data into **integer** format, **ordinal** and *nominal* data.  
`Amazon Redshift Spectrum` -> Data **warehousing** service, can query and retrieve structured and semistructured data from files in `Amazon S3` **without loading** the data. Provides *Online Analytical Processing* (**OLAP**).  
`Box plot` -> A method for graphically demonstrating the locality, spread and **skewness** groups of numerical data. If a number is less than `Q1 – 1.5×IQR` or greater than `Q3 + 1.5×IQR`, then it is an **outlier**.  

### Note
* `Sagemaker Linear Learner`, *automatic model tuning* will set `num_models1` to 1.
* `Bivariate/Multivariate visualizations` can **not** be used to group data points(*clustring*).
* `LDA` can figure out the right **categories** for each *product*.
* Drop features, **low variance**, **low correlation** and lots of **missing values**.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty: 3 PRACTICE EXAMS `(Practice Test3)`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 16
`One-hot encoding` -> A process by which **categorical** variables are converted into a form that could be provided to ML algorithms, such as *day of week*.  

### Note
* Increase **batch size**, weights of features are adjusted **less often**.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty MLS-C01 [2023]

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 17
`K-nearest neighbors(KNN)` -> Supervised, **classification**, **regression**. Uses proximity to make classifications or predictions about the **grouping** of an individual data point, can be used to **non-linear** regression.  

### Note
* `SageMaker built in XGBoost`, no code necessary, automatically **scaling**, do **not** perform *one-hot encoding* on **binary** features. 

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty MLS-C01 [NEW 2023] `(Practice Test) - OK`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 18
`VPC endpoint` -> Enables connections between a `virtual private cloud (VPC)` and supported *services*, without requiring that you use an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection.  
`VPC gateway endpoint` -> A target for a route in your route table used for traffic destined to either `Amazon S3` or `DynamoDB`.  
`A/B testing` -> **Compares** the performance of two versions of model to see which one *appeals* more to visitors/viewer, uses the 2 model variants with **half** the traffic serving each of them. **low risk**.  
`Amazon SageMaker DeepAR` -> A supervised learning algorithm for forecasting scalar (**one-dimensional**) **time series** using *Recurrent Neural Networks* (**RNN**). Specializes in forecasting **new product performance**.    
`Amazon Textract` -> A machine learning (ML) service that automatically **extracts** text, handwriting, and data from **scanned documents**.  
`Collaborative filtering` -> Recommender systems for calculating ratings based on ratings of similar users. Recommandations are based on the other **users(collaborator)**.  
`Content-based` -> Recommander system, Recommandations are based on the **contents**.  

### Note
* Increase the *mini-batch size* with the number of *GPUs* **linearly** in order to fully utilize all GPUs.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams 2023 `(1&2 - OK)`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 19
`Comprehend` -> Supports **multiple languages**, can do **summarization**, **supervised classification** and **extract** text from documents.  
`Splunk` -> A *software* platform be used to search, analyze and visualize of data.   
`Managed ETL service` -> `AWS Glue` (works with only **one** engine) and `AWS Data Pipeline` (can use **multiple** engines).   
`Logarithm Transformation` -> Decreases the effect of the **outliers**, to be more *normally distributed*.  
`Residuals` -> Represent the portion of the target that the model is unable to predict. A **positive** residual indicates that the model is **underestimating** the target, whereas a **negative** residual indicates an **overestimation**.(`Residual = Actual value – Predicted value`)  
`Amazon SQS` -> A **queuing service**, send, store, and receive messages between software components at any volume.  
`Amazon Forecast` -> A fully managed service that uses statistical and machine learning algorithms to deliver highly accurate **time series** forecasts. *ML background* is **not** required.  
`Blue/Green deployment` -> A deployment strategy in which you create two **separate**, but **identical** environments, once testing is completed, direct **all** traffic.  
`AWS Database Migration Service (AWS DMS)` -> A managed *migration* and *replication* service that helps move your database and analytics workloads to AWS

### Metrics
| Metrics | Meaning |
| --- | --- |
| High bias | **Underfitting** (too simple) (The model has not established the perfect relation between inputs and outputs) |
| High variance | **Overfitting** (too complex) (model not generalizing well to new data points) |

### Note
* When the graph has a long **right tail**(fewer data), it is **right-skewed** and vice versa. 
* A `KMS key policy` permission should be granted to the **Role** who are going to access the data reside in S3. 
* The prebuilt containers in `SageMaker` supports **Python** SDK not *R*.
* All the *containers* of the **same model** should reside on the **same EC2** instance.
* `Amazon Blazingtext`, the training/validation file should contain a training sentence **per line** along with the labels. 

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 20
`AWS Direct Connect` -> **Connection** between **on-premises** network to the **cloud** network.  
`Amazon SageMaker Linear Learner` -> Supervised, used for solving either **classification** or **regression** problems of **high-dimension** data.  
`Amazon Macie` -> A **data security service** that uses machine learning (ML) and pattern matching to discover and help protect your sensitive data.  
`Warm Start` -> Start a *hyperparameter tuning job* using one or more **previous** tuning jobs as a starting point.  
`Perplexity` and `BLEU score` -> Used for evaluating the performance of the **machine-translated** text.  
`Logistic regression` -> Supervised, with given specific *features*, predict the outcome as a probability(**binary output**).  
`K-fold cross validation` -> For **balanced** data, used to **estimate** the performance of the **model** on new data.  
`AWS DataSync` -> An online **data transfer service** that moving data between **on-premises** storage systems and **AWS storage** services, and also between AWS storage services.  

### XGBoost Hyperparameters
| Name | Function |
| --- | --- |
| Gamma | Regularization |
| ETA | Overfitting |
| Subsample | Overfitting |
| Alpha | L1 regularization |
| Scale_pos_weight | Adjusts the balance between **positive** and **negative** weights. |
| eval_metric(`validation: error`) | Emphasize **accuracy** |
| eval_metric(`validation:auc`) | Area under the curve(distinguish between **positive** and **negative** samples) |

### Amazon Ground Truth
| Service | Note |
| --- | --- |
| Mechanical Turk | A team of global, on-demand workers from Amazon. |
| Private labelling workforce | A team of workers from the company. |
| Vendor | A selection of experienced vendors who specialize in providing data labelling services. |

### Note
* `Amazon S3` uses a **gateway endpoint** not an *interface endpoint*.
* For `XGBoost`, when 2 features are found to have a **strong correlation** (positive or negative, like 0.97), one of them should be **removed**, *recommended*.
* Strongly correlated features **won’t** have a strong impact on *decision trees* algorithm(leave them will only have minimum impact).
* The *true positive rate* is the same as the **sensitivity** of the mode.

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 21
`Recursive Partitioning` -> A statistical method for multivariable analysis(`AWS GLUE`).  
`Sockeye` -> A sequence-to-sequence framework for **Neural Machine Translation** based on Apache MXNet Incubating.  
`Bayesian optimization` -> Build a probability model of the objective function and uses it to select **hyperparameter** to evaluate in the true objective function. Tuning like a **regression** problem, features are statistically *dependent*.  
`Amazon FSx for Lustre` -> FSx for Lustre **speeds up** your training jobs by serving your `Amazon S3` data to Amazon SageMaker at high speeds, high **throughput** and low **latency**.  

### Note
* A single `Amazon SageMaker endpoint` **cannot** serve two different `models`, support deploy different **versions** of the models behind a single endpoint.
* SageMaker, Hyperparameter tunning job: `HyperparameterTunner()`

### Question Set
* AWS Skill Builder -> AWS Certified Machine Learning - Specialty Official Practice Question Set (MLS-C01 - English)
* AWS Skill Builder -> Exam Readiness: AWS Certified Machine Learning - Specialty 

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 22
`AWS Glue` -> A **serverless** Apache **Spark** platform, *data preprocessing* for analysis through automated extract, transform and load (**ETL**) processes. Not meant to process *near real-time* data. **Not** support **RecordIO-Protobuf**, **Timestream** nor **LibSVM** format. Using **prefixes**.   
`network isolation` -> The containers **can't** make any *outbound* network calls, even to other AWS services such as `Amazon S3`.  
`Amazon SageMaker IP Insights` -> An **unsupervised** learning algorithm that learns the usage patterns for **IPv4 addresses**, using for **Fraud Detection**.  
`Within-cluster sum of squares(WSS)` -> **"elbow method"**, by ploting a `Line Chart` of showing a distortion score, could determining the **optimal value** of **k** in *k-Means* clustering.  
`Amazon SageMaker Neo` -> Enables developers to **optimize** machine learning (ML) models for inference on SageMaker in the cloud and supported devices at the **edge**.   
`Amazon IoT Greengrass` -> *Software*, extends *cloud capabilities* to **local devices**.  

### S3
| Name | Type | Note |
| --- | --- | --- |
| S3 Standard | **Frequent** | **Processed** data, high availability |
| S3 Standard-IA | **Less** frequent | Low availability |
| S3 Intelligent tiering | **Random** access | **Raw** data, high availability | 
| S3 Glacier Instant Retrieval | **Rarely** accessed, requires retrieval in milliseconds. | **Processed** data |
| S3 Glacier Deep Archive | Accessed **once** or twice in a year | **Raw** data, high availability |
* `S3 Lifecycle Rule`: Automating the archiving or deletion of old data
* `S3 versioning`: Keep the older version of the objects.

### Note
* Use `PCA` for dimensionality reduction for the large features cases even the question was **not** mentioned.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams 2023 `(3&4) - OK`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 23
`Seq2Seq` -> nlp, need **RecordIO-protobuf** format with **integer** tokens. Only supported on **GPU** instance(Accelerated Computing: `p*` & `g4*`) types and is only set up to train on a **single** machine.  

### Kinesis
| Name | Send multiple | Ingested from multiple | Auto scaling | 
| --- | --- | --- | --- |
| Kinesis Data Streams | Yes | Yes | No(manually (`UpdateShardCount`) |
| kinesis Firehose | No | Yes | Yes |
| Kinesis Video Stream | No | No | - |

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams 2023 `(5-ok&6-ok)`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 24
`Tf-idf(Term Frequency-Inverse Document Frequency)` -> `tf('fox', sent) * idf('fox', doc)`, where `tf('fox', sent) = 2/12` and `idf('fox', doc) = log(2/2) = 0`, respectively. Dimension of the matrix: `(sentences, unigram + bigram)`, *symbols* are **not** counted. Give less weight to the less frequent words in the dataset, and allow the more informative and frequent words to have a greater impact on the sentiment analysis. 
 
---

`Amazon Athena` -> An interactive query service that makes it easy to analyze data directly in Amazon Simple Storage Service (**Amazon S3**) using standard **SQL**. **Serverless**, **Parquet** format.  
`Amazon EMR` -> **Not serverless**, a managed cluster platform that simplifies running *big data frameworks*, such as **Apache Hadoop** and **Apache Spark**.(File system: *hdfs*, emrfs, local file system)   
`AWS DeepLens` -> *Hardware*, a deep learning-enabled **video camera**.  

### Date Imputation(Missing Data)
| Method | Type |
| --- | --- |
| KNN | Numerical |
| Deep Learning | Categorical | 
| MICE(**Multiple Imputation** by Chained Equations) | The **most** modern technique |
| Create a separate boolean column | - |
| Fill with zeros | - |
| Regression | - |
|Impute with median value | For outliers |

### Note
* **Decreasing** the class probability threshold makes the model more **sensitive**, marks more positive cases.
* Handle review **missing** data, *copy* the entire review to summary. 
* Use `Object2Vec` instead of `Word2Vec` when the target is for *sentences* or *paragraphs*.

### Online Practice
* **Air quality** prediction is a regression problem. 4
* Use `AWS KMS` to secure date on `S3` at rest. 5
* `AWS Glue` can **not** be used to train a model. 9
* `SageMaker` needs data to be on `S3`. 10
* **Customer churn** is a classification problem(YES or NO). 12
* **Trend** and **seasonality** do **not** take *bias* into account. 13
* `S3` **restrict access** using *DENY* if sourceVpce (vpc endpoint), or sourceVpc (vpc) is not equal. 15
* Makesure the Docker container is **NVIDIA-Docker compatible** if you want to use GPU. 18
* `Amazon Kinesis Firehose` can **transform**(simple) the data from one format to another. 22
* `Naive Bayes classifier` 25
* 26
* nlp: To *lower case*, *remove stopwords*, *tokneization*. 27
* **Data augmentation** for *overfitting*. 29
* **Overfitting**, **not** *generalized* enough. 39
* **Overfitting**, **decreasing** feature *combinations*(removing features). 44
* `RecordIO`, the best **format** choice for `SageMaker. 56  
* **Rescaling** the *entire* dataset before splitting it can lead to *data leakage*, rescale the training set and apply the *same* scaling to the validation and test sets. 59
* You could install *SageMaker docker container*(tensorflow, etc) for **local training**. 60
* `Amazon Kinesis Data Analytics` can use `lamda` to convert GZIP. 62

### Question Set
* Machine Learning – Specialty (MLS-C01) Sample Exam Questions `(2,6,8,9) - OK`
* https://www.examtopics.com/exams/amazon/aws-certified-machine-learning-specialty/view/14/

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 25
`T-SNE(T-Distributed Stochastic Neighbor Embedding)` -> An unsupervised, non-linear technique primarily used for data exploration, **dimensionality reduction**, **visualizing high-dimensional** data, **grouping**.  

### Note
* `Amazon ECR` save algorithm code. 74
* **Tagging a Docker image** means giving the image a specific label or name that distinguishes it from other versions or variants of the same image. 78
* Change class **wights** of loss function to improve Recall. 81
* **Two linear dependent features** will create a *singular matrix* during optimization. 84 
* `t-SNE` can do **grouping** and **visualization**. 89
* Run a **correlation check** of all features against the **target** variable. Remove features with **low** target variable correlation scores. 92
* `Stratified k-fold cross-validation` for inbalanced dataset with `k=5`(standard value). 100

### Question Set
* https://www.examtopics.com/exams/amazon/aws-certified-machine-learning-specialty/view/20/

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 26
`Image Classification` -> CNN, assigning a **label** or class to an entire image, can be used for **identify license plates**.  
`FM(Factorization Machines)` -> Supervised, a general-purpose supervised learning algorithm that you can use for both **classification** and **regression** tasks. **float32** format. Use for **high-dimension** data. Good for **click prediction** and **item recommendation**.  
`Naive Bayes classifier` -> A collection of **classification** algorithms based on Bayes' Theorem, good for *binary problem*. It assumes that each input variable is **independent**.  
`Amazon SageMaker Object Detection` -> MXNet algorithm detects and **classifies** objects in images using a single deep neural network. Require code development. Identify **objects** and their **locations**.  
`Amazon Augmented AI` -> Implement **human reviews** and audits of ML predictions based on your specific requirements, including multiple reviewers.  

### Kinesis
| Name | Note |
| --- | --- |
| Kinesis Data Stream | Streaming(**real-time**),  *rate*, ingest shards: **1000 KB/s** or 1000 messages/s |
| Kinesis Data Analytics | **Near real-time** analytics(**real-time SQL query**), can scripts out the **unneeded** data. |
| Kinesis Data Firehose | **Not real-time**, for **streaming** data(not used to *stream video*) into S3, etc. **Easiest way of Ingestion**, built-in lambda: *JSON* -> *Parquet* or *ORC*, can **not** use with `Glue` |
| Kinesis Video Stream | Streaming **video**(uses Amazon *S3* for backend storage), **analysis** |

### Note
* Select the value of `k` at the "elbow" ie the point after which the distortion/inertia starts decreasing in a **linear** fashion. 102
* Kinesis Data Stream speed. 104
* `Naive Bayes classifier`, features should be strongly **independent**. 105
* `Amazon Random Cut Forest (RCF)` does **not** use *older* records in the stream for machine learning. 108
* `Amazon SageMaker Object Detection`, data format for Computer Vision algorithms in SageMaker: `RecordIO`. 111
* `SageMaker` can automatically **reformat** the data that are stored in `S3`. 113
* Use **event tracker** in `Amazon Personalize` to include *real-time* user interactions, adding new training data to the model. 115
* `VPC endpoint policy` can limit the access to specific group of **user/roles**, `iam user policy` can limit user access other aws **service** but not secure the traffic. 116
* `lifecycle configuration` for `SageMaker`, automatic. 121
* To configure a Docker container to run as an **executable**, use an `ENTRYPOINT` instruction in a Dockerfile. 
* Jobs submitted to `AWS Batch` are **queued** and executed based on the assigned order of preference, it also offers an automated **retry** mechanism.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams `(Practice Test 1)`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 27
`Word2Vec` -> A text **classification** algorithm. Word2vec is useful for sentiment analysis, entity recognition, and translation, operates on **individual words**.  
`Amazon Redshift` -> A fully managed, petabyte-scale data **warehouse service** in the cloud, stores **structured** data from `EMR`. Can use **business intelligence** tools.  
`AWS Data Pipeline` -> A web service that makes it easy to schedule regular **data movement** and **data processing** activities in the AWS cloud. Including aws **SQL** service.  
`AWS Batch` -> AWS Batch helps you to run batch computing workloads on the AWS Cloud. **Automate** the batch *data preprocessing* and ML training aspects of the *pipeline*. Scheduling and allocating the **resources**.    
`AWS Panorama` -> Add **computer vision(CV)** to your **existing** fleet of cameras with AWS Panorama devices, which integrates with **existing camera** networks.  
`Normalization Transformation` -> Handle features that vary in different **magnitude**.  

### L1, L2 Regularation
| Name | Description |
| --- | --- |
| L1 | Reduce **dimensionality** (by zero the weights of features), not available to `Object2Vec` |
| L2 | Adjust **weight** for features (can also use for **underfitting**) |

### Note
* SageMaker, with `pipe input mode`, dataset is **streamed directly** to training instance, instead of being *downloaded* first. Does **not** support *Apache Parquet* data format.
* `AWS Batch` is **not** a valid destination of *S3 Events*.
* You need to wait a minimum of **30 days** before you can transition from the `S3 Standard` tier to `S3 Standard-IA`.
* `Amazon Kinesis Data Firehose` **buffers** incoming streaming data to a certain size or for a certain period of **time** before delivering it to destinations. 
* `Amazon Kinesis Data Streams`'s **Data Retention Period**, the minimum value for it is 24 hours.

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams `(Practice Test 3)`

[Top](#aws-machine-learning-specialty-cheatsheet)

---
## Day 28
`Amazon Redshift ML` -> Create, train, and deploy machine learning (ML) **models** using familiar **SQL** commands.  
`Amazon SageMaker Autopilot` -> **Automatically** trains and tunes the best machine learning models for *classification* or *regression*, **tabular data(csv)** format is required. **LEAST** operational overhead.  
`Peered VPCs` -> A networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. (Data does **not traverse** the **public** internet.)  
`Kinesis Client Library(KCL)` -> Acts as an intermediary between your record **processing** logic, **reading** data and *Kinesis Data Streams*. It **cannot** be used on the **source system** to produce real time data.  
`Custom entity recognition` -> Extends the capability of Amazon Comprehend, identify your specific new entity types that are not in the preset generic entity types.  
`Levenshtein distance` -> For example, the word "raed" is closer to the word "read" than the word "baed". This is more suited for applications like autocorrect.  

### Note
* `SageMaker` available data format, *JPG* and *CSV*.
* `Kinesis Data Firehose` is **not** a valid streaming source for a streaming ETL job in `AWS Glue`.
* Ensure that your containers are `nvidia-docker` compatible.
* Adjust the score *threshold* to tune the classification model performance.
* Use *pronunciation lexicons* in `Polly`.
* `Random Cut Forest (RCF)` can also be used in **time-series** data prediction.
* `Data Pipeline` does not support external **MySQL** databases. 

### Question Set
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams `(Practice Test 2)`

[Top](#aws-machine-learning-specialty-cheatsheet)

---

## Resources
* AWS Skill Builder -> AWS Certified Machine Learning - Specialty Official Practice Question Set (MLS-C01 - English) `(20 questions)`
* AWS Skill Builder -> Exam Readiness: AWS Certified Machine Learning - Specialty `(43 questions)`
* Udemy -> AWS Certified Machine Learning Specialty 2023 - Hands On! `(10 questions)`
* Udemy -> AWS Certified Machine Learning Specialty Full Practice Exam `(65 questions)`
* Udemy -> AWS Certified Machine Learning Specialty: 3 PRACTICE EXAMS `(10+65+65 questions)`
* Udemy -> AWS Certified Machine Learning Specialty MLS-C01 [2023] `(65 questions)`
* Udemy -> AWS Certified Machine Learning Specialty MLS-C01 [NEW 2023] `(20 questions)`
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams 2023 `(20*6 questions)`
* Machine Learning – Specialty (MLS-C01) Sample Exam Questions `(10 questions)`
* Udemy -> AWS Certified Machine Learning Specialty Practice Exams `(10+25+65 questions)`

---


