# Assignment2-Advanced-Topics

This repository contains Jupyter notebooks for an advanced assignment on evaluating the trustworthiness of Large Language Models (LLMs) in the context of phishing vulnerability assessment. The project focuses on analyzing bias, fairness, and reasoning patterns across multiple LLM providers.

## Repository Structure

```
Assignment2-Advanced-Topics/
├── Dataset Collection phase/
│   ├── DC1_Dataset_Generation_GoogleProvider.ipynb
│   ├── DC2_Dataset_Generation_MicrosoftProvider.ipynb
│   ├── DC3_Dataset_Generation_MetaProvider.ipynb
│   └── DC4_Dataset_Generation_MistralProvider.ipynb
├── Dataset/
│   ├── Per provider/
│   │   ├── Google/
│   │   ├── Meta/
│   │   ├── Microsoft/
│   │   └── Mistral/
│   └── combined_dataset_final.csv
├── DP1_Data_Processing_&_Validation.ipynb
├── EV_Trustworthiness_Evaluation_of_LLMs_Bias,_Fairness,_and_Reasoning_in_Phishing_Vulnerability.ipynb
├── README.md
├── Archive/
│   ├── Assignment2_V1.ipynb
│   ├── Assignment2_V2.ipynb
│   └── Assignment2.ipynb
└── Report progress/
```

## Files Overview

### Dataset Collection Phase
These notebooks generate synthetic datasets by prompting LLMs to create diverse personas and classify their phishing vulnerability.

- **DC1_Dataset_Generation_GoogleProvider.ipynb**: Dataset generation using Google's LLM provider (Gemma models: gemma-2b-it, gemma-7b-it, gemma-2-9b-it). Implements persona generation (Prompt 1) and vulnerability classification (Prompt 2) to evaluate consistency, bias, and reasoning patterns.

- **DC2_Dataset_Generation_MicrosoftProvider.ipynb**: Dataset generation using Microsoft's LLM provider (Phi models: Phi-3-mini-128k-instruct, Phi-3.5-mini-instruct, Phi-3-mini-4k-instruct). Follows the same two-stage prompting approach, enabling systematic evaluation of model behavior in phishing scenarios.

- **DC3_Dataset_Generation_MetaProvider.ipynb**: Dataset generation using Meta's LLM provider (Llama models: Llama-3.2-3B-Instruct, Meta-Llama-3.1-8B-Instruct). Generates diverse personas and assesses their phishing vulnerability, supporting analysis of fairness and decision consistency.

- **DC4_Dataset_Generation_MistralProvider.ipynb**: Dataset generation using Mistral's LLM provider (Mistral models: Ministral-8B-Instruct-2410, Mistral-7B-Instruct-v0.1, Mistral-7B-Instruct-v0.2). Creates structured datasets for evaluating reasoning patterns and potential biases in vulnerability assessments.

### Dataset Folder
Contains the generated and processed datasets used in the evaluation.

- **Per provider/**: Subfolders for each LLM provider containing their individual generated datasets before integration.
  - **Google/**: Datasets from Google Gemma models.
  - **Meta/**: Datasets from Meta Llama models.
  - **Microsoft/**: Datasets from Microsoft Phi models.
  - **Mistral/**: Datasets from Mistral models.
- **combined_dataset_final.csv**: The final unified dataset combining all provider outputs after processing and validation, ready for trustworthiness evaluation.

### Data Processing Notebook
- **DP1_Data_Processing_&_Validation.ipynb**: Integrates and cleans datasets from all providers. Performs structural validation, handles data quality issues like missing selections, parsing errors, and ensures consistency across columns and data types.

### Evaluation Notebook
- **EV_Trustworthiness_Evaluation_of_LLMs_Bias,_Fairness,_and_Reasoning_in_Phishing_Vulnerability.ipynb**: Main evaluation notebook that analyzes the combined dataset for trustworthiness metrics. Examines consistency, bias correlations with demographics, and reasoning patterns across different LLM providers.

### Archive Folder
Contains previous versions of the assignment notebooks:
- Assignment2_V1.ipynb
- Assignment2_V2.ipynb
- Assignment2.ipynb

### Report Progress Folder
Contains progress reports and intermediate documentation for the assignment.

## Replication Steps

To replicate the analysis and results of this project, follow these steps in order:

1. **Collect Data from All Providers**:
   - Run `DC1_Dataset_Generation_GoogleProvider.ipynb` to generate datasets for Google Gemma models.
   - Run `DC2_Dataset_Generation_MicrosoftProvider.ipynb` to generate datasets for Microsoft Phi models.
   - Run `DC3_Dataset_Generation_MetaProvider.ipynb` to generate datasets for Meta Llama models.
   - Run `DC4_Dataset_Generation_MistralProvider.ipynb` to generate datasets for Mistral models.
   - This will populate the `Dataset/Per provider/` subfolders with individual provider datasets.

2. **Data Processing and Validation**:
   - Run `DP1_Data_Processing_&_Validation.ipynb`.
   - This notebook feeds on the datasets generated in the DC phase, combines them, and processes the data to produce one high-quality unified dataset.
   - The output is `Dataset/combined_dataset_final.csv`, which integrates all provider outputs after cleaning, validation, and quality assurance.

3. **Evaluate Trustworthiness**:
   - Run `EV_Trustworthiness_Evaluation_of_LLMs_Bias,_Fairness,_and_Reasoning_in_Phishing_Vulnerability.ipynb`.
   - This notebook uses the combined dataset to evaluate the trustworthiness of LLMs, analyzing bias, fairness, and reasoning patterns in phishing vulnerability assessments across all providers.

## Project Goals
- Evaluate LLM consistency in decision-making under identical conditions
- Analyze potential biases in vulnerability assessments based on demographic attributes
- Examine reasoning patterns used by different models in phishing classification tasks
- Compare performance across Google, Microsoft, Meta, and Mistral providers