# 🚇 Namma Metro Ridership Analysis: Statistical Inference & Time Series

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![SciPy](https://img.shields.io/badge/SciPy-Statistical%20Testing-lightgrey)

## 📌 Project Overview
This project performs an end-to-end statistical analysis of the daily ridership records for Bengaluru's Namma Metro. The primary objective is to evaluate the adoption rate of digital ticketing (QR codes) versus traditional tokens, mathematically validate commuter behavior patterns, and isolate cyclical seasonality for operational forecasting.

## 🎯 Key Objectives
1. **Commuter vs. Leisure Validation:** Use Hypothesis Testing to statistically prove behavioral differences between weekday commuters and weekend travelers.
2. **The "Payment War":** Track the cannibalization of physical tokens by digital QR ticketing systems.
3. **Operational Forecasting:** Isolate the underlying growth trend from the daily "noise" and weekly seasonality.

---

## 📂 Repository Structure

* **`01_Metro_Exploratory_Data_Analysis.ipynb`**
  * Data cleaning, handling date formats, and preliminary aggregations.
  * Descriptive statistics and distribution checks (KDE plots, Q-Q plots) to test for normality.
* **`02_Statistical_Inference_and_TimeSeries.ipynb`**
  * The core statistical engine of the project.
  * Contains T-Tests, ANOVA, Chi-Square analysis, and Time Series Decomposition.

---

## 🔬 Methodology & Statistical Tests

To ensure mathematical rigor, this project relies on advanced statistical inference rather than mere observation:

* **Welch’s T-Test:** Used to compare Weekday vs. Weekend ridership (chosen over Student's T-Test due to the non-normal distribution and unequal variance found in the EDA phase).
* **One-Way ANOVA & Tukey’s HSD:** Applied to compare ridership across all 7 days of the week, successfully isolating the homogeneous "Mid-Week Work Block."
* **Chi-Square Test of Independence:** Proved a statistically significant relationship between the *Day of the Week* and the *Preferred Payment Method*.
* **Additive Time Series Decomposition:** Deconstructed the timeline into *Trend*, *Seasonality* (7-day strict cycle), and *Residuals* (anomalies/holidays).

---

## 📊 Key Insights & Business Value

1. **The System is Strictly Commuter-Driven:** Statistical tests confirmed a massive, non-random drop in weekend ridership. The metro is primarily sustained by the Monday-Friday workforce, not tourists.
2. **Digital Adoption is Accelerating:** QR ticketing is rapidly capturing market share from physical tokens. Weekend travelers (casual users) show a higher propensity for tokens/QR, while daily commuters rely heavily on Smart Cards.
3. **Highly Predictable Seasonality:** The Time Series analysis revealed a strict 7-day cyclical "heartbeat," meaning BMRCL can highly optimize train frequency and station staffing based on these predictable drops.

---

## 📈 Visual Highlights


### The Rise of QR Ticketing (Substitution Effect)
> `[![Stacked Area Chart](path_to_your_stacked_chart.png)](https://github.com/RCB13/namma-metro-analysis/blob/main/03_Pay_Meth.png)`

### The 7-Day Transit "Heartbeat" (Time Series Decomposition)
> `[![Time Series](path_to_your_time_series_chart.png)](https://github.com/RCB13/namma-metro-analysis/blob/main/03_time_seri.png)`

---

## ⚙️ How to Run
1. Clone this repository:
   ```bash
   git clone [https://github.com/yourusername/namma-metro-analysis.git](https://github.com/yourusername/namma-metro-analysis.git)
   
2.Install the required dependencies:
Bash
pip install pandas matplotlib seaborn scipy statsmodels

3.Launch Jupyter Notebook or Google Colab to interact with the .ipynb files.
***
**Final Reminder:**
* Under `## 📈 Visual Highlights`, don't forget to replace the text inside the parentheses `()` with the actual image links you copied from GitHub!
* Update `yourusername` in the `git clone` link at the very bottom.
