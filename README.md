# Fraud Detection in Financial Transactions
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/header.jpeg)

## Introduction

### Background and Problem
Fraud in financial transactions is a widespread issue that has significant negative impacts on individuals, businesses, and economies. Various types of fraud, such as insurance fraud, identity theft, bank fraud, healthcare fraud, and credit card fraud, pose significant challenges to financial institutions and law enforcement agencies. Traditional methods like signature verification, manual review, blacklist filtering, and Address Verification Services (AVS) have been used to combat fraud. However, these methods often fall short due to their outdated nature and inability to keep up with evolving fraud techniques.

### Project Objective
The objective of this project is to address the problem of fraud detection in financial transactions using machine learning techniques. By analyzing a provided dataset containing transaction details, customer information, and fraud labels, we aim to build a predictive model that can accurately identify fraudulent transactions. We will utilize popular libraries such as Scikit-learn, TensorFlow, Python Pandas, and Tableau for data analysis, model training, and visualization.


## Methodology and Results

### Dataset Description
For this project, we utilized a synthetic dataset obtained from [Kaggle](https://www.kaggle.com/datasets/bannourchaker/frauddetection). 
- The dataset includes information such as transaction type, transaction amount, and the sender and recipient's account balance before and after each transaction.

### Data Preprocessing
To prepare the data for analysis, we used the PySpark library in Colab for data cleaning and preprocessing.

### Model Selection: Keras Sequential Model
We chose to use a Keras Sequential model for our analysis. 
- This model is well-suited for identifying patterns and relationships between transaction amount, initial balance, and balance after a transaction. 
- Its flexibility allowed  us to create a customizable neural network architecture.

### Model Architecture
Our sequential model consisted of three layers with a total of 2,941 trainable parameters.  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/model_structure.png)

## Model Training and Evaluation
Due to the size of the dataset, we ran ten epochs during model training. The model achieved a loss of 0.0027400129474699497 and an accuracy of 0.9994659423828125.

### Linear Regression
After applying a random oversampler to our linear regression model, its performance decreased from 0.8904248433622179 to 0.8426175294757221. However, the resampled prediction showed improvement in identifying fraudulent cases.
- Initital Model  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/intial_linear_regression.png)
- Resampled Model  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/resampled_linear_regression.png)


## Conclusion

### Limitations
While all three models performed reasonably well with accuracy scores around 80%, our access to real-world data was limited. Additionally, the dataset provided only allowed training the models with features related to transaction amount and its impact on the sender and recipient's account balance.

### Summary of Findings
- The Keras Sequential model performed better overall, but this can be attributed to the imbalanced nature of the dataset. 
- Our [Tableau dashboard](https://public.tableau.com/app/profile/richard.moreno/viz/FraudDetectionDashboard_16865366705560/Dashboard) visualizations revealed a significant imbalance between fraudulent and non-fraudulent transactions.  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/fraud_piechart.png)
- Further research led us to explore data resampling techniques to address this issue, resulting in improved performance for the linear regression model.


## Instructions to Run Notebooks
- Both notebooks must be run using Colab.
- The following instructions will apply to both the tf_model.ipynb and sklearn_model.ipynb notebooks.
1. Before running the code, download the ["transactions_train.csv" file](https://drive.google.com/file/d/1wm5uV6MKiL-HvUJ3JntBucqjS4VdrASO/view?usp=sharing) and upload it to your Google Drive.
2. Start running the code from the first cell.
3. When prompted to mount your Google Drive, grant Colab permission to access the file.
4. **Do not run the following cell until you have changed the file path to match the location of the "transactions_train.csv" file in your Google Drive.**  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/drive_cell.png)
5. To change the file path, click the "Files" button in Colab.  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/Files_image.png)
6. Open the folder where you have the "transactions_train.csv" file, and click the three buttons on the side.  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/Three_buttons_image.png)
7. Select "Copy path"  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/copy_path_image.png)
8. Paste it inside the single quotes in the cell.
   - You will need to replace the path already within the quotes.  
![alt text](https://github.com/Adrian-Stahl/Project-4/blob/main/Images/file_path_image.png)
9. Run the cell.
10. Afterwards, you will be able to run all cells normally.




