# Transfer Impv

### preprocess impv
* LARE method
* prepare file:
  * download gloss_embedding.npy in https://cloud.tsinghua.edu.cn/d/f6baaff5c398463388b2/ to src_LARE/
  * download SentiWordNet_3.0.0.txt in https://github.com/aesuli/SentiWordNet to src_LARE/
  * unzip stanford-postagger-full-2020-11-17 in https://nlp.stanford.edu/software/tagger.html to src_LARE/stanford-postagger-full-2020-11-17
* tune the bound rate in preprocess_LARE.py
  * As Boundrate grows, the tokens in the sent are more likely to be neither negative and positive
* run 
```
bash ./scripts/LARE/preprocess_amazon_LARE.sh
bash ./scripts/LARE/preprocess_yelp_LARE.sh
```
to preprocess the raw data using LARE method

In fact, the preprocessed data are contained in the project

***

### run finetune
run
```
bash ./scripts/LARE/fine_tune_amazon_LARE.sh
```
or
```
bash ./scripts/LARE/fine_tune_yelp_LARE.sh
```
to run the finetune process.