# National Poll on Healthy Aging (NPHA) Doctor Visits Analysis

## ⚕️ Introduction

This project delivers an interactive Streamlit dashboard designed to provide meaningful insights into the health, well-being, and healthcare utilization of older adults in the USA. Utilizing data from the **National Poll on Healthy Aging (NPHA)**, the application serves as a tool for healthcare policymakers and insurance providers to make data-driven, well-informed decisions.

The primary objective is to analyze healthcare utilization patterns among older Americans by addressing key questions through the dashboard:

1.  **Attributes Leading to Doctor Visits**: Identifying which attributes are associated with a higher frequency of doctor visits.
2.  **Bias in Demographic Features**: Assessing whether the dataset is biased in terms of race and gender distribution.
3.  **Relation Between Health Features**: Exploring the relationship between physical and mental health.
4.  **Impact of Dropping Sensitive Features**: Evaluating how excluding sensitive features like race and gender affects feature importance and model predictions.
5.  **Overall Health Status Based on Demographics**: Determining the overall health status across different demographic factors.
6.  **Low Doctor Visits Despite Poor Health**: Identifying subsections of the population with poor health but low doctor visit frequency to help policymakers provide targeted benefits.

---

## 🚀 Key Features

*   📊 **Explore the Dataset**: Get a comprehensive overview of the NPHA dataset, including its summary, key features, and a data snippet.
*   📈 **Understand Traits and Trends**: Utilize interactive visualizations like bar plots, pie charts, and histograms to understand demographic distributions and relationships between variables.
*   ⚙️ **Train a Customized ML Model**: Train a Random Forest Classifier to predict the number of yearly doctor visits. Users can retrain the model after excluding sensitive attributes like 'Gender' and 'Race'.
*   🔍 **Make Live Predictions**: Use the "Making A Prediction" interface to input custom data and receive real-time predictions from the trained model.
*   🔄 **Compare Prediction Scenarios**: Instantly see how changing one or more input parameters affects the model's prediction probabilities with a "Current vs. Previous Prediction" comparison view.
*   ⚖️ **Analyze and Correct Bias**: The "Bias Correction" section demonstrates how Random Over-Sampling can be used to address uneven class distributions for features like 'Race' and 'Employment'.

---

## 📄 About the Dataset

The dataset originates from the University of Michigan's **National Poll on Healthy Aging (NPHA)**, which collects data on health, healthcare, and policy issues affecting Americans aged 50 and older. The subset used for this project contains **714 records** and **14 attributes**, curated for developing and testing machine learning algorithms to predict the number of doctor visits per year.

-   **Creators**: Preeti N. Malani, Jeffrey Kullgren, and Erica Solway (University of Michigan).
-   **Date Collected**: April 2017.
-   **Funding**: AARP and Michigan Medicine.
-   **Collection Method**: Conducted by the GfK Group using the KnowledgePanel, a probability-based web panel representative of the US population.
-   **Target Variable**: `Number of Doctors Visited` (Categorical: '0-1', '2-3', '4 or more').
-   **Protected Attributes**: The dataset includes sensitive attributes such as Race, Gender, and Age, which require careful handling.

---

## 📂 Project Structure

The application is modularized into several Python files, each handling a specific page or functionality within the Streamlit app.

├── NPHA-doctor-visits.csv # The dataset file
├── main_app.py # Main application - handles page navigation
├── welcome.py # The landing/welcome page
├── npha.py # 'About the Dataset' page with summaries and stats
├── barplot.py # 'Exploring Data' page with interactive plots
├── model.py # 'Training a Model' page with model training and explainability (LIME/SHAP)
├── predict.py # 'Making a Prediction' page for user-input predictions
├── bias.py # 'Bias Correction' page demonstrating over-sampling
└── requirements.txt # Python dependencies

---

## 🛠️ Technologies & Libraries

*   **Application Framework**: Streamlit
*   **Data Manipulation**: Pandas, NumPy
*   **Data Visualization**: Matplotlib, Seaborn, Plotly Express
*   **Machine Learning**: Scikit-learn (RandomForestClassifier)
*   **Model Explainability**: LIME, SHAP
*   **Bias Handling**: imbalanced-learn (RandomOverSampler)

---

## 🚀 Getting Started

To run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    A `requirements.txt` file should be created with the following content:
    ```
    streamlit
    pandas
    plotly
    scikit-learn
    matplotlib
    seaborn
    lime
    shap
    imbalanced-learn
    ```
    Then, run the installation command:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Streamlit application:**
    ```bash
    streamlit run main_app.py
    ```
    The application will open in a new tab in your web browser.

---

## 🔮 Future Scope

*   **Enhanced Models**: Develop and integrate more sophisticated models (e.g., Gradient Boosting, Neural Networks) to improve prediction accuracy.
*   **Broader Applications**: Apply similar analytical methodologies to other age groups or different public health datasets.
*   **Policy Impact**: Collaborate with policymakers and healthcare organizations to translate insights from this dashboard into tangible healthcare improvements and policies.
*   **Model Performance with Balanced Data**: Fully implement the synthetically generated dataset (from the bias correction step) for training a new prediction model and formally analyze how the model's performance and fairness metrics are affected.
