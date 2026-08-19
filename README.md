# microPuberty

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Analytical code for **"Individual differences in brain microarchitecture related to pubertal hormone"**.

Using data from 7,457 youth (ages 9–13 years) in the **Adolescent Brain Cognitive Development℠ (ABCD) Study**, this project applies sex- and age-stratified multi-task elastic net regression to link salivary hormone levels (DHEA, testosterone, estradiol) and physical maturation (PDS) to Restriction Spectrum Imaging (RSI) metrics of cellularity (RNI) and neurite density (RND).

---

## Repository Structure

```
AllenBrainSummary.py   # CNS receptor expression based on data from the Allen Brain Atlas's Developmental Transcriptome
data_grabber.py        # Creating the subset of ABCD Study data used here, using 62442katieb/ABCDWrangler
data_cleaning.py       # Quality control, filtering, wrangling, and outlier detection
multitask_enet.py      # Primary data analysis pipeline with permutation-based feature importance
relevance_plots.py     # Plots resulting importance of each brain region per model
relevance_tables.py    # Distills importance across permutations into a table
mri_varnames.json      # Maps variable names to human-readable brain region names
requirements.txt       # pip package lock, for posterity (and transparency (and reproducibility))
```

## Data Availability
All code for data processing, statistical modeling, and figure generation is fully available in this repository.

However, neuroimaging, hormone, and phenotypic data are from the ABCD Study (release v5.1), which is restricted and hosted on the NIMH Data Archive (NDA). Access requires an approved NDA Data Use Certification (DUC).

There is a slim chance that this codebase will be updated to use 7.1+ data in the course of revisions, but don't hold your breath.
