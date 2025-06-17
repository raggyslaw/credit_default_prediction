<h1 align="center">💳 Credit Default Risk Prediction</h1>

<p align="center">
  A complete machine learning pipeline to identify high-risk credit customers.<br>
  Focused on minimizing missed defaulters using <b>F2-score</b> and domain-aware modeling.
</p>

<hr>

<h2>🚀 Project Overview</h2>
<p>
  This project was built to predict whether a credit card customer is likely to default next month. It combines advanced financial feature engineering, class balancing using SMOTE, model training with threshold optimization, and final selection based on real-world financial risk considerations.
</p>

<ul>
  <li><strong>Goal:</strong> Minimize undetected defaulters (false negatives)</li>
  <li><strong>Primary Metric:</strong> F2-Score</li>
  <li><strong>Final Models:</strong> Voting Classifier and Calibrated Classifier (based on business tolerance)</li>
</ul>

<h2>📊 Workflow Summary</h2>
<ol>
  <li><b>EDA</b> — Financial trend analysis, distribution study, outlier detection</li>
  <li><b>Feature Engineering</b> — 17 custom behavior-based features (e.g., delay streak, bill volatility, repayment ratios)</li>
  <li><b>Preprocessing</b> — Outlier treatment, encoding, scaling, SMOTE-based balancing</li>
  <li><b>Model Training</b> — Logistic Regression, Decision Trees, Random Forest, XGBoost, LightGBM</li>
  <li><b>Tuning & Calibration</b> — RandomizedSearchCV, threshold sweeping, calibration (Platt scaling / isotonic)</li>
  <li><b>Ensemble & Evaluation</b> — Voting Classifier, confusion matrix, F2 vs Accuracy plots, PR curves</li>
</ol>

<h2>🎯 Final Outcome</h2>
<ul>
  <li><b>Voting Model:</b> Aggressive — flags more defaulters; ideal for risk-averse firms</li>
  <li><b>Calibrated Model:</b> Balanced — closer to actual default rate; better for realistic applications</li>
</ul>

<h3>📌 Business-Side Summary</h3>
<p>
  The model reflects real-world tradeoffs:
</p>
<ul>
  <li><b>False Negatives (missed defaulters)</b> → high financial risk (to be minimized)</li>
  <li><b>False Positives (false alerts)</b> → customer dissatisfaction or revenue loss</li>
</ul>

<p>
  The <b>F2-score</b> was chosen over F1/Accuracy to align with credit risk goals. ROC-AUC was monitored, but not used for model selection.
</p>

<h2>📁 Repository Structure</h2>
<pre>
├── data/                  # Raw and processed datasets
├── notebooks/             # Jupyter notebooks for EDA, modeling, tuning
├── models/                # Saved models (optional)
├── utils/                 # Custom functions and feature generators
├── outputs/               # Results, visualizations, and reports
├── requirements.txt       # Python dependencies
└── README.md              # You're here!
</pre>

<h2>🧪 Tech Stack</h2>
<ul>
  <li><b>Python 3.10</b>, NumPy, Pandas, Scikit-learn, XGBoost, LightGBM</li>
  <li>Seaborn & Matplotlib for data visualization</li>
  <li>Imbalanced-learn for SMOTE and class balancing</li>
</ul>

<h2>📌 Key Highlights</h2>
<ul>
  <li>✅ 17+ domain-specific features engineered</li>
  <li>✅ Business-aware model evaluation with risk-cost tradeoffs</li>
  <li>✅ Dual-model strategy (Voting vs Calibrated) for practical use</li>
  <li>✅ Cross-validation and threshold optimization applied</li>
</ul>

<h2>📄 License</h2>
<p>This project is released under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.</p>

<hr>
<p align="center">
  Built with 💡 for FinClub Summer 2025 Project • Credit Risk Intelligence
</p>
