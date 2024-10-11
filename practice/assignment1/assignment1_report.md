# ASSIGNMENT 1: WORD2VEC REPORT 

### Word Embedding

- computers have a hard time processing written human-words, since they have few clear rules, and can be used quite diversely, so to work with words, people want to turn them into numbers for computers to work with
- you can assign random numbers, but then similar words (i.e synonyms) will have very different numbers, which is a problem if we want to save time when dealing with similar words
- instead, people use neural network to assign numbers to words, and that's basically **word embedding**

- steps to create the neural networks
1. create inputs for each unique words
2. connect each word to at least 1 (how many numbers we want to associate with each word) **activation function** (uses the identity function)
    - the **weights** on those connections will ultimately be the number that we associate with each word
    - the weights will start off randomly, and will be optimized using **backpropagation** (we have to make predictions by using the input words to predict the next word in the phrase)
    - connect the **activation functions** to outputs
      - add **weights** to those connections with random initilization values
      - run the outputs through the **SoftMax** function
      - use **Cross Entropy loss function** for **backpropagation**
3. the new **weights** on the connections from the inputs to the **activation functions** are the **word embeddings**

### Word2Vec 

- is a word embedding tool
- just predicting the next word doesn't give use a lot of context to understand each one so Word2Vec uses 2 methods to increase more context
  1. **Continuous Bag of Words**: using the surrounding words to preduct what occurs in the middle
  2. **Skip Gram**: using the word in the middle to predict the surrounding words
- they also use **negative sampling** to speed up the training process

### Assignment 1: Word2Vec implementation

- _your task is reimplement Word2Vec algorithm, train the model on WikiText-103 or WikiText-2, and visualize the word embeddings using t-SNE (To make the visualization readable, you should not visualize all the words, about 100 words are enough for demonstration purposes.)_
- _Your submission is a Jupyter notebook file with the t-SNE visualization_

1. reimplement Word2Vec algorithm
2. train the model
3. visualize the word embeddings using t-SNE

### Linkies 
- I first learned about WordEmbeddings [here](https://www.youtube.com/watch?v=viZrOnJclY0), but to understand that video you need to have a basic understanding of neural network, gradien descent, and backpropagation first, which I high recommend [this website](https://www.3blue1brown.com/topics/neural-networks)
- A reference, highly inefficient implementation is [here](https://colab.research.google.com/drive/1hBg2sCULriPmsCuht5oBhwLvk8ADjoxP?usp=sharing)
- [dataset](https://huggingface.co/datasets/Salesforce/wikitext/tree/main)

### Todos
- [ ] dive deeper into **Continuous Bag of Words**, **Skip Gram**, and **negative sampling**
- [ ] find out how the big models are doing it (there own methods? how many parameters are they using? what model are they using?)
