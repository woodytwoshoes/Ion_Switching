{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "This was my attempt at tackling the ion switching dataset. \n",
    "My attempted approaches were \n",
    "\n",
    "Features:\n",
    "1. Single feature\n",
    "2. Window of features\n",
    "3. Sampling of features in neighbourhood of central feature by distance increasing by golden ratio\n",
    "\n",
    "Models\n",
    "1. Logistic regression\n",
    "2. Linear Regression\n",
    "3. Logistic regression with ordinal probabilistic modelling\n",
    "4. Neural network (3 hidden layers, pytorch)\n",
    "5. Logistic regression with ordinal probabilistic modelling\n",
    "\n",
    "Initially I had hoped that I could rely on my neural network to compensate for the obvious drift in the dataset (varying baseline) however the construction of a feature that would prompt the neural network to interpret the baseline was a massive barrier due to compute power (there is probably a way to optimise that feature engineering). Therefore I decided that signal preprocessing would yield better results. After applying some techniques used for spectroscopy and finding them inadequate (probably due to difficulty choosing the right parameters) I submitted based on my best result (ordinal logistic regression).\n",
    "\n",
    "After reviewing the high ranking entries it is clear that a rolling average to find the baseline was the most appropriate approach.\n",
    "\n",
    "Overall, this was a great learning experience and challenged me to\n",
    "\n",
    "1. Engineer appropriate features\n",
    "2. Optimise compute power so that feature engineering can be done in a timely fashion\n",
    "3. Seek expert advice on signal preprocessing before applying a NN"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
