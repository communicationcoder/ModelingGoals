# ModelingGoals
This notebook applies LDA modeling to a an experimental dataset investigating participants' Instagram goal activation. 

## LDA topic modeling


The utility of topic modeling methods is their capability to uncover unobserved variables—topics—which shape the meaning of textual documents. Modern-day scholars utilize topic modeling to uncover latent topics from a wide array of textual information—from shorter texts, such as twitter posts to longer texts, such as journal articles.



This notebook applies LDA modeling to an experimental dataset investigating participants' Instagram use goals. 


### Key python libraries:
- gensim (https://radimrehurek.com/gensim/)
- nltk (https://www.nltk.org)
- spacy (https://spacy.io)

### Helpful Links:
- https://medium.com/@lettier/how-does-lda-work-ill-explain-using-emoji-108abf40fa7d
- https://towardsdatascience.com/light-on-math-machine-learning-intuitive-guide-to-latent-dirichlet-allocation-437c81220158


## A Comprehensive Example:

The data represent participants’ textual responses of 119 participants to the questionnaire described in the paper "A Theory-Driven Computational Measure of the Goal Activation in Communication Science." Participants were asked to list all the goals they could think of, leaving us with a total of 2976 documents—each participant providing up to 40 documents, across four time points. 

LDA assumes that a single document can contribute to multiple topics simultaneously; in other words, LDA explicitly models the actual distribution of words within each document. However, this assumption has drawbacks when modeling relatively shorter texts (e.g., twitter posts) because these documents may not contain enough meaningful words to model their distribution across topics. As a result, LDA models of longer texts produce more variance than with shorter texts. 

The goal of the analysis is to investigate participants’ responses of the questionnaire.

##  Steps of the analysis:

#### 1. Preparing data for LDA
    a. Spell check
    b. Expand contractions
    c. Read the data 
    d. Check data integrity
    e. Delete missing values
#### 2. Text preprocessing
    a. Tokenization
    b. Lemmatization  
    c. Stop Word Removal
    d. Bigrams and Trigrams
    e. Exclude terms in > 99% and < 1% of documents
    f. Generate Corpus and Dictionary
#### 3. Model selection (Selecting the number of topics (k))
    a. Computing Model Perplexity
    b. Analyzing model results through pyLDAvis visualization
    c. Saving selected model results
