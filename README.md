# Neural-network-stackoverflow-data-project

## Intent Detection through a Neural Network-Enabled Text Classifier
Contributors: Alexander Heger, Mugdha Khairnar, Ishan Nagrani

### Problem Statement
Our goal is to create a neural network text classifier which accurately predicts intent given a text document. Here, our predictors are the unique text tokens of questions posted to Stack Overflow. The labels are the Tags that Stack Overflow’s users assign to each question, since these indicate the intent of the question body. We aim to identify the model which best predicts the true label for each post.

### Motivation
We chose this prediction task to emulate the upstream stages of a language model-enabled chatbot. The model that we deliver will be able to predict labels which inform the response of a language model which could be used to answer questions about a product or topic in an online chat. Any company with an online presence could use our model, combined with a chatbot, to automate the purpose traditionally served by a call center.

While our model is only a precursor to a fully functioning chatbot, the predictions it accurately generates will provide insights into the context of a user’s question. Intent detection through neural networks is not a new idea; however, we have not seen our dataset used to this end, nor in the context of executing an upstream process for a chatbot.

### Data Source
Our data set comprises 139,638 questions posted to the programming forum, Stack Overflow from August 1 to August 31, 2022. We sourced our data through Google BigQuery which pulls from Stack Exchange’s Data Explorer tool. Our data contains the body text of various users’ questions posted to Stack Overflow along with the labels (Tags) attributed to each question by the site’s users, along with 18 other columns of metadate (e.g., ID, creation date, number of viewers, etc.).

At various points through the notebook we'll sample smaller sets of the data in order to make processes more efficient given Colab's resource limitations. We chose to use Google Colab Pro+ after finding that VertexAI's Jupyter Notebook version was incompatible with natural language processing (NLP) packages key to our analysis.
