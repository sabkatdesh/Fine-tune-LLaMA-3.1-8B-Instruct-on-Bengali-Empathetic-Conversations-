# Fine-tune-LLaMA-3.1-8B-Instruct-on-Bengali-Empathetic-Conversations

## 📌 Project Overview
This project implements a complete pipeline for parameter-efficient fine-tuning of a Large Language Model (LLM) on the Bengali Empathetic Conversations corpus. The goal is to enable the model to generate contextually appropriate and empathetic responses in Bengali.

**Key Challenge & Approach**: Due to hardware constraints and model access issues, the project demonstrates two parallel approaches:
1.  **A Complete Pipeline with TinyLlama**: A full implementation showing data processing, LoRA fine-tuning, and evaluation with a working model.
2.  **Correct Architecture with LLaMA 3.1-8B**: Loading and configuring the exact model specified in the assignment brief, with a clear explanation of hardware limitations.

## 🗂️ Repository Structure

Fine-tune-LLaMA-3.1-8B-Instruct-on-Bengali-Empathetic-Conversations-/
│
├── Llama_3.1B.ipynb # Main notebook for LLaMA 3.1 setup and methodology
├── Tiny_llama_Bengali_empathetic_conversation_fine_tuned.ipynb # Complete pipeline with TinyLlama
├── README.md # This file
├── LICENSE # MIT License
│
├── evaluation_metrics.json # Quantitative results (Perplexity, BLEU, ROUGE)
├── sample_responses.csv # Qualitative examples of generated Bengali responses
├── human_evaluation_template.csv # Framework for human assessment
├── documentation.md # Detailed project report and analysis
└── assignment_experiments.db # SQLite database for experiment logging


## 🚀 How to Run
1.  **Environment**: The notebooks are designed to run on **Kaggle** with a **P100/T4 GPU accelerator** enabled.
2.  **Execution**: Open the desired notebook (`Tiny_llama_*.ipynb` for the complete demo, `Llama_3.1B.ipynb` for the specified model setup) and run all cells sequentially.

## 📈 Key Features & Implementation
*   **Modular OOP Design**: Implements `DatasetProcessor`, `LLAMAFineTuner` (using Strategy Pattern for LoRA), and `Evaluator` classes for maintainable code.
*   **Parameter-Efficient Fine-Tuning**: Utilizes LoRA (Low-Rank Adaptation) to train only 0.17% of the model's parameters.
*   **Comprehensive Evaluation**: Implements automated metrics (Perplexity, BLEU, ROUGE) and provides a template for human evaluation of empathetic quality.
*   **Experiment Logging**: A custom SQLite logging system tracks all experiments and generated responses as per the assignment requirements.

## 🔍 Results & Findings
*   The fine-tuned model successfully generates fluent Bengali responses.
*   The TinyLlama implementation provides a complete benchmark for the pipeline's functionality.
