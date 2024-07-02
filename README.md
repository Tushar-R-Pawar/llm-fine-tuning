# Gemma-2B Finetuning for Math Word Problems

This repository contains code for finetuning the Gemma-2B model on math word problems dataset using Hugging Face's Transformers library and other related tools.

## Setup and Configuration
Clone this repository and navigate into the directory. Ensure to set up your environment properly.

## Data Preparation
The math word problems dataset (microsoft/orca-math-word-problems-200k) is used for finetuning. It is loaded and preprocessed using the AutoTokenizer from Hugging Face.

## Model Finetuning
The Gemma-2B model is finetuned using the SFTTrainer from Trl. Here are some key training parameters:

Batch Size: 1
Gradient Accumulation Steps: 4
Warmup Steps: 2
Max Steps: 500
Learning Rate: 2e-4
Optimization: PagedAdamW with 8-bit precision
Prints the number of trainable parameters in the model before training.

## Evaluation
Example of generating output from the finetuned model on a math word problem input.

## Model Saving and Uploading
The finetuned model (google/gemma-2b-finetuned) and tokenizer are saved and uploaded to Hugging Face Model Hub.

## Installation

Install necessary dependencies using pip:

```bash
!pip3 install transformers==4.38.2
!pip3 install -U torch datasets sentence_transformers
!pip3 install accelerate==0.27.2 peft==0.4.0 bitsandbytes==0.40.2 trl==0.4.7
!pip3 install wandb```

