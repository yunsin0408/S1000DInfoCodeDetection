# S1000DInfoCodeDetection
This project uses and compares SVM, Random Forest and BERT as training models to identify the Information Code in S1000D Data Module Codes.

According to the S1000D 6.0 specification, there are a total of 1,145 Information Codes covering a wide range of topics (e.g., function, operation, servicing, fault reports). These codes categorize technical information into various functional areas. Given this, we aim to leverage machine learning by using XML files with correctly labeled Information Codes as a dataset to train an automated classification tool.

Our dataset contains four parts-the S1000D 6.0 Manual pages 3498-3546 (574 items), S1000D Bike Data Set for Release number 6 R2 (116 items), ‘s1kd_tools’(46 items) and ‘fossig’(12 items). We directly downloaded the first two (the first being the entire S1000D 6.0 Manual)  from the official S1000D website and the other two from Github. Since data was still inadequate for creating a model that could identify the full information code for these files, we decided to focus on identifying the first digit (the primary code) instead. This means the model should be able to identify large categories, for example: ‘Disconnect, remove and disassemble procedures’. 

The models used in the training process include Support Vector Machine (SVM), Random Forest (RF), and BERT. By employing these three models, the classification task benefits from a comprehensive approach that combines the advantages of traditional machine learning methods and natural language processing techniques.
After training, the model is evaluated on a testing set, using accuracy, precision, recall, and F1 score as evaluation metrics to assess its performance.
