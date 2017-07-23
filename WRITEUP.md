# Deep-Learning-Final-Project

DATA DESCRIPTION:

TED-LIUM Corpus

This is the TED-LIUM corpus release 2, 
licensed under Creative Commons BY-NC-ND 3.0 (http://creativecommons.org/licenses/by-nc-nd/3.0/deed.en). 

All talks and text are property of TED Conferences LLC. 

--- 

The TED-LIUM corpus was made from audio talks and their transcriptions available on the TED website. We have prepared and filtered these data in order to train acoustic models to participate to the International Workshop on Spoken Language Translation 2011 (the LIUM English/French SLT system reached the first rank in the SLT task). 

More details are given in this paper: 

A. Rousseau, P. Deléglise, and Y. Estève, "Enhancing the TED-LIUM Corpus with Selected Data for Language Modeling and More TED Talks",
in Proceedings of the Ninth International Conference on Language Resources and Evaluation (LREC’14), May 2014.

--- 

Contents: 

- 1495 audio talks in NIST sphere format (SPH) 
- 1495 transcripts in STM format 
- Dictionary with pronunciation (159848 entries) 
- Selected monolingual data for language modeling from WMT12 publicly available corpora

ABSTRACT & SUMMARY:
The goal of the project is aim to show the great performance of using deep learning in text classification for a supervised dataset of TedTalk transcripts whether the speech is from a male voice or female voice. The training/learning is gone through two comparable methodologies which is a baseline model using scikit learn versus a strong deep learning model using keras modules. The evaluation showed that the accuracy for baseline model is about 99.7% while with the right metric evaluation( in this case, it's k-top-categorical-accuracy), deep learning model is able to predict correctly 100%. This shows that deep learning model is really powerful in advanced contexts.

QUESTION & ANSWERS:
* What was the biggest challenge/obstacle/hurdle?

During the training, the challenges are scattered through each step, the biggest challenge is during the training proccess. Since putting the wrong hyperparameters would yield a significant wrong result, it did take time and tests to investigate the optimized result.

* If you had two more weeks what would you do?

If there are additional time for this project, I would likely to explore with more complex classification rather than just male and female. It can be subject/topic classification such as science, math, environment, english,... .
    
* Does it scale?

Yes, the model is able to be flexible for adjusting size of all keras parameters such as embedding dimension, MAX_SEQUENCE_LENGTH 

* How would you turn your project in a data product?

To do so, the input data must have to be formatted in same way with the Tedtalk transcript document. The input data will then be able to preprocessed. All parameters in keras would have been set to be bigger or smaller upon the size of dataset or user's choice.

* Why does your deep learning model beat your baseline?

Deep learning is able to adjust weight by using different optimizers, by doing so, accuracy is slightly improved but it will results in high tradeoff with loss.

* What are the tradeoffs between your baseline and your deep learning model? Would you put your deep learning model into production over your baseline? Why or why not?

Even though multiple loss functions have been tested, the training still shows high loss tradeoff with accuracy. Because of this, the model maybe not be considered as a perfect model for data production.

* What evidence can you provide that your model has generalized correctly?

Evaluation for test data always reach 100% for every repeat test.

* Are your results significant?
Yes, they are.

* What hyperparameters mattered? Which didn't?

Metrics is the most important hyperparameter among others. For the imbalance dataset, the wrong metrics had leaded to the significant incorrect predictions.

* Why did or didn't you use accuracy as your evaluation metric?
I start by testing with different metrics and it appears that k-top-categorical-accuracy showed the top result. Its algorithm works by calculate how often a target class is within the top-k predictions.
