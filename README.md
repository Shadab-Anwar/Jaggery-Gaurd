# JaggeryGaurd 🌾
### AI-Powered Jaggery Quality Risk Intelligence Dashboard

JaggeryGaurd is an interactive dashboard for exploring jaggery quality non-compliance risk using information associated with the FSSAI *Pan India Jaggery Surveillance 2022* report. It combines risk visualisation, a sample risk calculator, model-comparison charts, and feature-importance analysis in one interface.

## Features

- **Interactive state-wise risk map** to explore predicted risk across Indian states and union territories.
- **Sample risk calculator** based on selected state, jaggery type, form, and sampling channel.
- **Model comparison** using accuracy, precision, recall, F1-score, and ROC-AUC.
- **ROC curve visualisation** for comparing classification models.
- **Confusion matrix** to review classification outcomes.
- **Feature-importance visualisation** to explore the relative influence of model inputs.
- **Risk-band analysis** for low-, medium-, and high-risk categories.
- **Survey sample breakdown** by jaggery type and form.
- **Responsive interface** with light/dark theme support.

## Dataset Overview

The dashboard represents 3,060 samples using a breakdown by jaggery type and form:

| Jaggery type | Form | Samples |
|---|---|---:|
| Cane | Solid | 527 |
| Cane | Liquid | 343 |
| Cane | Powdered | 486 |
| Coconut | Solid | 521 |
| Date palm | Solid | 574 |
| Palm | Solid | 609 |
| **Total** | | **3,060** |

The dashboard is intended for exploratory analysis. Because the underlying rows are reconstructed from summary tables, they may not preserve the original sample-level relationships in the surveillance data.

## Machine Learning Workflow

The dashboard presents concepts used in a non-compliance classification workflow:

1. Structure and prepare the reconstructed survey information.
2. Encode categorical inputs such as state, jaggery type, form, and sampling channel.
3. Compare classification approaches.
4. Review metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.
5. Visualise ROC curves and a confusion matrix.
6. Explore feature importance and risk bands.
7. Present the results in an interactive dashboard.

### Models represented

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- Support Vector Machine (SVM)

**Metric note:** Displayed scores should be considered illustrative unless they are replaced with metrics produced by actual model training and evaluation on a documented, held-out dataset.

## Technology Stack

- **HTML5** — page structure
- **CSS3** — layout, styling, responsive design, and themes
- **JavaScript** — interactions and client-side calculations
- **SVG** — ROC curve visualisation
- **Machine learning concepts** — classification evaluation and feature importance

The dashboard is delivered as a standalone HTML file and does not require a frontend build step.

## Run Locally

### Requirements
A modern web browser such as Chrome, Edge, or Firefox.

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/jaggeryguard.git
   ```

2. Open the project folder:

   ```bash
   cd jaggeryguard
   ```

3. Open `JaggeryGaurd.html` in your browser.

You can also use the **Live Server** extension in Visual Studio Code.

## Project Structure

```text
jaggeryguard/
├── JaggeryGaurd.html   # Interactive dashboard
├── README.md           # Project documentation
└── assets/             # Optional screenshots and images
```

## Potential Applications

- Exploratory analysis of food-surveillance information
- Visualising regional patterns in reported quality issues
- Demonstrating classification metrics and model explainability
- Prototyping a decision-support interface for food-quality monitoring

## Limitations

- The dataset is reconstructed from published summary tables, not original laboratory records.
- The dashboard does not contain verified sample-level measurements for moisture, sucrose, colour, contaminants, or other laboratory properties.
- A risk score is not proof that a sample is compliant or non-compliant.
- The displayed model metrics and explanations require verification against actual training and evaluation outputs.
- The dashboard should not be used for regulatory, commercial, or food-safety decisions.

## Future Research

Potential extensions include obtaining genuine sample-level laboratory data, incorporating physicochemical measurements, evaluating models with geographically independent test data, calibrating predicted probabilities, and validating the approach on new market samples.

## Author

**Shadab Anwar**  
Food Process Engineering  
National Institute of Technology Rourkela

## Data Source

Food Safety and Standards Authority of India (FSSAI), *Pan India Jaggery Surveillance 2022*.

## Disclaimer

JaggeryGaurd is an educational and exploratory project. It is not an official FSSAI product. Predictions and visualisations should not be interpreted as laboratory results, regulatory assessments, or food-safety guarantees.
