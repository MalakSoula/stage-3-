# **Authors** 

Logy Khaled (@Logy), Alaa Hewela (@Alaa253), Rahma mamdouh Mohammed (@Rahmamam2000), Tawfek Ahmed Tawfek (@Tawfekahmed25), Malak Abdelfattah Soula (@Malak), Zeyad Ashraf (@Zashraf03), Nourhan Mahmoud (@NorhanM1) , Mohammed Dahab (@mdahab7)

## **GithubRepo**

https://github.com/Logykh/hackbio-cancer-internship


# **Introduction** 

This study compares **primary** and **metastatic breast cancer** to identify biomarkers that distinguish between these stages, essential for improving treatment strategies.

# **Dataset and Preprocessing**

**RNA-seq data** from the **CMI-MBC project**, comprising **40 samples** (**20 primary and 20 metastatic**), was obtained from GDC. Preprocessing involved data normalization and filtering genes with more than 25 zero values to ensure robust results. Random selection of 20 samples per group was performed.

# **Methodology** 

**Differential expression analysis** was conducted using DESeq2 to find differentially expressed genes based on an adjusted **p-value \< 0.05** and a **|log2FoldChange| \> 1**. Ensembl gene IDs were mapped to ENTREZ IDs for functional enrichment analysis. 

**GO enrichment** focused on biological processes, while **KEGG analysis** revealed relevant pathways.

# **Results**

The analysis identified key **differentially expressed genes** between primary and metastatic tumors. 

![image](https://github.com/user-attachments/assets/9c2491c8-037d-4a7e-8979-d001c0f887ee)


**GO Analysis** revealed significant biomarkers related to muscle structure and function, including muscle contraction and regulation of blood circulation.

![image](https://github.com/user-attachments/assets/16c10007-1f93-4f24-ab2b-61690a2af3d4)

![image](https://github.com/user-attachments/assets/82fe7cf6-9e64-4860-afaf-5f8700f3164d)

**KEGG pathway** analysis revealed significant involvement in cytoskeleton-related pathways in muscle cells and several cancer-associated pathways.

![image](https://github.com/user-attachments/assets/17f4a479-82f2-45ef-92c9-ec25e594793a)

![image](https://github.com/user-attachments/assets/97e91b86-5b25-47c1-aa62-3878fc4797f8)

# **Machine Learning Pipeline Overview**
This section describes a machine learning pipeline for the classification of gene expression data from breast cancer using a Random Forest classifier. The goal is to classify samples through gene expression data into metastatic and primary breast cancers.

# Data Preparation
It begins by reading the dataset and cleaning; the genes with low variance are filtered out and those containing a lot of missing values. Preprocessed data are standardized so that all features must have the same scale.

# Labeling
Labels are provided for 40 samples, from which the first 20 are metastatic, labeled as 1, and the remaining 20 as primary, labeled as 0.

# Dataset Split
Now, the pre-labeled dataset is split into training and test sets where 80% of the data can be used for training and the remaining 20% has been kept for testing. This split takes those features into consideration that are highly interlinked with the given labels.

# Model Training
The model trains on the selected features. The model performed at a very good level as its achieving an accuracy of 75% and some other metrics, including confusion matrix and classification are used for further evaluation

# Visualizations
**1- Feature Importance Plot:** 
The importance of the top 20 genes for making the predictions in a horizontal bar chart shows which features are most important for the model's performance.

![Picture1](https://github.com/user-attachments/assets/d662b6e0-36fb-45fb-86e5-bc0d1e18e8b9)

**2- Confusion Matrix Heatmap:**
It provides an overview of the model's performance by showing the count of true positives, true negatives, false positives, and false negatives of all the predictions. 

![Picture2](https://github.com/user-attachments/assets/eb44715f-398d-46f1-835c-b4372a214511)



These visualizations together provide information regarding the efficacy of the model and feature importance of various genes in the classification of breast cancer.


# **Conclusion**

This analysis suggests potential biomarkers for distinguishing between primary and metastatic breast cancer. The machine learning pipeline, utilizing a Random Forest classifier, achieved an accuracy of 75%. Future research should focus on validating these biomarkers and exploring their potential therapeutic applications, alongside enhancing machine learning models for improved classification.

