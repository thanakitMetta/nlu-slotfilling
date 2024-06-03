# nlu-slotfilling

NLU Slot Filling Idea:

The objective of the task is to discover and extract relevant data from the provided text,
then map that information to predicted slots. So, I decided to use word2feature combined with
the CRF model as the main concept. This approach is perfectly suited to deal with the sequence
labeling problem in the context of this task. Word2feature is important since the dataset needs to
be transformed into a feature vector before being entered into the CRF model. In addition,
‘STOP_WORDS’ has been added inside the model to return a list of commonly occurring words
in the English language. For the CRF model, it used ‘lbfgs’ as its algorithm, L1 and L2
regularization are set to 0.1, the maximum iterations is 250, and the model will include all
possible label transitions.

NLU Slot Filling Good Points and Difficult parts:

A difficult part is in the preprocessing section, when I must organize the dataset to fit in
the CRF model. This part took me almost a day to finish. For the good points of this model, The
sequence labeling model may become more accurate and effective, and it may also allow for
more flexibility in the development of features that are unique to the use cases. Furthermore,
using word2feature along with CRF model help to reduce overfitting and improve generalization.

The Lesson Learn in NLU Slots Filling Task:

According to the solid part of this hackathon, I have learned a lot in the preprocessing
part. This involves tokenizing the data, POS tagging, named entity recognition, and data
cleaning
