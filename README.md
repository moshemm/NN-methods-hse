# NN-methods-hse

This is a repo for HWs or any pther trials for [HSE NN methods in NLP course (2021-2022)](https://github.com/daria-sa/NNmethods_ba_hse21-22).

## Contents:
1. [MLP](MLP_cedr.ipynb) for [Cerd dataset](https://huggingface.co/datasets/cedr)
2. [CNN](CNN-HW2_1.ipynb) for [RuTweetCorp Dataset](http://study.mokoron.com):
> CNN на уровне слов: модель берет слова, пропускает их через Embedding слой. По эмбеддингам проходит CNN c фильтрами с разным окном, полученные результаты конкатенируются друг с другом по глубине, по результату конкатенации еще один сверточный слой, далее max pooling over time, на выходе линейный слой + сигмоида, функция потерь BCELoss.
