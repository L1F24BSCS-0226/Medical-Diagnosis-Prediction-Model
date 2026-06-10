****MEDICAL DIAGNOSIS PREDICTION SYSTEM:****
Detailed Project Report
Submitted for the Data Structures Course

**Abstract:**
This project presents a Medical Diagnosis Prediction System developed in C++. The system combines traditional data structures with a machine learning approach to provide disease prediction support based on symptoms entered by users. The application manages patient records, prioritizes critical patients, maintains diagnosis history, and predicts possible diseases using a multiclass logistic regression model trained on a symptoms dataset.

**Introduction:**
Healthcare systems handle large amounts of patient information that require efficient storage, retrieval, and processing. This project demonstrates how data structures can be applied to solve real-world healthcare problems. The system provides facilities for patient registration, symptom assessment, disease prediction, prioritization of emergency cases, and record management.

**Objectives:**
• Develop a console-based healthcare application.
• Apply data structures to real-world scenarios.
• Implement efficient patient management.
• Prioritize patients based on severity.
• Predict diseases using machine learning.
• Store and retrieve records using file handling.
• Provide undo functionality for predictions.

**Problem Statement:**
Hospitals and clinics often face challenges in organizing patient information and prioritizing urgent cases. The objective of this project is to develop a system that can efficiently manage patients and provide disease predictions based on symptoms while demonstrating the practical implementation of data structures.


**System Features:**
1. Patient Registration
2. Automatic Patient ID Generation
3. Phone Number Validation
4. Patient Record Storage
5. Queue-Based Patient Assessment
6. Priority-Based Emergency Handling
7. Disease Prediction using AI
8. Top-5 Disease Recommendations
9. Prediction History Tracking
10. Undo Last Prediction
11. Patient Search and Editing
12. CSV Dataset Integration




**Data Structures Used:**
Queue: Used for normal patient assessment.
Stack: Used to undo the last prediction operation.
Linked List: Maintains prediction history.
Max Heap: Prioritizes patients with higher severity.
Binary Search Tree: Stores disease information for searching.



**Queue Implementation:**
The queue follows the FIFO principle. Patients with lower severity levels are inserted into the queue. Operations include enqueue, dequeue, and checking whether the queue is empty. The time complexity of enqueue and dequeue operations is O(1).



**Stack Implementation:**
The stack follows the LIFO principle. Whenever a prediction is generated, a copy of the patient record is pushed onto the stack. The pop operation allows the system to undo the most recent prediction. Push and pop operations both execute in O(1) time.



**Linked List Implementation:**
The linked list stores the prediction history. Each node contains patient details and predicted disease information. New records are inserted at the head of the list, resulting in O(1) insertion complexity.

****Max Heap Implementation:****
The max heap prioritizes patients according to severity. Critical patients are automatically inserted into the heap, while normal patients may later be transferred from the queue. Insert and extract operations execute in O(log n) time.



**Binary Search Tree Implementation:**
The BST maintains disease information. Diseases are inserted alphabetically and can be searched efficiently. Average search complexity is O(log n), although worst-case complexity may become O(n).



**Machine Learning Component:**
The project incorporates multiclass logistic regression using a One-vs-Rest approach. Separate binary classifiers are trained for each disease class. During prediction, probabilities from all classifiers are compared and the diseases with the highest confidence values are returned.

**Dataset Description:**
The dataset is stored in CSV format and contains disease-symptom relationships. Based on the provided implementation, the model supports 41 diseases and 131 symptoms. The uploaded dataset contained approximately 4920 training records representing 41 distinct diseases.


**Input Validation:**
The system validates age, severity levels, phone numbers, and menu selections to ensure that invalid inputs do not compromise system functionality.


**File Handling:**
Persistent storage is achieved through text files. Patient records are stored in patient.txt, diagnosis records are written to diagnosis_records.txt, and the most recent patient ID is maintained in last_id.txt.




**System Workflow:**
Step 1: Register patient.
Step 2: Generate patient ID.
Step 3: Determine severity level.
Step 4: Store patient in queue or heap.
Step 5: Collect symptoms.
Step 6: Generate disease predictions.
Step 7: Store prediction history.
Step 8: Provide search, edit, and undo functionality.


**Time Complexity Analysis:**
Queue Enqueue: O(1)
Queue Dequeue: O(1)
Stack Push: O(1)
Stack Pop: O(1)
Linked List Insert: O(1)
Heap Insert: O(log n)
Heap Extract Max: O(log n)
BST Search: O(log n) average
Logistic Regression Prediction: O(Number of Diseases × Number of Symptoms).


**Advantages:**
• Efficient patient prioritization.
• Practical application of multiple data structures.
• Persistent record storage.
• Predictive healthcare assistance.
• User-friendly console interaction.


**Limitations:**
• Console-based interface.
• Model accuracy depends on dataset quality.
• Predictions should not replace professional medical advice.
• Limited to diseases present in the dataset.



**Conclusion:**
The Medical Diagnosis Prediction System successfully integrates core data structures with a machine learning model to address a realistic healthcare problem. The project demonstrates technical proficiency in C++, object-oriented programming, file handling, algorithmic thinking, and predictive analytics. It highlights the importance of selecting appropriate data structures to improve efficiency and usability in software systems.


**Major Classes and Responsibilities:**
Class	Purpose
Patient	Stores patient information and symptom data.
MedicalDiagnosisSystem	Controls overall application workflow.
Queue	Manages waiting patients.
MaxHeap	Handles patient prioritization.
Stack	Provides undo functionality.
LinkedList	Stores prediction history.
BST	Stores disease information.
MultiClassLR	Handles multiclass disease prediction.
LogisticRegression	Implements binary logistic regression.
FileHandler	Performs file operations.
IDManager	Generates unique patient IDs.

