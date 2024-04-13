# TITLE-CONVERSATION SUMMARIZER
# SHORT DESCRIPTION
- By using this project you can summarize the conversations of two people or the group,it is based on the "Pegasus" model which I have fine tuned for "text summarizer" further more trained on "Samsum" dataset which contains several dialogues between people and there summary.
# HOW TO USE
- You have to assign variable sample test with your dialogues which you wants to be summarized, you can also set the length of your desired summary by changing the max_length parameter and length penalty parameter in gen_kwargs and then you will get your desired summary.
# DETAILED DESCRIPTION
> * Firstly I have set the coding environment by importing all the necessary libraries,model and dataset and used GPU provided by google colab so that the trianing process is fast .
> * After setting the coding environment ,I have written a function to do all the text preprocessing required in nlp project which included punctuation removal,lowering the text,tokenization,stop word removal and lemmatization by using the tokenizer of nltk library and converted input data into batches.Data is already splited into train,test and validation therefore no need to do train_test_split.
> * Then a function is written for input and output encoding and from transformer datacollaboratorforseq2seq is imported as we have made a text summarizer which takes input as sequence and provide output as also a sequence.
> * Now the model is trained by assigning the required values for all the parameters setting epochs to 2 having 1840 steps,as more than two epoch will take more time while reducing the lose by a negligible factor,loss is printed after each 500 steps.
> * Score is calculated using rouge metrics, model and tokenizer is saved and then sampling is done,got ROUGE-N score of 0.5 and ROUGE-W score of 0.4.
# MOTIVATION AND WHAT YOU GOT FROM THIS PROJECT
- I got the motivation to build this model by feeling its need in Indian Intelligence and police department,as they contain the long records of telephone conversations of suspected people and spend a lot of time hearing or reading them ,think what if there work of reading and interpreting the information is done by a AI tool ,it will save a lot of time by just giving you the interpreted information which can be used to get insights or clue about the case.