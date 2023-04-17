# DeepLearningForHealthCare_FinalProject
In the paper "Predicting Heart Failure Readmission from Clinical Notes Using Deep Learning" https://arxiv.org/ftp/arxiv/papers/1912/1912.10306.pdf, the authors aim to prove that deep learning models are more accurate at the readmission prediction task as compared to other machine learning models. Specifically, the authors hypothesize that a CNN model will perform better than a  regular machine learning model based on random forest. We will test these same two models to compare performance.
 
Dataset Used:
The datasets used in this study are created from the MIMIC III database. They consist of clinical summary notes from heart failure hospital readmissions. The authors create two datasets, one for all readmissions, and one for readmissions within 30 days. 
https://physionet.org/content/mimiciii/1.4/

Prerequirests: Keras + Tensorflow

General Pipeline
1. imported NOTEEVENTS.csv, ADMISSIONS.csv, DIAGNOSES_ICD.csv
2. Filtred DIAGNOSES_ICD table to only include rows of data with heart failure ICD-9 codes:'39891', '40201', '40211', '40291', '40401', '40403', '40411', '40413', '40491', '40493', '4280', '4281', '42820','42821', '42822', '42823', '42830', '42831', '42832', '42833', '42840', '42841', '42842', '42843','4289'
3. used ADMISSIONS.csv to obatin emergency addmissions, which have readmission within 30 days and have diagnosis as heart failure
4. from NOTEEVENTS.csv, the discharge summaries for the addmission obtained from the previous step were extracted
5. Merged notes, admissions and diagonses to preprocess and generate embeddings
6. preprocessed discharge summaries to remove special chacters, extra spacing and lower case all text
7. tokenized notes by splitting each note and appending words to an array
8. used tokenized words to train Word2Vec model
9. used keras library to convert text corpus of notes to sequence of integers and padded sequences to length of 75
10. Transformed the output label to turn it into form that is more sutiable for the model and converted output label to a binary class matrix
11. split dataset into train and test sets
12. used keras to run CNN achitecure, and evalute performance
13. For ablation test, Word2Vec pre-tranined on clinical case reports was used generate embeddigs used in the CNN achitecure and evaluated. 
14. Random forset model used to compare performance
