# IP Network Traffic Flows Labeled with 75 Apps

## Dataset Description

This dataset provides a comprehensive analysis of network traffic collected at Universidad Del Cauca, Popayán, Colombia. The data spans six days in April and May 2017, capturing diverse network activities. The dataset includes flow statistics obtained using CICFlowmeter and application layer protocol information obtained through Deep Packet Inspection (DPI) processing with ntopng.

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

- Hetav (202001447): 

- Vrund (202001075):

- Arth (202001274): EDA

- Vandan (202001041): EDA
