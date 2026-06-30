# Network Intrusion Detection System (IDS) - Machine Learning & Feature Extraction Pipeline

This repository contains the core Machine Learning and Data Engineering pipeline developed for a Next-Gen Hybrid Intrusion Detection System (IDS). The pipeline is engineered to process live network traffic, extract statistical flow features in real-time, and utilize advanced predictive models to classify malicious behaviors (such as DDoS and Brute Force attacks).

##  Key Features Engineered
* **Real-Time Traffic Inspection:** Developed utilizing **Python** and **Scapy** to passively sniff network packets from live interfaces.
* **Statistical Feature Extraction:** Dynamically extracts **56 distinct flow-based features** (including durations, packet counts, protocols, and byte sizes) to transform raw network data into structured inputs for the models.
* **Intelligent Behavioral Classification:** Integrated an optimized **XGBoost Classifier** to deliver instant network anomaly and threat detection verdicts based on behavioral intelligence rather than static rules.

##  Model Architecture & Performance
To maximize security efficiency, hyperparameter tuning (optimizing tree depth and learning rate) was systematically performed on the XGBoost model to maximize **Recall** and minimize critical false negatives.

### Classification Report Summary
The model achieves an overall accuracy of **89%**, with near-perfect **100% (1.00)** precision and recall metrics on severe mass network attacks:

| Attack Type | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: |
| **DDoS attack-LOIC-UDP** | 1.00 | 1.00 | 1.00 |
| **DoS attacks-GoldenEye** | 1.00 | 1.00 | 1.00 |
| **FTP-BruteForce** | 1.00 | 1.00 | 1.00 |
| **SSH-Bruteforce** | 1.00 | 1.00 | 1.00 |
| *Overall Accuracy* | | | **0.89** |

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Network Analysis:** Scapy
* **Machine Learning:** XGBoost, Scikit-learn
* **Data Manipulation:** Pandas, NumPy
