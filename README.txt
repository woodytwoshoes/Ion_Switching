Ion Switching Kaggle Challenge

________________________________

This was my attempt at tackling the ion switching dataset. 
My attempted approaches were 

Features:
1. Single feature
2. Window of features
3. Sampling of features in neighbourhood of central feature by distance increasing by golden ratio

Models
1. Logistic regression
2. Linear Regression
3. Logistic regression with ordinal probabilistic modelling
4. Neural network (3 hidden layers, pytorch)
5. Logistic regression with ordinal probabilistic modelling

Initially I had hoped that I could rely on my neural network to compensate for the obvious drift in the dataset (varying baseline) however the construction of a feature that would prompt the neural network to interpret the baseline was a massive barrier due to compute power (there is probably a way to optimise that feature engineering). Therefore I decided that signal preprocessing would yield better results. After applying some techniques used for spectroscopy and finding them inadequate (probably due to difficulty choosing the right parameters) I submitted based on my best result (ordinal logistic regression).

After reviewing the high ranking entries it is clear that a rolling average to find the baseline was the most appropriate approach.

Overall, this was a great learning experience and challenged me to

1. Engineer appropriate features
2. Optimise compute power so that feature engineering can be done in a timely fashion
3. Seek expert advice on signal preprocessing before applying a NN