💤 Sleep Disorder Detection & Quality Clustering using KMeans + Random Forest
This project analyzes sleep data to identify and classify sleep disorders based on extracted features and clustering. It involves:

1) Stage-wise generation of Light, Deep, and REM sleep durations
2) Clustering using KMeans to categorize sleep quality
3)Classification using Random Forest to detect sleep disorders
4)Evaluation of performance across different quality groups (low, medium, high)

📁 Dataset
The dataset should contain the following columns (at a minimum):
Sleep Duration
Quality of Sleep
Blood Pressure (format: Systolic/Diastolic)
Gender, Occupation, BMI Category
Sleep Disorder

🚀 Project Pipeline
1. Sleep Stage Estimation
Each user's Sleep Duration is randomly distributed into:
Light Sleep
Deep Sleep
REM Sleep
Based on the dataset index, rows are grouped into 3 clusters with different baseline distributions.

2. Clustering Sleep Patterns
A 3D K-Means clustering is performed using (Light, Deep, REM) values.
Clusters are labeled based on average Quality of Sleep scores.
Each row is assigned a quality label:
0 = Low Quality
1 = Medium Quality
2 = High Quality

3. Data Preprocessing
Blood Pressure is split into Systolic BP and Diastolic BP.
Categorical columns like Gender, Occupation, and BMI Category are encoded.
Sleep Disorder is converted into a binary label (1 = has disorder, 0 = none).

4. Classification
For each sleep quality category:
SMOTE is used for balancing the dataset.
Random Forest classifier is trained to predict sleep disorder presence.
Performance is evaluated using accuracy, precision, recall, and F1-score.

📊 Outputs
KMeans clustering visualized in a 3D scatter plot
Confusion matrices for all quality categories
Classification reports for each sleep quality group
Metrics summary table comparing performance

🛠️ Libraries Used
numpy, pandas, matplotlib, seaborn
sklearn (KMeans, RandomForest, LabelEncoder, StandardScaler, train_test_split, classification metrics)
imblearn for SMOTE oversampling

🧠 Insights
Clustering sleep stages gives better context to how sleep quality affects disorders
Classifier performance varies with sleep quality
Helps prioritize intervention for users in low-quality clusters

💡 Future Improvements
Introduce more granular features (e.g., wake-up count, time in bed)
Use deep learning models (e.g., LSTM) for temporal sleep pattern analysis
Add UI/UX for sleep disorder screening based on uploaded data

References:

https://ieeexplore.ieee.org/Xplore/home.jsp
https://ieeexplore.ieee.org/document/10212725/

Kohn TP, Kohn JR, Haney NM, Pastuszak AW, Lipshultz LI. The effect of sleep on 
men's health. Transl Androl Urol. 2020 Mar;9(Suppl 2):S178- S185. doi: 
10.21037/tau.2019.11.07. PMID: 32257858; PMCID: PMC7108988.

Zhang K(2023) Sleep staging model based on deep convolutional neural network and 
recurrent neural network. Information and Computer (Theoretical Edition), 35: 68-70. 

M. Suzuki et al., “Seasonal changes in sleep duration and sleep problems: A 
prospective study in japanese community residents,” Sleep, vol. 41, pp. A135–A135, 
04 2018.








