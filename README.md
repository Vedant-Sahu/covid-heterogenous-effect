# The Heterogeneous Impact of COVID-19 Lockdowns: Evidence from India's Scheduled Castes and Tribes

**Collaborators:** Dhananjay Balakrishnan, Vedant Sahu  
**Contact:** dhananjb@stanford.edu, vsahu@stanford.edu

## Project Description

India's COVID-19 lockdowns created an unprecedented economic shock, but did all communities experience it equally? This project examines whether marginalized populations, specifically Scheduled Castes and Scheduled Tribes (SC/ST), suffered disproportionately larger impacts on health and socioeconomic outcomes compared to privileged caste groups.

We leverage a natural experiment in India's National Family Health Survey (NFHS-5), which surveyed different districts before versus during the pandemic. Using difference-in-differences estimation, we identify the causal effects of COVID-19 lockdowns and estimate heterogeneous treatment effects across India's caste hierarchy.

## Data Sources

### National Family Health Survey (NFHS)
- **NFHS-4 (2015-16):** Baseline data across all districts
- **NFHS-5 (2019-2021):** Split into two phases: pre-pandemic and post-pandemic

**Data Access:** [The DHS Program](https://dhsprogram.com/)

## Repository Structure

```
covid-heterogenous-effect/
│
├── data/                         # All data files (raw data not tracked by git)
│   ├── raw/                      # Original NFHS data files
│   │   ├── nfhs4/                # NFHS-4 (2015-16) datasets
│   │   └── nfhs5/                # NFHS-5 (2019-21) dataset
│   └── processed/                # Cleaned and aggregated datasets
│
├── code/                         # All analysis scripts
│   ├── 01_data_processing/       # Data cleaning and aggregation
│   ├── 02_exploratory/           # Exploratory data analysis and visualization
│   ├── 03_analysis/              # Main causal inference analysis
│   └── 04_visualization/         # Publication-ready figures and tables
│
├── results/                      # All outputs 
│   ├── figures/                  # Plots and visualizations
│   ├── tables/                   # Regression tables and summary statistics
│   └── models/                   # Saved model objects and estimates
│
├── notebooks/                    # Jupyter notebooks for exploration
│
├── docs/                         # Documentation
│   └── Project_Proposal.pdf      # Original project proposal
│
├── .gitignore                    # Specifies files to exclude from version control
├── environment.yml               # Conda environment specification
├── LICENSE                       # MIT License
└── README.md                     # This file
```

**Note:** Raw data files are excluded from git tracking to protect sensitive survey data. See `.gitignore` for details.

## Getting Started

### Prerequisites

- **Miniconda or Anaconda** installed ([Download here](https://docs.conda.io/en/latest/miniconda.html))
- **Git** for version control
- **VS Code** (recommended) or your preferred IDE
- **DHS Program account** for NFHS data access (registration required)

### Step 1: Clone the Repository

```bash
git clone https://github.com/Vedant-Sahu/covid-heterogenous-effect.git
cd covid-heterogenous-effect
```

### Step 2: Set Up Python Environment

**Using Conda:**

```bash
# Create environment from specification file
conda env create -f environment.yml

# Activate the environment
conda activate covid-heterogenous-effect

# Verify installation
python -c "import pandas, statsmodels, dowhy; print('Environment ready!')"
```

### Step 3: Download NFHS Data

1. **Register for DHS access:**
   - Visit [The DHS Program](https://dhsprogram.com/)
   - Create an account and request access to India datasets
   - Approval typically takes 24-48 hours

2. **Download required datasets:**
   - NFHS-4 (2015-16): Household and Individual Recodes
   - NFHS-5 (2019-21): Household and Individual Recodes

3. **Organize data files:**
   ```
   data/raw/
   ├── nfhs4/
   └── nfhs5/
   ```

**Important:** Raw data files are automatically excluded from git tracking (see `.gitignore`).

## Related Literature

- Banerjee & Mishra (2023): Spousal violence during COVID-19 using NFHS data
- Banerjee & Mishra (2024): Intimate partner violence and reproductive health
- Deshpande & Bhardwaj (2021): Descriptive insights from NFHS-5
- Deshpande & Ramachandran (2023): COVID-19 and caste inequalities

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Last Updated:** November 2025
