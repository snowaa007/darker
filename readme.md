# DARKER
The code and full version with Appendix of DARKER. 
The full version of DARKER is shown in full_version.pdf

## Setup
```bash
pip install -r requirements.txt
```


We use the UEA datasets. Download the raw, preprocess, weights data from https://lifehkbueduhk-my.sharepoint.com/:f:/g/personal/21482276_life_hkbu_edu_hk/EnI9aWHAXnBDrXyP5-d5_lwBcvIbRGBvgs-iOc0Tn1cMgA?e=Ojluxf

Create data folder
```bash
mkdir data
```
You can directly put all files from download link to data/

Or for a specific dataset named BasicMotions, put it as follows:

```bash
mkdir data/raw
mkdir data/preprocess
mkdir data/preprocess_learned
```

Put raw data from download link /raw/ in dir:
```bash
data/raw/BasicMotions
```
Put the preprocessed data from download link /preprocess/ in dir:
```bash
data/preprocess/BasicMotions
```

Put the weights data from download link /preprocess_learned/ in dir:

```bash
data/preprocess_learned/BasicMotions
```



## Run an example
To run an example:
```bash
cd src
python main.py --dataset BasicMotions
```

## For other datasets and settings

To train a dataset with name "dataset_name"
```bash
python src/main.py  --dataset dataset_name
```

To train a dataset for a baseline (e.g.full attention)

```bash
python src/main.py  --dataset dataset_name --model_name full
```

To train a dataset for a method with hyperparameters (epcochs and batch size)

```bash
python src/main.py  --dataset dataset_name --epochs 200 --batch_size 32
```

## Acknowledgments

Thanks for the research community for supporting the datasets, particularly grateful for the UCR/UEA TSC archive.

If you find this code or any of the ideas in the paper useful, please consider citing:

```bash
@article{zuovldb2024,
author = {Zuo, Rundong and Li, Guozhong and Cao, Rui and Choi, Byron and Xu, Jianliang and Bhowmick, Sourav S},
title = {DARKER: Efficient Transformer with Data-Driven Attention Mechanism for Time Series},
year = {2024},
issue_date = {July 2024},
publisher = {VLDB Endowment},
volume = {17},
number = {11},
issn = {2150-8097},
doi = {10.14778/3681954.3681996},
journal = {Proc. VLDB Endow.},
month = {aug},
pages = {3229–3242},
numpages = {14}
}
```



# Previous work
DARKER improves the efficiency of transformer for time series.
Readers who are interested in time series transformer may refer to our previous work SVP-T (https://github.com/rdzuo/svp-transformer).

