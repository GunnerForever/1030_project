# A Quantitative Test for SARS-Cov-2 Infection

### This is the repository for Zefeng Xu's DATA 1030 Final Project at DSI, Brown University. <br>
This project aims to add a quantitative approach to the testing and diagnosis of COVID-19 using gene expression data. Other approaches include biological analyses such as Nucleic Acid Tests. <br>
This project is to solve a binary classification problem of whether a patient is infected with COVID-19 using data from Gene Expression Omnibus (GEO) database. <br>

To reproduce the results, please read below. <br>

Below is the structure of this repository. <br>
```
├── data/                     
    ├── preprocessed/             
    └── labels.csv                
├── figures/                  
├── report/                   
├── results/                  
├── src/                      
├── .gitignore                
├── LICENSE                   
├── README.md                 
└── requirements.yml          
```
data/ <br>
This directory contains both raw and preprocessed feature matrix and target label files. <br>
Raw file containing all labels at in labels.csv at root of data/. <br>
Preprocessed X_train, X_test, y_train, y_test for each of the 10 random states are stored in data/preprocessed subdirectory. <br>
File containing the original feature matrix is too large to store as a single file so is not present here. <br>
Please read below in Section **Data** for the way to download the raw feature matrix. <br>

figures/ <br>
This directory contains all figures generated in this project. <br>

report/ <br>
This directory contains the pdf version of the final report of this project. <br>

results/ <br>
This directory stores all saved models, tuned parameters, train/test scores, and corresponding training and testing sets from cross validation. <br>

src/ <br>
This directory contains source code for both the midterm and final presentations, and the final report. <br>
The latter one contains the most recent and important results. <br>

## Data
The feature matrix file is publicly available on GEO website with dataset ID GSE212041. <br>
To download the feature matrix, follow the below steps. <br>
1. Go to this [website](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE212041). <br>
2. Scroll down to the bottom and you will see **Supplementary file**. <br>
3. Download the one with file name **GSE212041_Neutrophil_RNAseq_TPM_Matrix.txt.gz**. <br>
4. Unzip it and you will find a .txt file with name **TPM_S1G.txt**. <br>
5. This file contains 60640 rows and 782 columns and is the original feature matrix. <br>
- This feature matrix is transposed in this project since 60640 is used as number of columns and 782 is used as number of rows. <br>
- There are only 781 samples instead of 782. There is a 'Symbol' column (removed for this project) in original data that contains the Gene Symbol of the 60640 genes. <br>

## Dependency
The developing environment used for this project is **Anaconda with Python 3.10.12**. <br>
Below are the major packages and their versions used. <br>
There is a requirements.yml file in the root directory for ease of use. <br>
- numpy 1.26.2 <br>
- scipy 1.11.4 <br>
- scikit-learn 1.2.2 <br>
- pandas 2.1.3 <br>
- matplotlib 3.6.0 <br>
- xgboost 2.0.2
- scanpy 1.9.5

## Author
Zefeng Xu (zefeng_xu@brown.edu)

## License
This project is licensed under the MIT License.













