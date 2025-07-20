## 📊 Student Performance Predictor using Multiple Linear Regression

### 📝 Project Overview:

This project aims to **predict student academic performance** using **Multiple Linear Regression**, based on a combination of academic and lifestyle-related factors. By leveraging a structured dataset that includes features like study hours, sleep time, past scores, and involvement in extracurricular activities, the model estimates a student's **Performance Index**, which can be used for targeted academic guidance and intervention.

---

### 🛠️ Technologies Used:

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn

---

### ✅ Core Highlights:

- **Multi-Feature Input**  
  Considers multiple influential parameters to predict performance outcomes.

- **Comprehensive Preprocessing**  
  Handles encoding of categorical variables and scales numerical features for model readiness.

- **Statistical Correlation Analysis**  
  Identifies key attributes that have the strongest influence on academic success.

- **Model Evaluation Metrics**  
  Assessed using **R² Score** and **Mean Absolute Error** for better understanding of model reliability.

- **Intuitive Visualizations**  
  Helps understand data distribution and relationships using plots and heatmaps.

---

### 📂 Dataset Information:

- **Filename:** `[Student_Performance.csv]
- **Target Variable:** Performance Index  
- **Selected Features:**
  - Study Hours  
  - Sleep Time  
  - Previous Exam Scores  
  - Extracurricular Activity Participation  
  - Practice of Sample Question Papers

---

### 🔁 Workflow Breakdown:

1. **Loading & Cleaning Data**  
   - Handled missing values and checked data consistency.

2. **Encoding Categorical Fields**  
   - Converted non-numeric fields such as “Extracurricular Activities” into numerical formats.

3. **Exploratory Data Analysis**  
   - Used scatter plots and pairplots to visualize data distribution.

4. **Correlation Matrix & Feature Selection**  
   - Created a heatmap and selected top features based on correlation with the target.

5. **Feature Normalization**  
   - Used **MinMaxScaler** to scale numerical inputs within a standard range.

6. **Model Training**  
   - Applied **Linear Regression** using Scikit-learn’s implementation.

7. **Performance Evaluation**  
   - Evaluated the model using:
     - **R² Score** – to assess model fit  
     - **Mean Absolute Error** – to understand average prediction error

---

### 📈 Visual Output:

- 🔹 **Scatter Plots:** Show trends between individual input features and predicted score  
- 🔹 **Heatmap:** Visualizes correlations between features and target variable

---

### 🧪 Results Summary:

- **R² Score:** Depends on train/test split  
- **MAE (Mean Absolute Error):** Varies with data distribution

---

### 🔮 Future Enhancements:

- Try **Polynomial Regression** or **Random Forest** for improved accuracy  
- Add more features like **socioeconomic factors**, **family background**, etc.  
- Deploy as a web app using **Streamlit** or **Flask**

