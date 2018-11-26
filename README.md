# Baisc Reading Comprehension

## Setup
Install Python 2.7
<br /> pip install nltk
<br /> [Download Stanford Parser](http://nlp.stanford.edu/software/stanford-parser-full-2015-04-20.zip) 
<br /> python2 read.py

## Baseline
Build Triples (S,V,O) (First without parser and then with) - Find the triples (embeddings) that match with the question and output them.

## Approach
We are building triplets (sunject, verb and object) and using them to identify answers for a question given.
To identify relationship betweens objects (nouns) in the sentence consider this sentence                                    <br/> Sita won a race against her brother to the bottom of the hill.

![](https://github.com/j07nikita/Baic-QA/blob/master/sita.png)

A key observation to answering questions is that they can be reworded to be fill in the blanks.                               <br/> Who did Sita win a race against? -> Sita won a race against _______

## Parsing
The first thing we have to do is parse the sentence to see the sentence structure and to determine which parts of a sentence are objects, verbs and propositions. To do this, we used the Stanford parser.

## Describing
We can use the parse tree to build the word graph by doing it recursively. For each grammar rule, we need to describe how to build the word graph.

## Answer
We can answer questions by converting the question to a “fill in the blank” and then following the words in the “fill in the blank” in the word graph to the answer. 

