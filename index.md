## An Overview on Language Models

Have you ever wondered how your phone knows what word you’re about to type before you actually type it? Are these devices reading our minds now? Fortunately, not yet. 

Our phones have technology embedded in them that uses probability distribution, also known as fancy math, on words to predict what word best fits the sentence that you have already partially typed. These are known as language models. Although it is a relatively new technology, many different kinds of language models have been created in the past few years. In this article, I intent to explore what language models are, how they are used and how they have impacted the natural language processing community.
 
### Background

As our devices get smarter, people, especially who’s not so familiar with computer science, might think that they are starting to gain actual abilities. What we need to keep in mind is that computers are dumb pieces of hardware, and able to perform all the tasks that they do through mathematical computations. So, the first question we need to pose is “How do they work?”.
Language models can be used for several different tasks such as question answering, speech recognition, sentence completion, grammar checkers, machine translation, etc. However, for the purpose of this article, I will base my examples on sentence completion in order to answer our question at the top. 

Sentence completion language models can be created by simply using probability as portrayed in the imaged below. 

![here](corpus.png)
The above image represents our corpus (the words that compose out text),
![](prob-eq.png)
And the above equation calculates the probability of Wn to be followed by Wn-2 Wn-1. 
Let’s put in some real words for it to make sense:
![](prob-example.png)
Images courtesy of [exploredatabase.com](https://www.exploredatabase.com/2020/04/bigram-trigram-and-ngram-language-model-in-nlp.html)

Following this probabilistic equation in the image above, we can calculate the probability of the word “of” following the word “prime minister”. This is the simpler approach for creating a language model. However, there’s several reasons why this is not the most accurate approach. As we can see, the probability of one word following another is solely based on the preceding n words we are considering. As the text gets more complex and lengthier, the next word in a sentence might not be directly related to the previous n words. This approach is also not ideal performance wise because as the number n increases, the computation gets more expensive. 
The probabilistic language model drawbacks take us toward a more complex but effective approach: neural networks. Simply put, neural networks are a mathematical representation of how human brains work, where each node in the network represents a neuron and each edge in the network represents an axon (refer to the image below). 

![](axon.png)
Image courtesy of [this github page](https://github.com/fastai/fastbook/blob/master/01_intro.ipynb)

The idea is that the network would be trained on a, usually large, dataset coming in from the input layer, going through a series of hidden layers, and then coming out from the last layer of the network, the output layer. While training, the network starts picking up on patterns, using threshold and weight values as guides, in the training dataset and learns to recognize them. By letting the network know when it got the right answer and vice-versa, it starts correcting the wrong answers and improving its accuracy score (the percentage of correct answers). 
This is a very high-level description of how neural networks work but enough to understand the rest of this article. However, if you’re interested in learning more about them, start by checking out [this post](https://www.ibm.com/cloud/learn/neural-networks).

![](nn.png)
Image courtesy of [ibm.com](https://www.ibm.com/cloud/learn/neural-networks).

Neural networks overcome the probabilistic model performance issues by being able to consider all the previous words when choosing the next word without impacting performance especially when using recurrent neural networks. A recurrent neural network is just a special kind of neural network with a keen ability to remember sequences from the input they received, which is why they are mainly used to make predictions on what’s coming next in the sequence.
Although, recurrent neural networks reach state-of-the-art results in sentence completion tasks, there is one more technique used to address sentence completion that I want to explore: transformers. 
Transformers made their way into the natural language community only a few years ago when Google published the [Attention is all you need](https://arxiv.org/abs/1706.03762) paper. 


### Discussion

- What are the main points that the writer wants the reader to know about this topic?


### Conclusion

- Why should a reader care about this topic?
- What should a reader take away?


### References 

Here’s the list of the wonderfully helpful articles I used as sources for my own. 
- [A beginner’s guide to language models](https://towardsdatascience.com/the-beginners-guide-to-language-models-aa47165b57f9),
- [BERT language model](https://www.techtarget.com/searchenterpriseai/definition/BERT-language-model),
- [10 Leading Language Models For NLP In 2021](https://www.topbots.com/leading-nlp-language-models-2020/)
