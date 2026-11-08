# Machine Learning

A collection of hands-on notebooks for exploring datasets, practicing data analysis, and learning machine-learning tools. Each topic has its own folder, and shared datasets belong in `assets/`.

## Repository contents

```text
Machine Learning/
|-- assets/                           # Shared datasets and project assets
|-- eda_titanic_dataset/
|   `-- data_analysis.ipynb           # Starter notebook for Titanic data analysis
|-- load_data_from_sqldb/
|   `-- pandas_load_sql.ipynb         # Read SQL query results into pandas
|-- .gitignore
|-- README.md
`-- requirements.txt                 # Python packages used by the notebooks
```

## Set up the Python environment

These instructions use one virtual environment at the repository root. From the repository directory, run the following in a PowerShell terminal:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

If PowerShell prevents environment activation, you can install packages without activating it:

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## Choose the notebook kernel in VS Code

1. Open a notebook (`.ipynb`) in VS Code.
2. Select **Select Kernel** in the upper-right corner.
3. Choose **Python Environments**, then choose the interpreter inside this repository's `.venv` folder. It may appear as `.venv (Python 3.x)`.
4. If `.venv` is not listed, choose **Enter interpreter path** and select `.venv\Scripts\python.exe`.
5. Run this cell to confirm the notebook is using the expected environment:

   ```python
   import sys
   print(sys.executable)
   ```

   The printed path should end with `.venv\Scripts\python.exe`.

After installing a package, restart the notebook kernel before importing it. Keep notebook dependencies in `requirements.txt` so the environment can be recreated.

## Notebooks

### Titanic dataset exploration

Open `eda_titanic_dataset/data_analysis.ipynb` to start the Titanic exploratory data analysis project. Add its dataset and analysis steps as the project develops.

### Loading SQL data with pandas

Open `load_data_from_sqldb/pandas_load_sql.ipynb` to connect to a local MySQL database, query the `customers` table, and load query results into a pandas DataFrame.

This notebook expects a MySQL server and an `ecommerce_training` database with a `customers` table. Update the connection settings in the notebook to match your local database. Do not commit passwords or other credentials.

## Working with datasets

- Check the source, license, attribution requirements, and privacy restrictions before adding a dataset.
- Put small, shareable datasets used by multiple projects in `assets/`; keep project-specific data with that project.
- Do not commit private, sensitive, or very large data. Document how collaborators can obtain data that is hosted elsewhere.
- Keep original data unchanged where practical, and describe how any cleaned or generated data was produced.
- `.env` files and virtual environments are ignored by Git. Never put secrets in notebooks or dataset files.

## Adding a project

Create a descriptive folder for the topic or dataset. Add its notebooks, data-loading or analysis code, and a short explanation of the data source and project purpose. Add any new Python packages to the root `requirements.txt`.

## License

No repository-wide license has been selected. Add a `LICENSE` file before distributing code if you want to grant reuse rights. Dataset licenses and terms may differ from the code license.
