# ECG Analysis Project

This repository contains code and summary outputs for an ECG analysis project.

## Project Structure

- `code.ipynb` – Main analysis notebook.
- `final_check_output/` – Generated summary CSV files and intermediary outputs.
- `ECG Dataset/` – Raw ECG data (ignored from Git to keep the repository lightweight).

## Setup

1. Create and activate a Python virtual environment (optional but recommended).
2. Install dependencies:

```bash
pip install -r requirements.txt
```

## Usage

- Open `code.ipynb` in Jupyter or VS Code and run the cells in order.
- Summary CSVs are written to `final_check_output/`.

## Notes

- Raw datasets under `ECG Dataset/` and large intermediate CSV/NPZ files are **not** tracked in Git.
- If you add new scripts, place them alongside the notebook or in a `src/` folder and update this README accordingly.
