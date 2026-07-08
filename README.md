Car Price Prediction 🚗💰

A Machine Learning project for predicting used car prices based on car specifications such as brand, year, mileage, engine size, fuel type, transmission, and previous owners.
The project covers the full workflow of a regression problem, including data preprocessing, exploratory data analysis (EDA), feature encoding, model training, evaluation, and deployment using Streamlit.

📌 Project Overview

The goal of this project is to build a machine learning model that can estimate the price of a used car based on its key features.
The project starts with cleaning and exploring the dataset, then preparing the data for training, building a regression model, evaluating its performance, and finally saving the model for deployment in a Streamlit web app.

📂 Dataset Features

The dataset contains the following columns:

- Brand
- Year
- Mileage
- Engine_Size
- Fuel_Type
- Transmission
- Previous_Owners
- Price → Target variable

⚙️ Workflow

1) Data Loading

The dataset is loaded from "cars_data.csv" using Pandas.

2) Data Cleaning & Preprocessing

The following preprocessing steps were applied:

- Checked dataset shape, columns, and data types
- Handled missing values in Engine_Size using mean imputation
- Checked for duplicated rows and removed duplicates if found
- Removed extreme outliers from the Price column
- Reset the index after cleaning the data

3) Exploratory Data Analysis (EDA)

Several visualizations were created to better understand the dataset and the relationship between features and car price, including:

- Histograms for:
  - Engine_Size
  - Mileage
  - Price
- Count plots for:
  - Transmission
  - Brand
- Scatter plots between Price and:
  - Mileage
  - Engine_Size
  - Year
- Bar plots for:
  - Previous_Owners vs Price
  - Brand vs Price
- Correlation heatmap for numerical features
- Boxplots for outlier detection

4) Feature Encoding

Since the dataset contains categorical variables, encoding was applied before training the model:

- Label Encoding was used for:
  - "Brand"
  - "Fuel_Type"
  - "Transmission"

The encoders were also saved as ".pkl" files for later use in deployment.

5) Feature Scaling

Numerical features were scaled using StandardScaler before training.
The scaler was saved as "scaler.pkl".

6) Model Training

The dataset was split into training and testing sets using train_test_split, and then a RandomForestRegressor model was trained on the processed data.

7) Model Evaluation

The model was evaluated using R² Score.

- Model Used: "RandomForestRegressor"
- R² Score: 0.6986

8) Deployment

After training, the model was saved using pickle as:

- "car_price_model.pkl"

The project was then connected to a Streamlit app for interactive car price prediction.

🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pickle
- Streamlit

📁 Project Structure

Car_Price_Prediction/
│── Car_Price_Prediction.ipynb   # Main notebook containing preprocessing, EDA, training, and evaluation
│── cars_data.csv                # Dataset
│── car_price_model.pkl          # Saved trained model
│── scaler.pkl                   # Saved scaler
│── label_encoder_Brand.pkl      # Brand encoder
│── label_encoder_Fuel_Type.pkl  # Fuel type encoder
│── label_encoder_Transmission.pkl # Transmission encoder
│── app.py                       # Streamlit application
│── README.md                    # Project documentation

🎯 Model Input Features

The model predicts the car price based on the following input features:

- Brand
- Year
- Mileage
- Engine Size
- Fuel Type
- Transmission
- Previous Owners

📈 Model Performance

The trained model achieved an R² Score of 0.6986, which indicates a reasonable ability to predict car prices using the available dataset features.

▶️ How to Run the Project

1) Clone the repository

git clone https://github.com/TheMohamedFarag/Car_Price_Prediction.git
cd Car_Price_Prediction

2) Install the required libraries

pip install pandas numpy matplotlib seaborn scikit-learn streamlit

3) Open the notebook

Run the notebook file:

Car_Price_Prediction.ipynb

4) Run the Streamlit app

If the "app.py" file exists in the repository, you can launch the web app using:

streamlit run app.py

🚀 Future Improvements

Possible improvements for this project include:

- Trying additional regression models such as XGBoost or Gradient Boosting
- Performing hyperparameter tuning to improve accuracy
- Applying stronger feature engineering techniques
- Improving the Streamlit user interface
- Deploying the app publicly for easier access

👨‍💻 Author

Mohamed Farag
Computer Science Student | Data Science & AI Enthusiast

🔗 Repository Link

"GitHub Repository" (https://reference-url-citation.invalid/0)
