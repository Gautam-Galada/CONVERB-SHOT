# CONVERB-SHOT


CONVERB SHOT


This project is basically an oriented NLP architecture which consists of concepts like Fully connected neural networks, Lancaster stemmers, zero-shot learning/classifications and other pre-processing techniques. 

FNN
This part of the architecture is fed with intents.json which consists of 



This is where the model training begins.
The model is built using tflearn. Since it's a pattern based approach with a certain set of questions the model training is prone to give 100% accuracy. If we automate the training questions dataset then we can expect less than a 100% accuracy. 

For training we use Lancaster stemmer to normalize the word embedding and make it simple for the model to train. Lancaster stemmer is robust and quick but not accurate, so we define the model outlook to be pattern oriented to reduce the loss value. 

A normal conversation is initiated between the user and the chatbot. The user inputs the text, it is sent for testing to the fully connected network, if certain words like "support system"  are used then the input feed is sent to zero shot classification model. 

Zero shot classification works well with unseen data. A unique statement is a good test case and to deal with it zero shot learning can be a good approach.
Zero shot learning is a probabilistic model which tries to train on word embedding in a vector space and correlates it with the unseen data. 

Now these probabilistic values are of the classes pre-defined with the model classification. These classes are then captured in a dictionary and then mapped with the api keys. These api keys are the pathway to the support channels. 

Note : 
Until and unless certain keywords which help in invoking the zero shot classifier it will not communicate to the support and just be a stand alone chatbot.






