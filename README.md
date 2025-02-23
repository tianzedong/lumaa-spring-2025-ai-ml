# Simple Content-Based Movie Recommendation System
This project implements a content-based recommendation system that suggests movies based on a user’s text description of preferences. It uses TF-IDF vectorization and cosine similarity to match queries to movie plots.

## Dataset
- Source:`jrobischon/wikipedia-movie-plots` from Kaggle.
- Description: Wikipedia movie plot summaries with `Title` and `Plot` columns.
- Preprocessing:
  - Randomly sample 500 rows to meet the challenge’s small dataset requirement (100–500 rows).
  - Dropped rows with missing `Plot` values.
  
  **Note**: The system samples 500 movies from the original kaggle dataset to meet the challenge’s size constraint (100–500 rows). This random sampling may exclude some genres (e.g., space-action comedies), which could make search results seem less accurate for certain queries. For broader coverage, the full dataset (~35K rows) could be used, but this version prioritizes simplicity and efficiency.

## Setup
1. Prerequisites:
   - Python 3.9
   - Conda
   - Kaggle API key for `kagglehub`
2. Create and Activate Conda Environment
``` bash
conda create -n recsys python=3.9
conda activate recsys
```
3. Install Dependencies:
```bash
pip install -r requirements.txt
```
4. Register Kernel for Jupyter
```
python -m ipykernel install --user --name recsys --display-name "Recommendation System (recsys)"
```

Kaggle Authentication
- Download your Kaggle API key (`kaggle.json`) from Kaggle > Account > Create New API Token.
- Place it in `~/.kaggle/` (Linux/macOS) or `C:\Users\YourUsername\.kaggle\` (Windows).
- Set permissions (Linux/macOS): `chmod 600 ~/.kaggle/kaggle.json.`

## Running the Code
1. Open the Jupyter Notebook
``` bash
cd path/to/your/repo
jupyter notebook recommendation_system.ipynb
```
2. Run All Cells:
- In Jupyter, select `Kernel > Restart & Run All` to execute the code.
- The notebook loads the dataset, vectorizes plots, defines the recommendation function, and tests sample queries.
  
3. Test Your Own Query:
Edit the last cell’s `sample_query` variable (e.g., `sample_query = "Your description here"`) and re-run it.


## Salary Expectation
- $3000 per month