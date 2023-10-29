# ROPEE

Joint Overlapping Event Extraction Model via Role Pre-judgment with Trigger and Context Embeddings using Classification ahead of Identification Strategy

> **Abstract:** The objective of event extraction is to recognize event triggers and event categories within unstructured text and produce structured event arguments. However, there is a common phenomenon that triggers or arguments of different event types in a sentence may be the same word elements, which poses new challenges to this task. In this article, a joint learning framework for overlapping event extraction (ROPEE) is proposed. In this framework, a role pre-judgment module is devised prior to argument extraction. It conducts role pre-judgment by leveraging the correlation between event types and roles, as well as trigger embeddings. Experiments on the FewFC show that the proposed model outperforms other baseline model in terms of TC, AI, and AC by 0.4%, 0.9%, and 0.6%. In scenarios of trigger overlap and argument overlap, proposed model outperforms baseline models in terms of AI and AC by 0.9%, 1.2% and 0.7%, 0.6% respectively, indicating the effectiveness of ROPEE in solving overlapping events.

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

