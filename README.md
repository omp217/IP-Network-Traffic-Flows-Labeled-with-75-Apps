# IP Network Traffic Flows Labeled with 75 Apps

## Dataset Description

This dataset provides a comprehensive analysis of network traffic collected at Universidad Del Cauca, Popayán, Colombia. The data spans six days in April and May 2017, capturing diverse network activities. The dataset includes flow statistics obtained using CICFlowmeter and application layer protocol information obtained through Deep Packet Inspection (DPI) processing with ntopng. Overall it contains 87 attributes and 35,77,296 instances.

### Key Attributes

- **Flow Characteristics:** Duration, packet counts, and lengths in both forward and backward directions.
  
- **Inter-Arrival Times:** Information on inter-arrival times at the flow, forward, and backward levels.

- **Flag Counts:** Count of different flags (e.g., SYN, FIN) providing details on flag usage.

- **Packet Size and Length:** Metrics such as average packet size, minimum and maximum packet lengths.

- **Bulk Transfer Analysis:** Details on bulk transfer metrics for both forward and backward directions.

- **Subflows:** Information on the number of forward and backward subflows.

- **Connection Time Statistics:** Mean, standard deviation, maximum, and minimum times for both active and idle connections.

Each record in the dataset is labeled as either 'Normal' or 'Malicious,' providing insights into the nature of network activities. The dataset includes information on the Layer 7 protocol and the corresponding protocol name associated with the network traffic. This dataset is suitable for various applications, including network security analysis, anomaly detection, and performance optimization.

## Protocol Classification Problem
Using the available data we have tried to classify the Protocol Name. Initially we used all the columns except Protocol Name to classify the Protocol Name using decision tree and we got around 99% accuracy. Then we went on removing columns but the accuracy score remained the same. But when we removed L7Protocol column the accuracy went below 40%. On further analysing we found that there is a one-to-one mapping between L7Protocol and Protocol Name. Both of these columns are nominal and hence we couldn't notice the direct mapping through correlation as both the columns are encoded. To reduce the dimensions we used pca but still the accuracy was about 48%. 

There were some Protocol Name which were majority so we decided to split the dataset in two parts one which has Protocol Names which appears more than or equal to  10000 times and other in which the Protocol Name appears betweenn 10000 - 100000 times. Then we did a bit of preproceesing (through intutution and through trial and error).Later we predicted the Protocol Name using the following models Decision Tree, Random Forest, XGBoost, SVM, Neural Network.
## User Classification Problem

### Problem

The goal is to categorize users into distinct groups—Low Consumption, Medium Consumption, and High Consumption—based on their data plan usage. This classification enables the implementation of personalized policies within LTE network architectures, ensuring a more tailored and efficient use of network resources.

### Work

The following steps have been taken to address the user classification problem:

1. **K-Means Clustering:**
   - Users were initially classified into 2, 3, or 4 groups using K-Means Clustering.

2. **Classification Algorithms:**
   - Various classification algorithms were employed to categorize users into 2, 3, or 4 groups.

3. **Tree-Based Algorithms:**
   - Notably, tree-based algorithms such as Decision Tree, Random Forest, and XGBoost exhibited superior performance due to the dataset's nature.

4. **Utilized Algorithms:**
   - The following algorithms were used for user classification:
     - K-Nearest Neighbors
     - Support Vector Machine
     - Decision Tree
     - Random Forest
     - XGBoost
     - Artificial Neural Network

The comprehensive approach combines data mining and traditional machine learning techniques to derive insights into consumption behavior. The classification model, by grouping users based on their consumption patterns, enables the implementation of personalized policies. This, in turn, facilitates the enhancement of network security, maintenance of service quality, prevention of network failures, and the potential for offering targeted data plans to users.

## Contribution

- Om (202001462): Neural Network and Support Vector Machine for Protocol Classification Problem, Entire User Classification Problem (Unsupervised - K-Mean Algorithm and Supervised Learning - K-Nearest Neighbors, Support Vector Machine, Decision Tree, Random Forest, XGBoost, and Artificial Neural Network)

- Hetav (202001447): Data Preprocessing, Classification of Protocol Name using Random Forest and XGBoost

- Vrund (202001075): EDA, Data Preprocessing, Classification of Protocol Name using Decision Tree

- Arth (202001274): EDA

- Vandan (202001041): EDA
