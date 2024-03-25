# Project 1: Instruct-Tuning LLaMA (Supervised) 

Instruct-tuned the LLaMA recreation by OpenLM Research "Open LLaMA 7b", consisting of 7 billion parameters.

*** IMPORTANTLY -- we used QLoRA for efficient fine-tuning! QLoRA (4-bit) reduces memory usage so I can finetune a 7b parameter model in just 1.5 hours on A100 on Google Colab (5,000 iterations)!
    
- [QLoRA](https://github.com/artidoro/qlora) preserves the full 16-bit finetuning task performance by implementing 4-bit NormalFloat (NF4), a new data type that is optimal for saving memory without sacrificing performance.
    
We trained the LLM on the Dolly15k dataset, consisting of 15,000 prompts/answers (some with additional context). 

Training Goal: Make the LLM user-friendly! User is able to talk and get a quality response. Not just the transformer playing "predict the next token".

** Needs some slight revision. My goal is to upload this to HuggingFace and make a front-end. I've worked with lots of models, done lots of research/read lots of papers, finetuned... but haven't made something "end-to-end" until this! Will complete by March 28.


# Project 2: Fine-Tuning BLOOMZ (Unsupervised)

Fine-tuned BLOOMZ, which is the instruct-tuned version of BLOOM, for specific tasks... in this case, to mimic direct email marketing copy.

We used [LoRA](https://arxiv.org/abs/2106.09685), the 8-bit version. LoRA updates pre-trained weight matrices with low-rank matrices to adapt the model to specific task, while maintaing computational efficiency. Thus, significant savings in memory and storage, allowing for the deployment of customized models adapted for various tasks without inference latency.

We note that we only trained on 17 data points and got remarkably good performance. 

** I am excited especially by Project 2, since I can create so many different applications and obtain good performance, even on small datasets. Will certainly revise this, as well. Again, I'll add front end and train on a new dataset. Currently thinking of making it write jokes in the style of some of my favorite comedians.
