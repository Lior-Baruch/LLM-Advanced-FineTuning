# Repository Overview
This repository contains three Jupyter notebooks, each focusing on advanced techniques for fine-tuning large language models (LLMs). The notebooks demonstrate the use of LoRA, quantization, SFT (Supervised Fine-Tuning), and DPO (Direct Policy Optimization) on LLaMA and Mistral 7B models. These methods aim to enhance model performance by incorporating human preference data and efficient fine-tuning strategies.

## Notebooks

### 1. FineTune_llama
- **Objective**: Fine-tuning the LLaMA-2-7B model using LoRA and quantization techniques.
- **Key Features**:
  - **Model Loading**: Loading the LLaMA-2-7B model with quantization configurations for memory efficiency.
  - **LoRA Adapters**: Adding and configuring LoRA adapters for efficient fine-tuning.
  - **SFTTrainer**: Utilizing a custom `SFTTrainer` for supervised fine-tuning.
  - **Training Setup**: Setting up training arguments, including batch size, learning rate, optimizer, and scheduler.
  - **Model Testing**: Comparing the base model with the fine-tuned model to illustrate the effects of fine-tuning.
- **Libraries Used**: `transformers`, `datasets`, `bitsandbytes`, `trl`, `accelerate`, `wandb`.

### 2. Fine_tune_Mistral_7b_with_DPO
- **Objective**: Fine-tuning the Mistral 7B model using DPO with human preference data.
- **Key Features**:
  - **Data Formatting**: Custom function for formatting the dataset for DPO.
  - **LoRA Configuration**: Configuring LoRA parameters for the Mistral 7B model.
  - **DPO Training**: Setting up and executing DPO training with the specified dataset.
  - **Inference Testing**: Testing the model's inference capabilities post fine-tuning.
- **Libraries Used**: `datasets`, `trl`, `peft`, `bitsandbytes`, `wandb`.

### 3. DPO_llama (Contains Bugs)
- **Objective**: Applying DPO to train the LLaMA 7B model with human preference data.
- **Key Features**:
  - **Model and Tokenizer Setup**: Loading and configuring the LLaMA 7B model and tokenizer.
  - **Human Preference Data**: Loading and preprocessing a dataset of human preferences.
  - **DPO Configuration**: Setting up a DPO trainer with the model, reference model, dataset, and tokenizer.
  - **Comparative Testing**: Emphasis on comparing the base model with the fine-tuned model.
- **Libraries Used**: `transformers`, `datasets`, `trl`, `peft`.

## Repository Structure
- `FineTune_llama.ipynb`: Demonstrates fine-tuning of LLaMA 7B using LoRA and quantization.
- `Fine_tune_Mistral_7b_with_DPO.ipynb`: Focuses on fine-tuning Mistral 7B using DPO.
- `DPO_llama.ipynb`: Attempts to apply DPO to LLaMA 7B, currently with bugs.

## How to Use
- Each notebook is self-contained with detailed comments and explanations.
- Ensure all dependencies are installed as specified in each notebook.
- Notebooks can be run in environments like Google Colab for optimal performance.

## Contributing
- Contributions to fix bugs, enhance the models, or improve the notebooks are welcome.
- Please follow the standard pull request process for contributions.
