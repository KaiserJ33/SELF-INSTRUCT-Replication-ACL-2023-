# SELF-INSTRUCT-Replication-ACL-2023-
Replicated SELF-INSTRUCT framework.
# SELF-INSTRUCT Replication

## Overview

This project replicates the methodology presented in the ACL 2023 paper *SELF-INSTRUCT: Aligning Language Models with Self-Generated Instructions* by Wang et al.

The goal of the project is to investigate how a language model can generate its own instruction-following training data and subsequently use that data to improve task performance. The project demonstrates the process of synthetic dataset generation, filtering, and fine-tuning using modern transformer-based architectures.

## Research Objective

Large language models often require substantial amounts of instruction-following data. The SELF-INSTRUCT framework proposes a method for automatically generating such data using the model itself.

This project explores the following question:

> Can a language model generate useful instruction-response pairs that can subsequently be used to improve instruction-following behavior?

## Methodology

The project follows the general SELF-INSTRUCT pipeline:

1. Begin with a set of manually written seed instructions.
2. Use a language model to generate new instructions.
3. Filter low-quality, duplicate, or invalid examples.
4. Construct a synthetic instruction-following dataset.
5. Fine-tune a transformer model using the generated data.
6. Evaluate generated outputs qualitatively and quantitatively.

## Dataset Generation

The synthetic dataset was produced through iterative instruction generation.

The workflow included:

* Seed instruction selection
* Instruction generation
* Output generation
* Data filtering
* Duplicate removal
* Dataset construction

The resulting dataset consists of instruction-response pairs suitable for supervised fine-tuning.

## Model Training

Fine-tuning was performed using the Hugging Face Transformers framework.

Key components include:

* Transformers
* Datasets
* Seq2SeqTrainer
* Tokenization pipelines
* GPU acceleration via Google Colab

## Technologies Used

* Python
* Hugging Face Transformers
* Hugging Face Datasets
* Google Colab
* PyTorch
* Pandas
* NumPy

## Repository Structure

```text
├── self_instruct.ipynb
├── generated_dataset/
├── results/
├── README.md
```

## Results

The project successfully reproduced the core stages of the SELF-INSTRUCT framework:

* Automatic instruction generation
* Synthetic dataset creation
* Instruction filtering
* Transformer fine-tuning

The results demonstrate how synthetic instruction data can be used to train instruction-following models without requiring large manually annotated datasets.

## Skills Demonstrated

* Large Language Models (LLMs)
* Natural Language Processing (NLP)
* Dataset Construction
* Transformer Fine-Tuning
* Prompt Engineering
* Machine Learning
* Deep Learning
* Python Development

## Reference

Wang, Y., Kordi, Y., Mishra, S., Liu, A., Smith, N. A., Khashabi, D., & Hajishirzi, H. (2023).

*SELF-INSTRUCT: Aligning Language Models with Self-Generated Instructions.*

Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (ACL 2023).

## Author

Joseph Kaiser

M.S. Computational Linguistics, Montclair State University

M.A. Forensic Linguistics, Aston University
