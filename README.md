# DevelopersHub AI/ML Engineering Internship Tasks

Completed tasks for the DevelopersHub Corporation AI/ML Engineering Internship.

---

## Task 1 – Exploring and Visualising the Iris Dataset

**Objective:** Load, inspect, and visualise the Iris dataset to understand data trends and distributions.

**Dataset:** Iris Dataset (loaded via `seaborn`)

**Notebook:** `task1_iris_eda.ipynb`

**Key steps:**
- Loaded dataset with pandas; inspected shape, dtypes, and descriptive statistics
- Checked for missing values and class balance
- Visualised feature relationships using a pairplot and scatter plot
- Plotted value distributions using histograms per species
- Identified outliers using box plots
- Computed a correlation heatmap

**Key findings:**
- Dataset is clean (no missing values) with 150 balanced samples across 3 species
- Petal length and petal width are the most discriminative features (r = 0.96 between them)
- Iris Setosa is clearly separable from the other two species in petal space
- Sepal width is the weakest separating feature

---

## Task 2 – Predict Future Stock Prices (Short-Term)

**Objective:** Use historical stock data to predict the next day's closing price.

**Dataset:** Apple (AAPL) historical data fetched via `yfinance` (2020–2024)

**Models:** Linear Regression and Random Forest Regressor

**Notebook:** `task2_stock_prediction.ipynb`

**Key steps:**
- Fetched 5 years of OHLCV data using the `yfinance` API
- Engineered features: daily return, price range, 5-day & 20-day moving averages, 5-day rolling volatility
- Split data chronologically (80/20) — no shuffling to preserve time order
- Scaled features using StandardScaler
- Trained and compared Linear Regression vs Random Forest
- Evaluated with MAE, RMSE, R², and MAPE
- Visualised actual vs predicted closing prices and feature importances

**Key findings:**
- Random Forest outperforms Linear Regression by capturing non-linear price dynamics
- `Close`, `MA5`, and `MA20` are consistently the most important features
- Both models track general price trends well but may lag during sharp market movements

---

## Task 4 – General Health Query Chatbot

**Objective:** Build a chatbot that answers general health-related questions using prompt engineering and a free LLM.

**Model:** `llama-3.3-70b-versatile` via Groq API (free, no credit card required)

**Notebook:** `task4_health_chatbot.ipynb`

**Key steps:**
- Configured Groq API with a free API key
- Designed a system prompt restricting the model to general health queries only
- Implemented a regex-based safety filter to block harmful queries before API calls
- Tested with example queries from the task brief plus edge cases
- Built an interactive chat loop for live testing

**Key results:**
- Chatbot provides clear, friendly, non-diagnostic health information
- Safety filter correctly blocks overdose, self-harm, and prescription-related queries
- LLaMA 3.3 70B on Groq delivers fast, high-quality responses completely free

---

## Setup Instructions

### Task 1
```bash
pip install pandas seaborn matplotlib
```

### Task 2
```bash
pip install yfinance scikit-learn pandas matplotlib
```

### Task 4
```bash
pip install groq
```
Get a free Groq API key at https://console.groq.com → API Keys → Create API Key.  
No credit card required. Paste the key into cell 2 of the notebook.

---

## Repository Structure

```
├── task1_iris_eda.ipynb
├── task2_stock_prediction.ipynb
├── task4_health_chatbot.ipynb
└── README.md
```
