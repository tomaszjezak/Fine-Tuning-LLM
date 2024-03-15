### Fine-Tuning-LLM

# Project 1: Instruct-Tuning LLaMA (Supervised) 

Instruct-tuned the LLaMA recreation by OpenLM Research "Open LLaMA 7b", consisting of 7 billion parameters.

*** IMPORTANTLY -- we used QLoRA for efficient fine-tuning! QLoRA reduces memory usage so I can finetune a 7b parameter model in just 1.5 hours on A100 on Google Colab (5,000 iterations)!
    - [QLoRA](https://github.com/artidoro/qlora) preserves the full 16-bit finetuning task performance by implementing 4=bit NormalFloat (NF4)< a new data type that is optimal for saving memory without sacrificing performance.
    
We trained the LLM on the Dolly15k dataset, consisting of 15,000 prompts/answers (some with additional context). 

Training Goal: Make the LLM user-friendly! User is able to talk and get a quality response. Not just the transformer playing "predict the next token".

** Needs some slight revision. My goal is to upload this to HuggingFace and make a front-end. I've worked with lots of models, done lots of research/read lots of papers, finetuned... but haven't made something "end-to-end" until this! Will complete by March 23.

# Project 2: Fine-Tuning BLOOMZ (Unsupervised)

