# ECG Analysis – Heartbeat Classification

This repository contains an end‑to‑end ECG analysis project that processes raw electrocardiogram (ECG) signals and summarizes them into features and CSV reports. The goal is to distinguish between different cardiac conditions using 12‑lead ECG and extended lead II recordings.

The project is designed as a **portfolio‑ready** piece: someone visiting the repo (e.g., a recruiter) can quickly understand the problem, data, and analysis workflow.

---

## Problem Statement

Given ECG recordings from multiple subjects, the task is to analyze the signals and support classification into the following categories:

- **Normal Person**
- **Abnormal Heartbeat**
- **History of Myocardial Infarction (MI)**

The project extracts meaningful features from ECG signals (time‑domain statistics, waveform characteristics, etc.) and compiles them into structured CSV summaries for further analysis or model building.

---

## Repository Structure

- `code.ipynb` – Main analysis notebook: loading ECG data, preprocessing, feature extraction, and generation of summary tables.
- `final_check_output/`
	- `FINAL_COMBINED_SUMMARY.csv` – Combined overview of all processed ECG records.
	- `summary_12_leads_complete.csv` – Summary features calculated from 12‑lead ECG signals.
	- `summary_extended_lead_II_complete.csv` – Summary features calculated from extended lead II recordings.
- `ECG Dataset/` – Raw ECG data (kept locally and **ignored in Git** to keep the repository lightweight).
- `requirements.txt` – Python dependencies.
- `.gitignore` – Excludes large datasets and intermediate artifacts from version control.

> Note: Only final summary CSVs and code are tracked; large per‑record CSVs and `.npz` files are ignored.

---

## Technical Overview

At a high level, the notebook performs the following steps:

1. **Data Loading** – Read ECG recordings from local folders (12‑lead ECG and extended lead II).
2. **Preprocessing** – Basic cleaning steps such as handling missing values and preparing signals for analysis.
3. **Feature Extraction** – Compute descriptive statistics and signal‑based features from each recording.
4. **Aggregation** – Combine per‑record features into consolidated summary CSVs under `final_check_output/`.

These outputs can then be used for:

- Exploratory data analysis (EDA) on ECG features.
- Prototyping classification models for cardiac condition prediction.

---

## Setup

1. **Clone the repository**

```bash
git clone https://github.com/DhavalPanchal252/ecg-analysis-project.git
cd ecg-analysis-project
```

2. **Create and activate a Python virtual environment** (recommended)

```bash
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
.
venv\Scripts\activate     # Windows PowerShell
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Add the ECG dataset (not included in the repo)**

Place the original ECG folders under `ECG Dataset/` following the structure you used during development (e.g., `Abnormal heartbeat/`, `History of MI/`, `Normal Person/`).

---

## Usage

1. Open `code.ipynb` in Jupyter Notebook or VS Code.
2. Verify that the `ECG Dataset/` directory is present locally with the required subfolders.
3. Run the notebook cells in order to:
	 - Load and preprocess ECG data.
	 - Extract features from 12‑lead and extended lead II recordings.
	 - Generate and update the summary CSV files in `final_check_output/`.

You can then load the generated CSVs into Python, Excel, or any analytics tool for further analysis and visualization.

---

## Notes

- The raw ECG datasets under `ECG Dataset/` and large intermediate CSV/NPZ files are **not** tracked in Git.
- Only lightweight artifacts (code, summaries, and configuration files) are included so the repository is easy to clone and review.
- If you add new scripts (e.g., for model training), consider placing them in a `src/` folder and updating this README accordingly.

---

## Possible Extensions

- Build and compare machine learning models (e.g., logistic regression, random forest, gradient boosting, or deep learning) using the extracted features.
- Perform additional signal processing (filtering, peak detection, HRV analysis).
- Add visualizations of ECG waveforms and feature distributions.
- Automate the pipeline as a Python package or command‑line tool.

These extensions can strengthen the project further for academic or portfolio use.
