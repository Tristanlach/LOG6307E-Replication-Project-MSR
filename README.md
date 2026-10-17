# LOG6307E Replication Project

## Repository structure

```text
.
├── data/
│   ├── AIDev_Human_PRs/       # Parquet source data for humans
│   ├── rq1_metrics.csv        # Metrics used for research question 1
│   └── rq2_metrics.csv        # Metrics used for research question 2
├── figures/                   # Generated plots and figures
├── notebooks/
│   ├── 1_data_preparation.ipynb
│   └── 2_data_analysis.ipynb
├── report/                    # Project report
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation
```

The notebooks are numbered in their recommended execution order. The data preparation notebook processes the source data, while the data analysis
notebook produces the metrics and figures. Running `1_data_preparation.ipynb` before `2_data_analysis.ipynb` is optional because
the cleaned data required for the analysis are already included in `data/rq1_metrics.csv` and `data/rq2_metrics.csv`.

The human datasets are also included in the repository, so the notebooks can
be executed without manually downloading or adding them.

## Environment setup

Create a virtual environment from the repository root:

```bash
python3 -m venv .venv
```

Activate it:

**macOS/Linux**

```bash
source .venv/bin/activate
```

**Windows PowerShell**

```powershell
.venv\Scripts\Activate.ps1
```

Install the required libraries:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Running the notebooks

With the virtual environment activated, open and run the notebooks in order:

1. `notebooks/1_data_preparation.ipynb`
2. `notebooks/2_data_analysis.ipynb`

The human datasets required by the notebooks are included in the `data/AIDev_Human_PRs/` directory. The notebook `1_data_preparation.ipynb` loads the AI data automatically and prepares the data used by the analysis notebook.

## AI usage

AI tools were used to improve the grammar, formatting, language clarity, and to help with minor code debugging. The anlalysis, results, data collection and interpretations were all done verified by the authors.
