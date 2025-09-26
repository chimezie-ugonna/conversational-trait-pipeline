# Conversational Trait Pipeline
Pilot study pipeline for human-in-the-loop conversational trait analysis using Llama and Gemini models. This notebook demonstrates how conversational traits can be annotated, modeled, and evaluated using a small subset of human-labeled dialogues.

## Overview

This pipeline allows users to:

1. Load and preprocess human conversation data.
2. Annotate conversational traits manually (Human-in-the-Loop).
3. Automatically annotate conversation chunks using LLMs (Llama and Gemini).
4. Evaluate model performance against human annotations using Accuracy and Cohen’s Kappa.
5. Visualize trait distributions and comparison tables.

The pipeline is implemented in a Google Colab notebook for reproducibility and ease of use.

## Dataset

- The dataset used is a subset of conversations from a publicly available Kaggle dataset ([Kaggle, 2025](https://www.kaggle.com/datasets/projjal1/human-conversation-training-data/data)) stored in `human_chat.txt`.
- The notebook includes preprocessing to split individual speaker turns and organize them into chunks for annotation.
- Only a small subset is used in this pilot study to enable an in-depth demonstration of the framework.

## Requirements

- Python 3.8+
- Google Colab environment (recommended for GPU/TPU access)
- Libraries: `pandas`, `matplotlib`, `scikit-learn`, `google-generativeai`, `openai`

Install missing packages in Colab:

```python
!pip install pandas matplotlib scikit-learn google-generativeai openai
```

## Setup

1. **Upload the Dataset**  
   Ensure `human_chat.txt` is available in your Colab environment. The notebook will prompt you to upload it if missing.

2. **Install Required Libraries**  
   Run the following command in a Colab cell to install all necessary packages:

```python
!pip install pandas matplotlib scikit-learn google-generativeai openai
```

3. **Provide API Keys**
   You need API keys for the Llama and Gemini models. Place your keys into the code when prompted:
   
* Get your Llama API key [here](https://openrouter.ai/sign-in?redirect_url=https%3A%2F%2Fopenrouter.ai%2Fsettings%2Fkeys)
* Get your Gemini API key [here](https://aistudio.google.com/api-keys)


## How to Run
1. Upload `human_chat.txt` if not already in the notebook environment.
2. Input your API keys when prompted.
3. Load and preprocess the dataset.
4. Run the annotation pipeline:
	* Human annotation loop
	* Model annotation (Llama & Gemini)
5. Evaluate results and plot trait distributions.


## Output
* Accuracy and Cohen’s Kappa scores comparing human vs model annotations.
* Trait distributions per participant (bar charts).
* Chunk-wise comparison tables showing human and model labels.


## Citation
If you use this notebook, please cite it as:
```text
Chimezie, U. (2025) 'Conversational Trait Analysis Pipeline [Google Colab notebook]'. Available at: https://github.com/chimezie-ugonna/conversational-trait-pipeline
```

