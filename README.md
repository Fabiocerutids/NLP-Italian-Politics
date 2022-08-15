# NLP-Italian-Politics
In our project we are analysing the speeches made by italian parliamentarians at the italian parliament. The overall aim of our project is to generate a suite of NLP tools that can be used to aid social and political scientists with research on italian politics. With the scarcity of NLP models that go beyond just the english language the need for such tools if of increasing importance. As such our research questions are:

* Are there semantic differences in the way parliamentaries from different parties and political background speak?
* Can we exploit such differences and similarities to build a classifier that can effectively predict which party a politician belongs to by using what they said and a few demographic qualities?
* Can we build an effective POS tagger that is specialised on italian political language?

To accomplish those goals, we have constructed 3 different notebooks:
* Preprocessing&Exploratory.ipynb: Such notebook deals with the required preprocessing needed in order to study italian text. It also reports an exploratory analysis that employs Word2Vec, Doc2Vec, BERT, TSNE, Clustering and Topic Modelling that answers the first research question
*  Classification.ipynb: The notebook reports the data preparation and different models used to classify speeches. The best performance achieved is via Gradient Boosting (employing CATboost), attaining an F1 score on test data of 0.85 
Note: We employed a suit of Neural Networks but noticed significantly poorer performance than our best model
* StructuredPrediction.ipynb: The notebook contains the processing and structured prediction algorithms used to predict POS tagging of unseen text. The models used in this section are: the Structured Perceptron with both Greedy and Viterbi search, Convolutional Neural Networks, Bi-LSTM.
Overall, all models performed well on test data (all models achieved at least 97% accuracy). We observed as the best model the Structured Percpetron with Greedy search, achieving an accuracy of 99% on test data.
