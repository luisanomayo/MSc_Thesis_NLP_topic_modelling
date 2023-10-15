# Topic Modelling of Urban Discourse: A Machine Learning Approach for Understanding Life in Dubai

## Description
Topic modelling, a crucial text mining technique, is employed in this study to extract major themes from a vast array of documents pertaining to urban life in Dubai. By leveraging techniques such as Latent Dirichlet Allocation (LDA) and BERTopic, and analyzing conversations from the Reddit platform, this research project endeavors to understand Dubai's changing narrative and to evaluate the efficacy of prominent topic modelling methodologies on multi-contextual datasets. The study delves deep into areas of pre-processing, feature extraction, model development and optimization, and a temporal analysis of the surfaced topics. Key discussions in the results encompass areas such as mobility, the COVID-19 pandemic, employment opportunities, immigration, and multi-cultural relations. This research underscores the capabilities of topic modelling to decipher regional sentiments and experiences.

## Datasets
The project uses various datasets to support its findings:

- **bert_train_no_prep.csv**: Training data utilized for the BERTopic models.
- **comments.csv**: A compilation of raw comments sourced from the Reddit platform.
- **full_posts.csv**: A collection of raw posts/submissions from Reddit.
- **posts_upvote_ratio.csv**: Compilation of post IDs and their upvote ratios, retrieved from the Reddit platform.
- **sub_upvotes.csv**: Data subset used for time series analysis.
- **subset_sample_no_label.csv**: Test dataset.
- **lda_train.csv**: Pre-processed data used for training the LDA models.

## Notebooks
The following Jupyter notebooks encapsulate the research's coding efforts:

- **lda_model_new_20_08_22.ipynb**: Entails the pre-processing of training data and the training of LDA models using bag-of-words vector representations.
- **lda_model_new_tfidf_28_08_22.ipynb**:  the code for training the LDA models employing TF-IDF vector representations.
- **model_evaluations_lda.ipynb**: Concentrates on evaluating the LDA models.
- **model_evaluations_bertopic.ipynb**: Focuses on the evaluation of BERTopic models and their application on test data.
- **bertopic_model_1.ipynb**: Includes code for training BERTopic model on raw data with SBERT pre-trained language model, HDBSCAN clustering, and no topic representation fine-tuning.
- **bertopic_model_2.ipynb**: Encompasses training BERTopic model on processed data with SBERT pre-trained language model, HDBSCAN clustering, stop word removal, and topic representation fine-tuning.
- **bertopic_model_3.ipynb**: Details the training of BERTopic model on processed data with SBERT pre-trained language model, KMeans clustering, stop word removal, and topic representation fine-tuning.
- **bertopic_model_4.ipynb**: Highlights the process of training BERTopic model on processed data with a custom sentence model built using word2vec embeddings of the training data, KMeans clustering, stop word removal, and topic representation fine-tuning.
- **time_series_analysis.ipynb**: Concentrates on the temporal analysis of generated topics.

## Dependencies & Environment
- LDA models were structured using Python 3.10.1. The specific dependencies for these models can be found in the `lda_env_requirements.txt` file.
- BERTopic models were constructed using Python 3.7.16. Dependencies for these models are enumerated in the `bert_env_requirements.txt` file.

## Installation & Setup
Please refer to this detailed guide by [GitLab](https://docs.gitlab.com/ee/user/project/repository/) for our to clone this repository.

To successfully set up and run the project on a local machine, ensure adherence to the repository structure provided. 

Set up the necessary virtual environments conducive for executing the code for either module.

### For LDA Topic Modelling:
The development notebook is located in topic_modelling>LDA_models>notebooks.
The models trained during our study can be accessed in the topic_modelling>LDA_models>trained_models directory and can be utilized in a notebook using the gensim's LdaModel.load() module

### for BERTopic Modelling:
Unfortunately the models developed during our study could not be stored in this repository due to GitLab size limits. However our model development code can be accessed in the topic_modelling>bertopic_model_training directory, along with our training results 
