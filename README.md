# NYU High Performance Machine Learning Project
## Summary
<p>An implementation of Gemma and DeepSeek R1 with 4 bit quantization and low rank adapters trained on FinQA dataset to demonstrate the ability of using an LLM in domain specialized tasks with low resource/low power devices</p>
<br/>
## Description
Two LLMs - Google's Gemma 3 1B IT variant and DeepSeek's R1 Distill 1.5B Qwen variant are used here. Both LLMs are compared in their effectiveness in financial reasoning and mathematical ability by using the FinQA dataset.
This is performed by first running the models with 4 bit Quantization (by bitsandbytes) and low rank adapters (QLoRA) on sample questions from the dataset. 
The model weights are frozen and the low rank adapters are trained for 1 epoch on the dataset to improve the outcomes from both LLMs. The results and involved training are studied and contributing key factors and hyperparameters are determined.
The intent is to demonstrate the ability of these models to perform non-ambigious financial reasoning and calculations on low powered/low resource devices through the use of quantization and low rank adapters.
<br>
## Milestones
<ol>
  <li>Environment setup<li>Set up required tokens and libraries</li><li>Characterize the dataset</li></li>
  <li>Data Preparation<li>Format dataset into appropriate data structure</li><li>Format and tokenize dataset tuples into queries</li></li>
  <li>Gemma 3 with QloRA implementation</li>
  <li>DeepSeek-R1 with QloRA implementation</li>
  <li>Baseline benchmarking for Gemma 3</li>
  <li>Baseline benchmarking for DeepSeek-R1</li>
  <li>Fine tuning both models on FinQA</li>
  <li>Evaluate optimal hyperparameters using W&B</li>
  <li>Benchmarking on fine tuned models</li>
</ol>
