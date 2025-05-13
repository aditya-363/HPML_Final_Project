# NYU High Performance Machine Learning Project
## Summary
An implementation of Gemma and DeepSeek R1 with 4 bit quantization and low rank adapters trained on FinQA dataset to demonstrate the ability of using an LLM in domain specialized tasks with low resource/low power devices
<br>

## Description
Two LLMs - Google's Gemma 3 1B IT variant and DeepSeek's R1 Distill 1.5B Qwen variant are used here. Both LLMs are compared in their effectiveness in financial reasoning and mathematical ability by using the FinQA dataset.
This is performed by first running the models with 4 bit Quantization (by bitsandbytes) and low rank adapters (QLoRA) on sample questions from the dataset. 
The model weights are frozen and the low rank adapters are trained for 1 epoch on the dataset to improve the outcomes from both LLMs. The results and involved training are studied and contributing key factors and hyperparameters are determined.
The intent is to demonstrate the ability of these models to perform non-ambigious financial reasoning and calculations on low powered/low resource devices through the use of quantization and low rank adapters.
<br>

## Milestones
<ol>
  <li>Environment setup<ol><li>Set up required tokens and libraries</li><li>Characterize the dataset</li></ol></li>
  <li>Data Preparation<ol><li>Format dataset into appropriate data structure</li><li>Format and tokenize dataset tuples into queries</li></ol></li>
  <li>Gemma 3 with QloRA implementation</li>
  <li>DeepSeek-R1 with QloRA implementation</li>
  <li>Baseline benchmarking for Gemma 3</li>
  <li>Baseline benchmarking for DeepSeek-R1</li>
  <li>Fine tuning both models on FinQA</li>
  <li>Evaluate optimal hyperparameters using W&B</li>
  <li>Benchmarking on fine tuned models</li>
</ol>
<br>

## Results
Both models performed faster or at about the same inference speed as before fine-tuning. Gemma seemed to be CPU bottlenecked during inference and performed slower compared to DeepSeek-R1. CoT improved slightly after fine-tuning. 
Loss over training steps - Gemma
![Screenshot 2025-05-08 202357](https://github.com/user-attachments/assets/e667f7ff-82be-45dc-8f8e-eb1eb938c7b1)
Loss over training steps - DeepSeek-R1
![Screenshot 2025-05-08 200123](https://github.com/user-attachments/assets/1603be8e-e4ee-4055-bed4-e533ae76c986)
Learning Rate over training steps
![Screenshot 2025-05-08 200236](https://github.com/user-attachments/assets/63cb26d0-f0cf-4ecb-b474-013f2930de8b)


## Repository structure
This repo contains two notebooks initially run on Kaggle using the P100 GPU. One for Gemma and the other for DeepSeek R1. Required library dependencies are handled within the notebook.
<br>

## Execution Instructions
Run the notebook on Kaggle/Colab (with modifications as needed)
