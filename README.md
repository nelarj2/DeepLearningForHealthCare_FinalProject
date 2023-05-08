# DeepLearningForHealthCare_FinalProject

ORIGNIAL PAPER: <br>
This repository contains the code to reproduce experiments from the paper "Predicting Heart Failure Readmission from Clinical Notes Using Deep Learning" [1]
The authors aim to prove that deep learning models are more accurate at the readmission prediction task as compared to other machine learning models. Specifically, the authors hypothesize that a CNN model will perform better than a regular machine learning model based on random forest. We will test these same two models to compare performance.
 
 
DATA DOWNLOAD INSTRCTUTION: <br>
The datasets used in this study are created from the MIMIC III database. They consist of clinical summary notes from heart failure hospital readmissions. Files used to generate dataset were the "NOTEEVENTS.csv.gz" (1.1GB), "DIAGNOSES_ICD.csv.gz" (4.5MB) and "ADMISSIONS.csv.gz" (2.4MB) [2]
Link to dataset: https://physionet.org/content/mimiciii/1.4/
1) Using the link to the dataset, create a physinet account.
2) Navigate to he bottom webapge of the link to the "Files" section
3) Complete the listed required training: "CITI Data or Specimens Only Research"
4) Submit your training to physinet 
5) You'll recive an email that your application is approved, you can login in to phsionet and access the data. 

Prerequirests: <br>
Keras + Tensorflow
Word2Vec PubMed-and-PMC-w2v.bin 3.08GB http://bio.nlplab.org/
Glove Common Crawl (42B tokens, 1.9M vocab, uncased, 300d vectors, 1.75 GB) https://github.com/stanfordnlp/GloVe <br>

[1] [Xiong Liu, Yu Chen, Jay Bae, Hu Li, Joseph Johnston, and Todd Sanger. 2019. Predicting heart failure read-mission from clinical notes using deep learning.] <br>
[2] A. E. Johnson et al. MIMIC-III a freely accessible critical care database, Sci. Data, vol. 3, 2016. 
