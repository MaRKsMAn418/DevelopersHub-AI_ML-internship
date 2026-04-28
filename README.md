# DevelopersHub-AI/ML_Internship_Tasks
---

# 🔹 Task 1: Exploring and Visualizing a Dataset

## 📌 Objective
To understand the dataset by performing Data Inspection, Statistical Analysis, and Visualization.

## 📂 Dataset Used
* Iris Dataset (loaded using `seaborn`)

## ⚙️ Work Performed
* Loaded dataset using `pandas`
* Explored dataset structure using `.shape`, `.head()`, `.info()`, `.describe()`
* Checked for missing values and class balance
* Created visualizations:
  * Scatter plots and Pairplot to show feature relationships
  * Histograms to show value distributions per species
  * Box plots to identify outliers
  * Correlation heatmap to highlight feature relationships

## 📈 Key Findings
* Dataset was clean with no missing values and 150 balanced samples across 3 species
* Petal length and petal width were the most discriminative features (r = 0.96)
* Iris Setosa was clearly distinguishable while Versicolor and Virginica had slight overlap
* Sepal width was the weakest separating feature across all species

## 📓 Notebook
`Task1.ipynb`

---

# 🔹 Task 2: Stock Price Prediction (Short-Term)

## 📌 Objective
To Predict the Next Day's Closing Stock Price using Historical Data.

## 📂 Dataset Used
* Stock market data fetched using `yfinance` (Apple – AAPL, 2020–2024)

## ⚙️ Work Performed
* Retrieved 5 years of historical OHLCV data via `yfinance` API
* Engineered features: Daily Return, Price Range, 5-day MA, 20-day MA, 5-day Volatility
* Applied chronological train-test split (80/20) — no shuffling to preserve time order
* Scaled features using `StandardScaler`
* Trained **Random Forest Regressor**
* Visualised actual vs predicted prices and feature importances

## 📊 Evaluation Metrics
* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score
* Mean Absolute Percentage Error (MAPE)

## 📈 Key Findings
* `Close`, `MA5`, and `MA20` were the most important features
* Stock price volatility limits perfect prediction accuracy

## 📓 Notebook
`Task2.ipynb`

---

# 🔹 Task 4: General Health Query Chatbot

## 📌 Objective
To Build a Chatbot that Answers General Health-Related Questions using Prompt Engineering and a Free LLM.

## 🛠️ Tools Used
* `llama-3.3-70b-versatile` model via **Groq API**

## ⚙️ Work Performed
* Configured Groq API with a free API key
* Designed a system prompt to restrict the model to general health queries only
* Implemented a regex-based safety filter to block harmful queries before API calls
* Tested with multiple example queries including edge cases
* Built an interactive chat loop for live testing in the notebook

## 🔒 Safety Design
* Safety filter screens every query before it reaches the model
* Blocked categories: overdose, self-harm, prescription advice, drug abuse
* Model is instructed never to diagnose conditions or recommend medications

## 📈 Key Results
* Chatbot provided clear, friendly, and non-diagnostic health information
* Safety filter correctly blocked all harmful query patterns
* LLaMA 3.3 70B on Groq delivered fast, high-quality responses completely free
* Prompt engineering significantly improved response tone and conciseness

## 📓 Notebook
`Task4.ipynb`

---

## 📁 Repository Structure
```
├── Task1.ipynb
├── Task2.ipynb
├── Task4.ipynb
└── README.md
```

---

# 👤 Author – Hamza Shafiq
AI/ML Engineering Intern – DevelopersHub Corporation
DHC-6448
