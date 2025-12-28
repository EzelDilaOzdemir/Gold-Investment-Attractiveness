# 🏆 Gold-Investment-Attractiveness
A machine learning model using financial indicators that answers the question if gold is still a great longterm investment or if it is outdated. 

**📌 Overview**

This project is a quantitative valuation engine designed to estimate 6-month forward gold returns using macroeconomic fundamentals and an optimally weighted ensemble of statistical, machine learning, and deep learning models. Rather than relying on single-model price extrapolation, the system blends multiple modeling paradigms to form a structural, macro-conditioned valuation signal for gold.

**🧠 Research Motivation**

Gold is often perceived as outdated in the era of crypto, algorithmic trading, and high-frequency strategies.
This project investigates whether gold still responds systematically to macroeconomic drivers — and whether those relationships can be learned and forecasted using modern quantitative methods.

**🎯 Target Variable:** 6-Month Forward Gold Return

**📊 Macroeconomic Feature Set**

CPI:	Inflation (CPIAUCSL)
FEDFUNDS:	Federal Funds Rate
DFII10:	10-Year Real Yield
T10YIE:	Breakeven Inflation
M2SL:	Money Supply (M2)
^GSPC	S&P 500: Index
DX-Y.NYB	U.S. Dollar Index
SI=F:	Silver Futures

All features are resampled to monthly frequency.

**🏗️ Modeling Architecture**

ARIMA	for Statistical time-series structure
Random Forest	for Nonlinear macro-factor interactions
XGBoost	Gradient for boosting learning
LSTM for Neural Network	Long-term temporal dependencies

Each model captures a different structural aspect of gold price dynamics.

**🔴 Live Inference Logic**

The most recent 12 months of macro data are held out as a live input window.
The system generates a current 6-month expected gold return using trained models and optimized ensemble weights.

**📈 Final Output**: 6 Month EXPECTED GOLD RETURN (%): <predicted_value>

This value represents the macro-conditioned forward valuation signal.

⚙️ Installation

pip install numpy pandas yfinance pandas-datareader scikit-learn xgboost statsmodels tensorflow

▶️ How to Run

python gold_valuation_engine.py


**⚠️ Disclaimer**

This project is for educational and research purposes only and does not constitute financial advice.

**👩‍💻 Author**

Student researcher with strong interest in quantitative finance, macro modeling, and valuation analytics.
Open to feedback, research discussion, and collaboration.
