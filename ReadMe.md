# Honey Type Classification by NMR – 400 MHz vs 700 MHz

This repository contains the analysis notebooks for the paper **“Comparative Performance of 400 MHz and 700 MHz ¹H NMR Spectroscopy for Honey Type Classification: A PLS‑DA Study with Open Commercial Data”**.

The study uses an open‑access dataset of 20 commercial honey samples  (honey bee and stingless bee) measured at both 400 MHz and 700 MHz. Principal Component Analysis (PCA) and Partial Least Squares‑Discriminant Analysis (PLS‑DA) are applied to compare the ability of the two field strengths to discriminate honey types.

---

## Repository Structure
Each notebook is self‑contained: it loads the data, preprocesses it, runs PCA, PLS‑DA with repeated k‑fold cross‑validation, bootstrap out‑of‑bag validation, permutation testing, VIP scores, and loading plots,and then saves all figures.

├── 400MHz_analysis.ipynb    # Full analysis for 400 MHz data <br>
├── 700MHz_analysis.ipynb    # Full analysis for 700 MHz data <br>
├── requirements.txt         # Python dependencies <br>
├── README.md                # This file <br>
└── data/                    # Data files <br>

## Dataset

The 1H NMR binned data were obtained from the Zenodo repository:

> Maulidiani, M. (2024). *1H NMR Data of Commercial Honey Analysed by  
> 400 and 700 MHz Spectrometers* (Version v2) [Data set].  
> Zenodo. https://doi.org/10.5281/zenodo.10969320

**Files required** (download from the link above):
- `NMR Binning Data commercial honey 400MHz.xlsx`
- `NMR Binning Data commercial honey 700MHz.xlsx`

Place them in the same directory as the notebooks, or update the  
`file_path` variable inside each notebook to point to the correct location.

---

## Environment Setup

The analysis was performed with **Python 3.11.2** and the following libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit‑learn

To install them run: `pip install -r requirements.txt`
 

### Core references: 

- **Dataset:** Maulidiani, M. (2024). *1H NMR Data of Commercial Honey Analysed by 400 and 700 MHz Spectrometers* (Version v2) [Data set]. Zenodo. [https://doi.org/10.5281/zenodo.10969320](https://doi.org/10.5281/zenodo.10969320)

- **Water region removal:** Beckonert, O., Keun, H. C., Ebbels, T. M. D., Bundy, J., Holmes, E., Lindon, J. C., & Nicholson, J. K. (2007). Metabolic profiling, metabolomic and metabonomic procedures for NMR spectroscopy of urine, plasma, serum, and tissue extracts. *Nature Protocols*, *2*(11), 2692–2703.

- **Metabolomics reporting practices:** Powers, R., Andersson, E. R., Bayless, A. L., Brua, R. B., Chang, M. C., Cheng, L. L., … Quality Control Consortium. (2024). Best practices in NMR metabolomics: Current state. *TrAC Trends in Analytical Chemistry*, *171*, 117478.

- **PLS‑DA cross‑validation:** Westerhuis, J. A., Hoefsloot, H. C. J., Smit, S., Vis, D. J., Smilde, A. K., van Velzen, E. J. J., … van Dorsten, F. A. (2008). Assessment of PLSDA cross validation. *Metabolomics*, *4*(1), 81–89.

- **Permutation test validation:** Szymańska, E., Saccenti, E., Smilde, A. K., & Westerhuis, J. A. (2012). Double‑check: validation of diagnostic statistics for PLS‑DA models in metabolomics studies. *Metabolomics*, *8*(Suppl 1), S3–S16.

- **Pareto scaling justification:** Alghamdi, A., Gray, A., & Watson, D. (2019). Investigation of metabolomics techniques by analysis of MS propolis data: which pre‑treatment method is better? *Advances and Applications in Statistics*, *58*(1), 13–34.