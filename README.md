# Volatility-Forecasting

Data Science Project Proposal: Financial Trading Strategy Development

Data Scientist: Christian Ingul, Anthony Navarro

Objective:
The project aims to develop, test, and deploy an automated trading strategy utilizing advanced data science and machine learning techniques. The process will leverage financial data extraction, preprocessing, exploratory data analysis (EDA), feature engineering, model development, backtesting, and deployment on a cloud platform for real-time trading.

Timeline:
- Duration: Spring Break plus two additional weeks.
- Phases: The project is divided into four main phases for structured completion.

Phase 1: Data Preparation and Exploration

- Data Extraction: Retrieve financial data from Quantitative Trading Google Drive, ensuring data is in a format conducive to analysis. Currently, the data is stored in time stamped feather files with features related to SPY (one day at a time). The extraction will require nuanced code for looping through the data folder to build a chronological dataset. Additionally, we will have to merge the target feature chronologically with our features. The target variable is in a separate file, which I will post on my GitHub.

- Exploratory Data Analysis (EDA): Conduct thorough EDA to understand underlying patterns, correlations, and distribution in the data. This will include statistical summaries, visualization, and initial hypothesis forming. I see this part of the project being particularly challenging given it is high dimensional and noisy. I suggest we bucket the various features into respective financial features such as spreads, features, equities, bonds, etc. 

- Data Dictionary: If necessary we can work to build out a comprehensive data dictionary explaining features and target variables.

Phase 2: Data Preprocessing and Feature Engineering

- Data Cleaning and Preprocessing: Apply techniques to limit extreme values, imputation for handling missing values, and general data cleansing to enhance data quality.

- Feature Engineering: Employ dimensionality reduction techniques like LASSO (Least Absolute Shrinkage and Selection Operator) and PCA ( Principal Component Analysis) to identify and select relevant features for model training. We can also explore using an autoencoder structure to generate PC’s. A new research paper from Polish researchers suggests the application of Lasso PCA, which is using LASSO on PC’s after initial PCA.

Phase 3: Model Development and Evaluation 

- Model Architecture: Design and implement a sophisticated encoder-decoder architecture alongside other deep learning methodologies tailored for financial time series prediction. Additionally, we can leverage shallow models such as Random Forest, XGBoost, etc. to benchmark our DL models.

- Model Training and Evaluation: Train models using the processed dataset, followed by rigorous backtesting to evaluate performance against historical data. Our comparison model will be the benchmark model including a selection of features (I will explain).

- Trading Strategy Development: Utilize insights and predictions from the model to formulate a comprehensive trading strategy.

Phase 4: Deployment and Real-time Trading

- Cloud Deployment: Migrate the model and trading strategy to AWS (Amazon Web Services) to leverage cloud computing for scalability, reliability, and real-time trading capabilities. Amazon Sagemaker would be the correct cloud application for this type of deployment.

- Experience Gaining: Utilize the deployment phase as an opportunity to gain practical experience with cloud platforms, automated trading systems, and real-time data processing. We can also loop in Austin Pollok and the stakeholder (Kevin), which may be willing to provide capital, or sponsor the project based on our results.


Expected Outcomes:

- A fully functional automated trading system that can predict SPY option volatility movements with high accuracy.
- Experience in deploying and managing machine learning models in a cloud environment for real-time applications.

Milestones:

- Week 1-2: Data extraction, EDA, and initial preprocessing.
- Week 3: Advanced data preprocessing and feature engineering.
- Week 4-5: Model development, training, and backtesting.
- Week 6: Deployment on AWS and initial real-time trading tests.

Quantitative Trading Class Drive
https://drive.google.com/drive/folders/1UsynFmMuGAarQC5r-A2wFXgVn2OoLXCd?usp=sharing

How to find raw data in the drive: “Input_Data” -> “Features_Per_Ticker_Per_Day” -> “SPY_84398”.

