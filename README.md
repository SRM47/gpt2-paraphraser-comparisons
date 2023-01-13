# gpt2-paraphraser-comparisons
Finetune GPT-2 Models for paraphrasing and compare them to PEGASUS and BART


## Create Datasets
Use the script ``create_dataset.ipynb`` to create the dataset in the file ``combined.txt``. Each line contains the following: ``<s>S</s>>>>><p>P</p>``, where ``S`` and ``P`` are paraphrased sentences. Sentences pairs are gathered from three different datasets available on huggingface.co

- TaPaCo (en) https://huggingface.co/datasets/tapaco
- Google PAWS https://huggingface.co/datasets/paws
- Quora https://huggingface.co/datasets/quora

## Finetune GPT-2 Models

Finetuned three different sized GPT 2 models for sentence level paraphrasing using the ``Trainer()`` API.
Models available on huggingface:
- SRM47/gpt2-paraphraser
- SRM47/gpt2-medium-paraphraser
- SRM47/gpt2-large-paraphraser


## Evaluate Models
To evaluate the finetuned GPT-2 models and other models, use the ``eval_models.ipynb`` script

## Results Analysis
See the paper ``final.pdf`` to read about the results of this investigation.

As of recent, large language models, particularly a part of the Generative Pre-Trained series, have demonstrated themselves to be powerful text generation models. Models such as GPT-2 (Radford et al., 2018) reveal that large language models have strong zero-shot capabilities in a variety of downstream natural language pro- cessing tasks. Other models, built for sequence to sequence modeling, such as PEGASUS, and BART have profound text summarization capa- bilities which can be adapted to paraphrasing. In this paper, I present an effective method for adapting GPT-2 for paraphrasing, and compare its paraphrasing outputs to fine tuned BART and PEGASUS based models from huggingface. Results show that GPT-2 based models produce less diverse paraphrases than PEGASUS and BART; GPT-2 based paraphrases do not alter lexical form as much as PEGASUS does.


