# Classifying-cybersecurity-incidents---ML-Model
 The task is to enhance the efficiency of Security Operation Centers (SOCs) by developing a machine learning model that can accurately predict the triage grade of cybersecurity incidents. Utilizing the comprehensive GUIDE dataset. The goal is to create a classification model that categorizes incidents as true positive(TP), benign positive (BP), or false positive (FP) based on historical evidence and customer responses. The model should be robust enough to support guided response systems in providing SOC analysts with precise context-rich recommendations, ultimately improving the overall security posture of enterprise environments.

 Objectives :
1.	A machine learning model capable of accurately predicting the triage grade of cybersecurity incidents(TP,BP,FP) with high macro F1 score, precision and recall.
2.	Implement a machine learning model for the classification and detection of attack patterns using MITRE ATT&CK data.
3.	A comprehensive analysis of model performance, including insights into which features are most influential in the prediction process. 


Issued faced and resolution :
	Memory Error :
		Because of the size of the dataset it led to memory error during initial data processing due to the computational weight of handling extensive data fields.
To overcome the memory issues encountered, two key preprocessing steps were applied :
Downsampling technique :
	Due to the large volume of data, downsampling was performed to reduce the overall size of the dataset. This involved, 
i)	Random sampling of the dataset to create a smaller representative subset of the data.
ii)	Selective downsampling of classes with disproportionately large data points, ensuring a balanced class representation and manageable data size.  
Datatype Optimisation :
	The dataset’s data types were modified to minimize memory usage. Specifically,
i)	Reducing integer and float datatypes : Floating point variables were converted from float64 to float32 and integer fields from int64 to int32 .
ii)	Optimizing categorical fields by converting string based categories into numerical codes, thereby reducing the memory footprint .
The combination of downsampling and datatype optimization allowed the model to efficiently process the data without exceeding memory limitations.
Model Development : 
	Once the data was prepared, machine learning models were trained to classify attack techniques. Key stages in model development included.
i)	Feature Engineering : Features were engineered based on MITRE ATT&CK tactics and techniques, focusing on distinguishing factors between different types of attacks .
ii)	Model Selection : Various machine learning model were evaluated, including tree based algorithms and neural networks, with an emphasis on balancing accuracy and computational efficiency .
iii)	Training and Evaluation : The models were trained on the optimized dataset and performance was evaluated based on accuracy , precision , recall and F1 score. 
Result and analysis : 
	The best performing model was able to classify cybersecurity threats effectively within the constraints of reduced memory usage. The memory optimization techniques ensured that the model could handle the data without crashes, making it suitable for deployment on machines with limited memory resources. 

Conclusion :
	The project demonstrates the feasibility of using machine learning with the MITRE ATT&CK framework for cybersecurity threat detection. By employing downsampling and datatype optimization, memory constraints were successfully mitigated, enabling efficient processing of high – dimensional cybersecurity data.
