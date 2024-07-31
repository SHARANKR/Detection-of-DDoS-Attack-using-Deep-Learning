# Detection-of-DDoS-Attack-using-Deep-Learning

## Introduction
A distributed denial-of-service (DDoS) attack is a malicious operation that seeks to disrupt the legitimate flow of traffic to a server, service, or network by flooding it with overwhelming network traffic.This has been a great challenge due to frequently changing attack patterns, the rapid development of cyber offense tools, and the open availability of cyber offense materials in the dark web. DDoS attacks can cause severe disruption to online services, resulting in lost revenue, reputation damage, and decreased customer trust.  DoS and DDoS are two different attack types, but the final aim of the attacker remains the same. DoS attacks use one computer (attack computer) and one victim. In contrast, DDoS attacks rely on more infected bots to carry out the tasks simultaneously to infect the target server, making it difficult to access the services for legitimate users. 

## Objectives
* Detection of Distributed Denial-of-Service (DDoS) attacks using a deep learning model.
* Utilization of the Long Short-Term Memory (LSTM) neural network architecture for feature selection and extraction.
* Use of the CICDDoS2019 dataset for training and testing the LSTM model.

## System Design
### Architectural Diagram
Fig showcases a DDoS attack detection system powered by a Long Short-Term Memory (LSTM) model. The system utilizes the CIC-DDOS2019 dataset, containing examples of both regular traffic and DDoS attacks, to train the LSTM model. By analyzing patterns in the training data, the LSTM learns to differentiate between normal and malicious network behavior. Once trained and evaluated, the system can classify new, real-time traffic as benign or a potential DDoS attack, enabling security personnel to take appropriate action.

## Methodology
### 1. Data Preparation:
* Dataset Selection: Curating a diverse and representative dataset is crucial for training and testing the DDoS detection models. The dataset should encompass various types of network traffic, including both benign and malicious traffic.
* Import and Distribution:The meticulous attention given to ensuring the random distribution of rows in the dataset is not just a procedural step; it's a preemptive measure against potential biases that might inadvertently influence the model during subsequent training and testing phases.
* Data Preprocessing: Before testing, the dataset undergoes preprocessing to ensure consistency, 
relevance, and suitability for input into the deep learning models. This may involve data cleaning, Feature Selection, Segregating data , label encoding, normalization.

### 2. LSTM Model Development:
Long Short-Term Memory (LSTM) is a type of recurrent neural network (RNN) architecture that is designed to overcome the limitations of traditional RNNs in learning and retaining longterm dependencies in sequential data.
![image_2024-07-31_193406307](https://github.com/user-attachments/assets/fcce4220-3d87-466d-bdd7-db90774f6f1a)

Each LSTM cell contains a memory cell and three gates: the input gate, the forget gate, and the output gate.
* Memory Cell *: It is capable of retaining information over long periods, enabling the LSTM model to capture dependencies across multiple time steps and a fundamental component of the LSTM architecture
* Input Gate: The input gate controls the flow of new information into the memory cell. It evaluates the current input and the previous hidden state to determine which new information should be stored in the memory cell. 
* Forget Gate: It evaluates the current input and the previous hidden state to determine which information from 
the memory cell should be discarded or forgotten. The forget gate allows the LSTM model to prioritize important information while discarding irrelevant or outdated information, thereby maintaining the relevancy of the memory cell over time.
* Output Gate: It controls the exposure of information from the memory cell to the next layer or as the output of the LSTM model.
* Activation Function :The selection of the sigmoid activation function in hidden layers and the softmax activation function in the output layer is a nuanced decision. It reflects an understanding of the binary nature of the classification problem, where the model needs to discern between benign and malicious traffic.

### 3. Model Training:
* Training Dataset and Evaluation:The training process is not just a computational task, it's a dynamic journey where the model 
learns to discern patterns, adapt to complexities, and generalize from the provided data.
* Hyperparameter Tuning and Optimization: It involves a delicate dance between computational efficiency and model performance and refining the model's internal representations.

 ### 4. Model Evaluation:
* Testing and Metrics:Testing the model on an unseen data and metrics chosen for evaluation – accuracy, precision, recall, and F1-score.
* Overfitting check:To check for overfitting, compare performance on training and validation sets, use cross-validation, and plot learning curves.

## Dataset Description
The CICDDoS-2019 dataset is a comprehensive dataset designed for researching Distributed Denial of Service (DDoS) attack detection. Collected by the Canadian Institute for Cybersecurity, this dataset includes a variety of DDoS attack types captured in a simulated environment with realistic background traffic. It contains labeled network traffic data, including packet captures (PCAPs) and flow features, which can be used to train and evaluate machine learning models for detecting DDoS attacks. Each row in the dataset represents a network flow, which is a summary of all packets exchanged between a source IP and a destination IP over a specific period.The dataset 80 columns (features), commonly  describing various aspects of the network flows. 

## Conclusion
The  primary objective was to tackle the critical challenge of detecting Distributed Denial of Service (DDoS) attacks by employing deep learning techniques, particularly focusing on implementing a Long Short-Term Memory (LSTM) model.By harnessing  deep learning model like LSTM, the project aimed to develop a robust solution for identifying and mitigating DDoS attacks in real-time. Initially, the dataset underwent preprocessing steps, which involved dropping columns with a single unique value and converting categorical labels into 
numerical equivalents. Following this, standardization and normalization techniques were applied to enhance the model's performance. The core aspect of the project involved constructing and training an LSTM model for DDoS attack detection, leveraging its capability to capture long-term dependencies in sequential data. The LSTM model architecture consisted of multiple layers of LSTM units, augmented with dropout layers to mitigate overfitting. Upon completion of the training process, the LSTM model demonstrated promising performance metrics on both the training and test datasets, indicating in identifying malicious network traffic accurately. It provided a comprehensive solution aimed at bolstering network security and fortifying defenses against DDoS attacks.

## Contributing
I welcome contributions to this project! Here are some ways you can help:

1. **Report bugs**: If you find any bugs, please create an issue.
2. **Feature requests**: If you have ideas for new features, please let me know.
3. **Code contributions**: Feel free to fork the repository and submit pull requests.

### Steps to Contribute
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.
