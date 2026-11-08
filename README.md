# Machine Learning

A workspace for exploring datasets, practicing data analysis, and building machine-learning projects. Each project should keep its notebooks, notes, and project-specific setup together.

## Repository layout

```text
Machine Learning/
|-- assets/                       # Datasets and other shared project assets
|-- eda_titanic_dataset/
|   |-- data_analysis.ipynb       # Titanic dataset exploration
|   |-- pandas_load_sql.ipynb     # Loading and working with data using pandas/SQL
|   `-- requirement.txt           # Dependencies for this project
|-- .gitignore
`-- README.md
```

Add a folder for each new dataset or analysis so its notebooks and documentation stay organized. Keep datasets in `assets/` when they are shared across projects; project-specific data can live in that project's folder.

## Getting started

1. Clone the repository and open it in your editor.
2. Create and activate a virtual environment in the project folder. For example, from the repository root:

   ```powershell
   py -m venv eda_titanic_dataset\.venv
   .\eda_titanic_dataset\.venv\Scripts\Activate.ps1
   ```

3. Install the current project's dependencies:

   ```powershell
   python -m pip install -r eda_titanic_dataset\requirement.txt
   ```

4. Start Jupyter and open a notebook:

   ```powershell
   jupyter notebook
   ```

   Open `eda_titanic_dataset/data_analysis.ipynb` or `eda_titanic_dataset/pandas_load_sql.ipynb`.

Use the dependency file belonging to a project when setting up other projects. Add or update that project's dependency file when introducing new packages.

## Datasets and responsible use

- Include only datasets you are permitted to share; check the source, license, attribution requirements, and any privacy restrictions.
- Avoid committing private, sensitive, or very large data. Use an approved data-hosting service for files that should not live in Git, and document how to obtain them.
- Keep original data unchanged where practical. Put cleaned or generated data in a clearly named subfolder and document how it was produced.
- Do not put credentials or other secrets in notebooks or datasets.

## Local configuration

Git ignores `.env` files and Python virtual-environment folders. If a project needs environment variables, create a local `.env` file and keep it out of Git. Share the variable names (not secret values) in `.env.example`.

> Ignore rules do not remove files already tracked by Git. If a secret was committed previously, remove it from version control and rotate the credential.

## Working with notebooks

- Use descriptive notebook names and include a short purpose statement near the top.
- Keep exploratory work reproducible: record important assumptions, data sources, and relevant package requirements.
- Clear bulky or sensitive notebook outputs before sharing.

## License

No repository-wide license has been selected yet. Add a `LICENSE` file before distributing code if you want to grant reuse rights. Dataset licenses and terms may differ from the code license.
