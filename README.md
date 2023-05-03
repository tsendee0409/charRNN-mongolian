# Mongolian charRNN model for ml5js

## Train model in Docker container

### Mongolian Text

```bash
$ sudo docker run -it --rm -v "$PWD":/usr/src/char-rnn -w /usr/src/char-rnn tensorflow/tensorflow:1.15.4 python train.py --data_path mongolia.txt --rnn_size 128 --num_layers 2 --seq_length 32 --batch_size 32
```

### Mongolian Long Text

```bash
$ sudo docker run -it --rm -v "$PWD":/usr/src/char-rnn -w /usr/src/char-rnn tensorflow/tensorflow:1.15.4 python train.py --data_path mongolia-long.txt --rnn_size 128 --num_layers 2 --seq_length 128 --batch_size 128
```