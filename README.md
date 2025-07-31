# UC-with-biostatistics
# 🧠 UC Remission Predictor & Treatment Recommender

This is a simulation-based AI tool that predicts the likelihood of remission in Ulcerative Colitis (UC) patients based on clinical and lab variables, and recommends the optimal treatment path—**biologics vs steroids**.

The tool is trained using a synthetic dataset (simulating 100–500 patients) and utilizes machine learning (XGBoost classifier) along with biostatistical methods to assign real-time probabilities and interpret relationships between features like CRP, albumin, comorbidities, and treatment outcomes.

---

## 💡 Why This Project?

Despite rapid advancements in medicine, **individualized treatment decisions** in complex diseases like UC still depend heavily on trial-and-error.

We wanted to simulate what happens if we equip a model with:
- A trained brain to **assign weights** to meaningful variables
- The ability to **suggest treatment** (biologics vs steroids)
- Integrated **biostatistics** for transparent and explainable inference
- Future readiness to power **clinical trial simulations**

---

## 🛠️ What We Built

| Component | Details |
|----------|---------|
| ML Model | XGBoost Classifier trained on synthetic UC dataset |
| Visual Explainability | SHAP waterfall plots |
| Treatment Simulation | Binary treatment arm (Steroids = 0, Biologics = 1) |
| Biostatistics | Logistic regression, chi-square tests, feature significance with p-values |
| Interface | Gradio app with sliders, checkboxes, and auto-generated graphs |
| Dataset | 100-500 synthetically generated patients, simulating real-world complexity |
| Output | Remission probability + Graphical explanation of most influential features |

---

## 🧪 Clinical Trial Simulation

The tool was built with a vision that goes beyond standard prediction.

> It can serve as a **base simulation engine** for future **AI-driven clinical trials**, where different patient profiles are entered, and outcome probabilities are simulated based on prior data patterns.

In the future:
- Real data can replace synthetic inputs
- Treatment arms can expand (small molecule, JAK inhibitors, etc.)
- Outcome types can include mucosal healing, hospitalization, surgery avoidance

---

## 📊 Integrated Biostatistics

We added classical **biostatistical validation** to the model pipeline to strengthen scientific credibility:

- **Logistic Regression** was used to understand the independent effect of each covariate on remission
- **Chi-square and T-tests** were used to compare group distributions and detect significant features
- Output includes **p-values and odds ratios** to support findings from the ML model

> This ensures **scientific robustness** and supports causality hypotheses, bridging ML with traditional EBM.

---

## 💻 Usage

Launch it in Google Colab:

```python
!pip install shap xgboost gradio --quiet
