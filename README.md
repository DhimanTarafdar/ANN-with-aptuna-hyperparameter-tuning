# Fashion MNIST ANN with Optuna Hyperparameter Tuning (Notebook)

## Overview

আগে আমি **Fashion MNIST dataset** এর উপর PyTorch ব্যবহার করে একটি ANN pipeline তৈরি করেছিলাম।
কিন্তু তখন গুরুত্বপূর্ণ hyperparameter গুলো যেমন:

* hidden layer কয়টা হবে
* প্রতি layer এ neuron সংখ্যা
* batch size
* learning rate
* number of epochs

 এগুলো আমি পুরোপুরি নিজের intuition এর উপর ভিত্তি করে সেট করেছিলাম।

---

## In This Notebook

এই notebook-এ আমি **Bayesian Optimization** ব্যবহার করে
**Optuna library** এর মাধ্যমে hyperparameter tuning করেছি 

 এখানে manually guess না করে,
Optuna automatically খুঁজে বের করে কোন parameter combination model-এর performance improve করে।

---

## What’s Inside

* PyTorch দিয়ে ANN implementation
* GPU support (CUDA detection)
* Configurable neural network (dynamic layers & neurons)
* Training & evaluation pipeline
* Optuna-based hyperparameter optimization

---

## Tuned Hyperparameters

এই notebook-এ নিচের hyperparameter গুলো optimize করা হয়েছে:

* `num_hidden_layers`
* `neurons_per_layer`
* `epochs`
* `learning_rate`
* `dropout_rate`
* `batch_size`
* `optimizer` (Adam / SGD / RMSprop)
* `weight_decay`

---

## Optimization Details

* Strategy: **Bayesian Optimization**
* Library: **Optuna**
* Multiple trials run করে best parameter খুঁজে বের করা হয়েছে

---

## Model Summary

* Input: 784 (28×28 image flattened)
* Output: 10 classes
* Activation: ReLU
* Regularization: Dropout + BatchNorm
* Hidden Layers: Optuna দ্বারা dynamically selected

---

## Key Insight

 আগে যেখানে intuition দিয়ে parameter set করতাম,
এই notebook-এ Optuna ব্যবহার করে **data-driven approach** follow করেছি।

 এর ফলে better accuracy এবং optimized performance পাওয়া গেছে।

---
