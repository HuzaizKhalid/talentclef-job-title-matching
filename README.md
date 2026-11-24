# Zero-shot multilingual job title matching (TalentCLEF 2025 Task A)

Code to reproduce the experiments: TF-IDF (char n-grams) vs multilingual-e5-base, LaBSE and bge-m3 on the Task A validation split (en, es, de, zh).

## Data
Download the TalentCLEF 2025 data from Zenodo (record 15292308, CC BY 4.0) and place the validation folder at `TaskA/validation`. The data is not included in this repository.

## Run (Google Colab, T4 GPU)
```
pip install -r requirements.txt
python code/talentclef_job_title_experiment.py
python code/significance_tests.py per_query_results.csv "MAP,NDCG@10,P@5,R@100"
```
Outputs: results.csv, per_query_results.csv, dataset_stats.csv, results_plot.png, significance_results.csv. Seed = 42; search is deterministic, bootstrap is seeded.

## Results
Result CSVs used in the paper are in `results/`.

## Citation
Add the paper reference here after publication.
