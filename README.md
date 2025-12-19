Multiclass Intrusion Detection System using CIC-IoT 2023

This project presents a multiclass intrusion detection system built using machine learning techniques on the CIC-IoT 2023 dataset. The system is designed to classify network traffic into benign and multiple malicious attack categories while prioritizing high recall, which is a critical requirement in cybersecurity systems to ensure that attacks are not missed. To improve robustness and generalization, the model integrates Decision Tree, Random Forest, and K-Nearest Neighbors classifiers using a soft voting ensemble approach.

The primary objective of this system is to accurately detect and classify various types of cyber attacks present in IoT network traffic. Special emphasis is placed on handling highly imbalanced data, minimizing false negatives, and providing meaningful group-wise attack classification to better reflect real-world intrusion detection scenarios.

The CIC-IoT 2023 dataset is a realistic IoT network traffic dataset that includes both benign traffic and a wide range of attack types. The dataset is inherently highly imbalanced, mirroring real-world network environments. Fine-grained attack labels are further grouped into higher-level categories such as DoS, Probe, R2L, U2R, Malware, MITM, Vulnerability Scan, and Benign traffic to facilitate comprehensive evaluation.

The system is implemented using Python and leverages popular data science and machine learning libraries including NumPy, Pandas, Scikit-learn, and Imbalanced-learn. Class imbalance is addressed through a combination of controlled under-sampling of majority classes and over-sampling of minority classes, ensuring balanced learning without excessive information loss.

Three individual machine learning models—Decision Tree, Random Forest, and K-Nearest Neighbors—are trained independently. Their predictions are then combined using a soft voting ensemble classifier, which aggregates class probability outputs to improve overall detection performance and stability.

Model evaluation is performed using multiple metrics including accuracy, precision, recall, F1-score, and group-wise attack accuracy. Among these, recall is treated as the most critical metric, as failing to detect an attack poses a greater risk than generating false alerts. This evaluation strategy ensures the system is suitable for real-world intrusion detection applications.
