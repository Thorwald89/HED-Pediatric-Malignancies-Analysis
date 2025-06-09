# HED-Pediatric-Malignancies-Analysis

This repository contains the Jupyter Notebook used in the study "HLA Evolutionary Divergence and Pediatric Disease Risk: Unveiling Genetic Associations". This research investigates the association between HLA Evolutionary Divergence (HED) scores and the risk of pediatric hematological malignancies.

## Table of Contents

- [Project Overview](#project-overview)
- [Study Data](#study-data)
- [Code Structure](#code-structure)
- [Setup and Reproducibility](#setup-and-reproducibility)
- [Results and Figures](#results-and-figures)
- [Citation](#citation)
- [Contact](#contact)
- [License](#license)

## Project Overview

This study explores the relationship between HLA Evolutionary Divergence (HED) profiles and the incidence of various pediatric hematological malignancies. HED quantifies the evolutionary distance between HLA alleles, reflecting the functional diversity of an individual's HLA genotype. The project aims to identify specific HED patterns that may correlate with disease susceptibility in a cohort of 101 pediatric oncology patients.

## Study Data

Due to patient confidentiality and ethical considerations, raw clinical and HLA genotyping data from the study cohort cannot be directly shared in this repository. However, the analysis is performed on an Excel (XLSX) file with a specific structure.

**Input Data Format:**
The primary input file (e.g., `your_data_file.xlsx`) should be an Excel spreadsheet containing, at minimum, the following columns with these exact headers:

- `sample`: A unique identifier for each patient.
- `nome paziente`: Patient's name or identifier.
- `Alleles`: HLA alleles in a comma-separated string format (e.g., `A2402,A2601,B3502,B5501,C0401,C0102`).
- `HED_A`: HED score for HLA-A locus, as calculated from HLA-div.net.
- `HED_B`: HED score for HLA-B locus, as calculated from HLA-div.net.
- `HED_C`: HED score for HLA-C locus, as calculated from HLA-div.net.
- `Allele`: The HED profile categorization (e.g., `HHH`, `HLL`, `LHL`, `LLL`, etc.).
- `DISEASE`: The specific hematological malignancy diagnosis.
- `birthdate`: Patient's birthdate (date format).
- `sex`: Patient's sex.
- `datediagnosi`: Date of diagnosis (date format).
- `età alla diagnosi`: Age at diagnosis (calculated based on birthdate and datediagnosi).

**(Optional: If you plan to include a small, anonymized sample data file in the repository, you can add: "A small `sample_data.xlsx` file demonstrating the required format is provided in the `data/` directory for testing purposes.")**

## Code Structure

This repository contains the following key file:

- `HED Famiglie NUOVO.ipynb`: This is the main Jupyter Notebook containing the complete analysis, from data loading and processing to HED profile calculations, statistical analyses, and figure generation.

## Setup and Reproducibility

To reproduce the analysis, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Thorwald89/HED-Pediatric-Malignancies-Analysis.git](https://github.com/Thorwald89/HED-Pediatric-Malignancies-Analysis.git)
    cd HED-Pediatric-Malignancies-Analysis
    ```
2.  **Environment:**
    The analysis was primarily conducted using the **default Python 3.x environment provided by Google Colab**. While efforts have been made to ensure reproducibility, minor environment variations might occur if running locally. To ensure compatibility, it's recommended to use a Python 3 environment.

3.  **Install required packages:**
    The necessary libraries are typically pre-installed or easily installable within Google Colab. If running locally, you might need to install them:
    ```bash
    pip install pandas scipy matplotlib seaborn openpyxl
    ```
    *(Note: `openpyxl` is needed for reading .xlsx files with pandas).*

4.  **Prepare your input data:**
    Place your formatted Excel data file (e.g., `your_data_file.xlsx`) in the same directory as the `HED Famiglie NUOVO.ipynb` notebook, or adjust the file path within the notebook accordingly.

5.  **Run the analysis:**
    Open the `HED Famiglie NUOVO.ipynb` notebook in Google Colab or a local Jupyter environment (e.g., Jupyter Lab/Notebook) and execute all cells sequentially.

    [Open in Google Colab](https://colab.research.google.com/github/Thorwald89/HED-Pediatric-Malignancies-Analysis/blob/main/HED%20Famiglie%20NUOVO.ipynb) *(Note: This link will work once your notebook is pushed to the 'main' branch of your GitHub repo).*

## Results and Figures

Executing the notebook will perform all analyses and generate the figures presented in the corresponding manuscript, including:
- Distribution of HED scores per HLA locus (similar to Figure 1 in the manuscript).
- Heatmap visualizing the association between HED profiles and disease types (similar to Figure 2 in the manuscript).
- Outputs from statistical tests (e.g., Fisher's Exact Test results).

## Citation

If you use this code or data in your research, please cite the corresponding publication:

**[Your Article Title]**
---------

## Contact

For any questions or issues, please contact:
- [Dr. Donato Madalese] (d.madalese@santobonopausilipon.it)

## License

This project is licensed under the Mozilla Public License 2.0 (MPL-2.0) - see the `LICENSE` file for details in your repository.
