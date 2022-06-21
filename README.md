# NN-methods-hse

This is a repo for HWs or any pther trials for [HSE NN methods in NLP course (2021-2022)](https://github.com/daria-sa/NNmethods_ba_hse21-22).

## Contents:
1. [MLP](MLP_cedr.ipynb) for [Cedr dataset](https://huggingface.co/datasets/cedr)
2. [CNN](CNN-HW2_1.ipynb) for [RuTweetCorp Dataset](http://study.mokoron.com):
> CNN на уровне слов: модель берет слова, пропускает их через Embedding слой. По эмбеддингам проходит CNN c фильтрами с разным окном, полученные результаты конкатенируются друг с другом по глубине, по результату конкатенации еще один сверточный слой, далее max pooling over time, на выходе линейный слой + сигмоида, функция потерь BCELoss.


> Word level CNN: The model takes words, runs them through the Embedding layer (a trained one). A CNN with filters of various windows (2grams, 3grams) is passed through the embedding layer, the results are concatenated with each other in depth, another convolutional layer is added based on the concatenation result, then max pooling over time, the output is a linear layer + sigmoid, BCELoss loss function.

3. [CNN v2](CNN_HW2_2.ipynb) for [Cedr dataset](https://huggingface.co/datasets/cedr)
> Комбинация эмбеддингов и символьных признаков: У этой модели два входа, один для эмбеддингов слов (предобученных или обучаемых - я взяла предобученные, так как датасет маленький и эмбеддингам не хватает данных, чтобы обучиться + попрактиковаться в предобученных эмб.), из них берем max или mean, делаем вектор для предложения, поверх линейный слой - получаем вектор X. Другой вход сети для символьного представления слов (это обучаемый Embedding слой, он будет брать на вход batch_size x symbols_len и сопоставлять каждому символу в каждом слове один эмбеддинг). Следующий слой сверточный, примените фильтры разных размеров. Результаты агрегируются с помощью max pooling over time и полученные векторы конкатенируются с вектором X.


>Combination of embeddings and character features: This model has two inputs, one for word embeddings (pre-trained or trainable - I took pre-trained ones, since the dataset is small and embeddings do not have enough data to get trained + practice pre-trained embeddings), we take max or mean, make a vector for the sentence, on top of a linear layer - we get a vector X. 
>Another network input for the character representation of words (this is a trained Embedding layer, it will take batch_size x symbols_len as input and match each symbol in each word with one embedding). The next layer is convolutional, apply filters of different sizes. The results are aggregated using max pooling over time and the resulting vectors are concatenated with the X vector.
