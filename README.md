# 📈 Cryptocurrency Analysis & Forecasting Dashboard

**Internship Project for Amdox Technologies**

This project is a comprehensive, multi-page Streamlit web application for analyzing cryptocurrency price trends and generating forecasts using multiple advanced time-series models.

![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white) ![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)

---

## 🚀 Key Features

* **Live Data:** Connects to the `yfinance` API to fetch the latest daily price data for Bitcoin (BTC-USD).
* **Exploratory Data Analysis (EDA):** Interactive charts for:
    * Historical Closing Price
    * 30 & 90-Day Simple Moving Averages (SMA)
    * Daily Volatility (Percentage Returns)
    * Histogram of Daily Returns
* **Multi-Model Forecasting:** Generates and visualizes forecasts from three different models:
    1.  **Prophet (by Meta):** A powerful model that accounts for daily seasonality (since crypto trades 24/7).
    2.  **ARIMA:** A classic statistical model (`auto_arima` is used to find the best parameters).
    3.  **LSTM (Deep Learning):** A Long Short-Term Memory neural network built with TensorFlow/Keras to learn complex, non-linear patterns.
* **Sentiment Analysis:** A dedicated page to analyze market sentiment.
    * Analyzes recent, pre-loaded news headlines.
    * Provides a live "Sentiment Analyzer" for you to input your own text.
* **Caching:** Uses Streamlit's `@st.cache_data` and `@st.cache_resource` to cache data and trained models, ensuring the app is fast and responsive after the first load.

---

## 🛠️ Technologies & Libraries

* **Core App:** Streamlit
* **Data & API:** `yfinance`
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn, Plotly (via `prophet`)
* **Statistical Modeling:** `pmdarima` (for auto_ARIMA)
* **Deep Learning:** `tensorflow` (Keras)
* **NLP/Sentiment:** `vaderSentiment`

---

## 🏁 Getting Started

To run this project on your local machine, follow these steps.

### 1. Prerequisite: Create `requirements.txt`

Before anyone can install the dependencies, you need to create a `requirements.txt` file. Run this command in your project's terminal:

```bash
pip freeze > requirements.txt
````

This will save all the libraries and their versions to a file, which you should add to your GitHub repo.

### 2\. Installation & Setup

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)
    cd YOUR_REPO_NAME
    ```

2.  **Create and activate a virtual environment (Recommended):**

    ```bash
    # Windows
    python -m venv venv
    .\venv\Scripts\activate

    # macOS / Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

### 3\. Run the App

Once everything is installed, run the following command in your terminal:

```bash
streamlit run app.py
```

Streamlit will open the app in your local web browser\!

-----

## ☁️ Deployment

This app is ready to be deployed\! The easiest way is to use **Streamlit Community Cloud**.

1.  Push your project (including `app.py`, `requirements.txt`, and any other files) to your GitHub repository.
2.  Go to `share.streamlit.io`.
3.  Sign up and link your GitHub account.
4.  Click "New app" and select your repository.
5.  Click "Deploy\!"

-----

## 🙏 Acknowledgements

This project was built as part of the Data Analytics internship program at **Amdox Technologies**, based on the provided project description for "Time Series Analysis with Cryptocurrency."
