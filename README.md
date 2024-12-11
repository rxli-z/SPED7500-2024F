# SPED7500-2024F

The project aims to analyze a dataset containing demographic, student-level, and family-professional partnership factors to predict student placement into tiers of support based on the Multi-Tiered Systems of Support (MTSS) framework. The analysis involves the following steps:

1. Data Processing:
The dataset is imported and processed using R, a statistical computing platform. Relevant variables are selected based on their theoretical alignment with MTSS tiers, including demographic characteristics, student challenges, and family-professional partnership factors. The data is cleaned to address missing or invalid responses, such as recoding skipped values and standardizing variable scales. Numeric and categorical variables are prepared for analysis.
2. Dimension Reduction:
An exploratory graph analysis (EGA) is conducted to identify underlying components within the data. Using the "leiden" algorithm and a graphical least absolute shrinkage and selection operator (GLASSO), five components are extracted: demographic characteristics, student behavioral challenges, family satisfaction, educational involvement, and school participation. Bootstrapping validates the stability of the components.
3. Cluster Analysis:
K-means clustering is applied to the components identified through EGA to group students into clusters. Each cluster aligns with one of the MTSS tiers, representing minimal, moderate, or intensive support needs. Cluster separation is visualized, indicating clear distinctions among student groups.
4. Predictive Modeling:
A multinomial regression model is trained on 70% of the dataset using cross-validation and bidirectional stepwise feature selection to determine the most predictive variables for MTSS tier placement. The remaining 30% of the data is used for model testing. The model’s accuracy and reliability are assessed using metrics such as sensitivity, specificity, precision, and F1 scores.
5. Visualization and Evaluation:
A confusion matrix and mosaic plot are generated to compare predicted and actual MTSS tier classifications. These visualizations highlight the model’s predictive performance and its ability to accurately reflect the support needs of diverse student populations.

The final results are summarized and exported for interpretation, offering insights into the relationship between family-professional partnerships and MTSS tier placement.
