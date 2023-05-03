# Mongolian charRNN model for ml5js

This repository is fork of [training-charRNN](https://github.com/ml5js/training-charRNN)

## Train model in Docker container

### Mongolian Text

```bash
$ sudo docker run -it --rm -v "$PWD":/usr/src/char-rnn -w /usr/src/char-rnn tensorflow/tensorflow:1.15.4 python train.py --data_path mongolia.txt --rnn_size 128 --num_layers 2 --seq_length 32 --batch_size 32
```

### Mongolian Long Text

```bash
$ sudo docker run -it --rm -v "$PWD":/usr/src/char-rnn -w /usr/src/char-rnn tensorflow/tensorflow:1.15.4 python train.py --data_path mongolia-long.txt --rnn_size 128 --num_layers 2 --seq_length 128 --batch_size 128
```

## Webpage with ml5js

### Run Nginx in Docker container

```bash
$ sudo docker run --name char-rnn-nginx -v "$PWD/models":/usr/share/nginx/html:ro -p 80:80 -d nginx:latest
```