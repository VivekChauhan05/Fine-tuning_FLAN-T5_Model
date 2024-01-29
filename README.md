# Dialogue Summarization with Hugging Face Transformers

## Overview

This repository contains code for fine-tuning and evaluating dialogue summarization models using Hugging Face Transformers. Dialogue summarization involves condensing conversational exchanges into concise summaries. We use the Hugging Face `transformers` library to train, evaluate, and compare the performance of different models on a dialogue summarization task.

## Processes

### 1. Installation

- Ensure you have Python installed.
- Install required packages using pip:

```bash
pip install --upgrade pip
pip install --disable-pip-version-check \
    torch==1.13.1 \
    torchdata==0.5.1 \
    transformers==4.27.2 \
    datasets==2.11.0 \
    evaluate==0.4.0 \
    rouge_score==0.1.2 \
    loralib==0.1.1 \
    peft==0.3.0
```

### 2. Dataset Loading

- Load the dialogue summarization dataset from the Hugging Face dataset library.
- Print information about the dataset.

### 3. Model Initialization

- Initialize the baseline Seq2Seq model for dialogue summarization.
- Load the tokenizer corresponding to the chosen model.

### 4. Model Training

- Define the function to print the number of trainable model parameters.
- Tokenize the input dialogue and summary pairs for training.
- Define the training arguments.
- Initialize the Trainer object for model training.
- Train the model.

### 5. Model Fine-tuning (PEFT)

- Initialize the PEFT (Parameter Efficient Fine-Tuning) configuration.
- Fine-tune the baseline model using PEFT.
- Save the fine-tuned model checkpoint.

### 6. Evaluation

- Evaluate the baseline model and PEFT fine-tuned model using Rouge metric.
- Compare the performance of both models.

## Use Cases

- Dialogue summarization for customer service chat logs.
- Summarizing meeting transcripts for quick reference.
- Generating brief summaries of online forum discussions.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.