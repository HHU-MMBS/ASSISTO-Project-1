# ASSISTO Project

## 1. Data Preparation

Let's start by preparing data. 

By runing `datapreparation/data_alignment.py`, we align the time series with the real daytime and split them to  one-hour intervals.

To read the data and split them to training and test sets, run the following code, `datapreparation/train_test_split.ipynb`,
which generates following files in format `.pickle`.
```
train_set.pickle
test_set.pickle
ood_set.pickle
```


## 2. Training

To train self-supervised model, run this command:
```train
python train.py --epochs 500 --batch_size 128 --lr 0.001 --hdim 128 --input_channel 512 --temperature 0.07 --window_size 1000
```

## 3. Evaluation
To evaluate the trained model, run this command:
```evaluation
python evaluation.py --model_path <path to checkpoint> --data_path <path to data>
```


