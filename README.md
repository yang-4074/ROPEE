# ROPEE


## 1. Environments

```
- python (3.7.16)
- cuda (11.4)
```

## 2. Dependencies

```
- torch (1.7.0)
- transformers (4.9.1)
```

## 3. Dataset

- FewFC: Chinese Financial Event Extraction dataset. The original dataset can be accessed at [this repo](https://github.com/TimeBurningFish/FewFC). Here we follow the settings of [CasEE](https://github.com/JiaweiSheng/CasEE). Note that the data is avaliable at ``/dataset/FewFC/data``, and we adjust data format for simplicity of data loader. To run the code on other dataset, you could also adjust the data as the data format presented.

## 4. Run

1. Download [bert-base-chinese](https://huggingface.co/bert-base-chinese#) to file bert-base-chinese.

2. Train/Dev/Test the model: Run as follows to train/dev/test the model:

```
CUDA_VISIBLE_DEVICES=0 python -u main.py --output_model_path ./models_save/model.bin --do_train True --do_eval True --do_test True > logs/model.log
```

The hyper-parameters are recorded in ``/utils/params.py``. 

