# [Code-Maroon-Global-Edition](https://yash8005.github.io/code-maroon-report/)

Information retrieval is a critical component of crisis response, but it's not always easy to find reliable sources in the midst of chaos. Rumors, gossip, and wild speculation run rampant, leaving authorities scrambling to sort fact from fiction. In this scenario, there is a need for a global, reliable and user friendly application to provide quick and accurate facts to the general masses.
This task is from 2022 TREC CrisisFACTs Track: https://crisisfacts.github.io/

## Features
Utilizes state-of-the-art machine learning models (T5, Roberta, OpenAI) to provide accurate and reliable information.
Extracts important information from news articles and stores them in a vector database for fast searching.
Supports multiple sources such as Twitter, Reddit, Facebook, and news websites.
Provides answers to user queries in real-time.
User-friendly web-based interface.

## Contents

This repository contains the following directories:

* data: contains the datasets used for training and testing the models. TREC 2022 dataset
* Test Data: contains smaller chunk of data used for inital testing

## Approach

* Collect and preprocess data by gathering from various sources and removing irrelevant text.
* Extract relevant context text called "Headlines" and embed chunks using Sentence-Transformer model "paraphrase-MiniLM-L6-v2".
* Use cosine similarity to extract relevant headline chunks from embedded headline data based on query.
* Perform fact extraction using large language models (LLMs) pre-trained on QA datasets like SQuAD dataset.
* Three successful LLMs used: "deepset/roberta-base-squad2," "Google Flan T5 Model," and "Open AI text-davinci-002 - GPT 3.5 series model".
* Input embeddings of query and relevant documents to LLMs using Roberta model tokenizer for "deepset/roberta-base-squad2" model.
* Output of models is extracted facts in answers form.

## Observations

We conducted experiments on T5, Open AI, and Roberta models for general and fact-based queries. On average, T5 outperformed the other models in terms of exact match, F1 score, recall, and precision for general queries, achieving an exact match rate of 14.38%, F1 score of 0.204, recall of 25.74%, and precision of 34.87%. However, for fact-based queries, T5 performed significantly better with an exact match rate of 60.00%, F1 score of 0.6, recall of 60.00%, and precision of 60.00%. Open AI and Roberta followed with 20.00% and 33% exact match rate respectively for fact-based queries.

These results highlight the potential of T5 as the preferred model for general queries, while Open AI and Roberta can be used as alternative models. However, for fact-based queries, T5 proved to be the most effective model, followed by Open AI and Roberta. These results were obtained from our experimentation repository, which includes all the code, data, and results. For more details, please refer to our report website. To experience our demo version, please visit our demo website and demo repository.

## Experiments and Results

For a more detailed overview of our project, including our methodology, experiments, and results, please visit our other repository Code Maroon Global Edition (https://github.com/yash8005/Code-Maroon-Global-Edition) . There, you will find information on the different models we tested, as well as the performance of each model on various datasets.

We have also created a website where you can find a detailed report of our experiments, including the methodology, results, and analysis. You can access the report website at https://yash8005.gitlab.io/code-maroon-report/

## Demo Website and Repo

If you are interested in trying out the demo version of Code Maroon, you can visit our demo website at https://codemaroon.streamlit.app/ or check out the demo repository at https://github.com/yash8005/code-maroon-deploy.

![Project Showcase](https://github.com/BhaShah12/BhaShah12.github.io/blob/main/images/showcase11.jpeg)



