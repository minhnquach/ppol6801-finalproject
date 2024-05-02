# Reddit Reactions to the Overturn of Roe v. Wade: A Sentiment Analysis and Topic Modelling Study

## Abstract

This project investigates the evolving discourse surrounding reproductive rights on Reddit in the context of the historic Dobbs v. Jackson Women's Health Organization decision, which overturned Roe v. Wade. Employing the standard topic modeling techniques and sentiment analysis tools on a dataset of 24,653 posts and 139,822 comments from March to August 2022, we identified key themes and sentiment patterns in response to the Supreme Court opinion leak and the official ruling. The findings reveal increased user activity and engagement, particularly in politically-oriented posts, as well as a significant drop in sentiment among political contents following the two events. These effects however did not last for more than a month. The study highlights the value of leveraging social media data to gain insights into public opinion dynamics surrounding pivotal events and lays the groundwork for further investigations into how these changes are reflected in and shaped by online discussions on popular social media platforms.

## Tutorial 

This README file provides an overview of the project as well as additional instructions for viewing and also replications. In here, there is the code directory, the input and output directories, the original research proposal, the research report, and this Readme file.

## Codes

The files below, written in Python Jupyter Notebook, are presented in the order that they were run. Due to the limited access policy of the AWS buckets, for replication purpose, users can skip the initial processing and analyses, and go straight to the final notebook which concerns NLP, using the provided parquet datafiles in the input directory. Also note that necessary modifications are needed to adapt the current code to a non-Spark approach that would work with the provided parquet datafiles.

- `project_starter_script.ipynb`: this code reads in the raw dataset from the Spark server provided, briefly explores and analyzes it, before filtering out the comments and submissions from only the subreddits of interest. The filtered data was then stored in a private AWS S3 bucket for later steps.
- `project_eda.ipynb`: this code loads the previously extracted data from the S3 bucket, and performs several exploratory data analyses with 5 component questions and interpretations included.
- `project_nlp.ipynb`: this code loads the data extracted from the S3 bucket, and perform 3 different Natural Language Processing analyses which include word frequency, topic modelling, and sentiment analysis.

## Data

The initial raw data for this project was stored on a private S3 bucket that was made available thanks to the courtesy of Professor Amit Arora from the course PPOL-5206. The original collector and provider of this data can be found below, with the relevant details:

https://arxiv.org/abs/2001.08435

The input directory in this repository contains the processed and extracted data for the subreddits and timeframe of interest, and stored in a parquet format.

## Output

The output directory has two main components:

- /csv/: which contains all table outputs produced by the scripts
- /plot/: which contains all graph and visual outputs produced by the scripts

