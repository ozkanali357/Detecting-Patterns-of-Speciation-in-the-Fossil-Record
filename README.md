# Detecting Patterns of Speciation in the Fossil Record

## Project Overview
This data science project analyzes patterns of mammalian speciation over time and space using data from the NOW (New and Old Worlds) fossil database. The goal is to identify "species factories" - specific times and places that gave rise to exceptionally high numbers of new species during mammalian evolution.

## Data Source
The project uses data from the NOW fossil mammal database, which contains global information about Cenozoic land mammal taxa and localities. The dataset includes:
- Geographic coordinates of fossil localities
- Age estimates for each fossil
- Taxonomic information (genus and species)
- Occurrence data across multiple time periods

## Methodology
The analysis follows these key steps:
1. **Data Preprocessing**:
   - Cleaning invalid coordinates and unidentified species
   - Mapping fossils to Mammal Neogene (MN) time units
   - Assigning unique IDs to species and handling duplicates

2. **Occurrence Analysis**:
   - Identifying first occurrences of species in the fossil record
   - Calculating distribution of occurrences across time periods
   - Analyzing spatial distribution of fossil localities

3. **Logistic Regression**:
   - Modeling the relationship between previous sampling density and proportion of first occurrences
   - Calculating expected first occurrence rates based on sampling effort

4. **Statistical Significance Testing**:
   - Identifying localities with statistically significant high rates of first occurrences
   - Using binomial distribution to calculate p-values

## Results and Findings
The analysis revealed several interesting patterns:

- Significant first occurrences clustered in specific time periods (MN3-MN6 and MN13-MN16)
- Geographically, species factories were concentrated in:
  - The Iberian Peninsula across multiple time periods
  - Central Europe during MN3-MN5
  - The Mediterranean region in later periods (MN13-MN15)
- Significant localities often occurred at geographical boundaries, suggesting ecological changes may have driven diversification

## Technologies Used
- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib & Pyplot**: Data visualization
- **Geopandas**: Geographic data handling and mapping
- **SciPy**: Statistical testing
- **StatsModels**: Logistic regression modeling

## Setup and Installation
```bash
# Clone this repository
git clone https://github.com/yourusername/fossil-analysis.git

# Install dependencies
pip install pandas numpy matplotlib geopandas scipy statsmodels

# Run the notebook
jupyter notebook fossil_analysis.ipynb
