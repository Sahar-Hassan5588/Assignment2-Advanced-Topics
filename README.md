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

## Project Goals
- Evaluate LLM consistency in decision-making under identical conditions
- Analyze potential biases in vulnerability assessments based on demographic attributes
- Examine reasoning patterns used by different models in phishing classification tasks
- Compare performance across Google, Microsoft, Meta, and Mistral providers