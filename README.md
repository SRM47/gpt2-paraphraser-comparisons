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
See the paper ``final.pdf`` to read about the results of this investigation


