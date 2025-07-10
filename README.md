# German-English Translation using OPUS Books Dataset

This repository contains a complete workflow for training a German-to-English translation model using the OPUS Books dataset. The project includes dataset exploration, preprocessing, training a Transformer-based model, and evaluating translation performance.

## Dataset

The dataset used is the OPUS Books German-English translation corpus, accessed via the Hugging Face `datasets` library.

Steps involved:
- Load the `de-en` split from the OPUS Books dataset.
- Display the dataset structure and a few sample entries for initial inspection.
- ## Exploratory Data Analysis (EDA)

The notebook includes exploratory analysis to better understand sentence and word characteristics:
- Sentence length distributions in both German and English.
- Frequency analysis of commonly used words.
- Visualization of these characteristics to aid in preprocessing and model design.
- ## Model Training

A Transformer-based model is implemented. Key training steps include:
- Tokenization and vocabulary setup using Hugging Face tokenizers.
- Data batching with attention masks and padding.
- Training loop with performance monitoring.
- ## Evaluation

Translation performance is evaluated using the BLEU score, computed on a held-out test set. Additionally, several example translations are shown to provide qualitative insight into the model’s output.

## Requirements

To replicate the environment used in this project, install the following packages:

```bash
pip install -U transformers
pip install -U transformers datasets fsspec==2023.6.0
pip install -q transformers datasets
pip install -q evaluate
pip install -q rouge_score nltk sacrebleu
pip install -q wordcloud
```

To open the notebook locally:

```bash
pip install notebook
```

## Running the Notebook

To run the translation workflow, open the Jupyter notebook `Assignment_2final.ipynb` and execute the cells in order:

```bash
jupyter notebook Assignment_2final.ipynb
```

A GPU is recommended for model training.

## Notes

- Due to environment or rendering limitations, the notebook preview may not display correctly on GitHub. It is recommended to download the file and open it locally using Jupyter for full functionality.
- Inline comments and visualizations in the notebook assist with comprehension and reproducibility.
  
