# A Quantitative Test for SARS-Cov-2 Infection

### This is the repository for Zefeng Xu's DATA 1030 Final Project at Brown University. <br>
This project aims to add a quantitative approach to the testing and diagnosis of COVID-19 using gene expression data. <br>
This project is to solve a binary classification problem of whether a patient is or is not infected with COVID-19 using data from Gene Expression Omnibus (GEO) database. <br>

Below is the structure of this repository. <br>
├── data/          <br>
├── figures/       <br>
├── report/        <br>
├── src/           <br>
├── LICENSE        <br>
└── README.md      <br>

data/ <br>
Directory contains only the file containing target labels of this project (manually collected).  <br>
File containing the feature matrix is too large and please read below in Section **Data** for the way to download it. <br>

figures/ <br>
This directory contains all figures generated in this project and all of them except one are used in the final report. <br>

report/ <br>
This directory contains the pdf version of the final report of this project. <br>

src/ <br>
This directory contains source code for both the midterm and final presentations. <br>
The latter one contains the most important results. <br>
To reproduce the results, please first read the section **Dependency** before any downloads. <br>

## Data
The feature matrix file is publicly available on GEO website with dataset ID GSE212041. <br>
To download the feature matrix, follow the below steps. <br>
1. Go to this [website](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE212041). <br>
2. Scroll down to the bottom and you will see **Supplementary file**. <br>
3. Download the one with file name **GSE212041_Neutrophil_RNAseq_TPM_Matrix.txt.gz**. <br>
4. Unzip it and you will find a .txt file with name **TPM_S1G.txt**. <br>
5. This file contains 60640 rows and 782 columns and is the original feature matrix. <br>
- This feature matrix is transposed in this project since 60640 is the number of genes and 781 is the number of samples. <br>
- There are only 781 samples. There is a 'Symbol' column (removed for this project) in original data that contains the Gene Symbol of the 60640 genes. <br>

## Dependency
The developing environment used for this project is **Anaconda with Python 3.10.12**. <br>
Below are the major packages and their versions used. <br>
- numpy 1.26.2 <br>
- scipy 1.11.4 <br>
- scikit-learn 1.2.2 <br>
- pandas 2.1.3 <br>
- matplotlib 3.6.0 <br>
- xgboost 2.0.2
- scanpy 1.9.5














