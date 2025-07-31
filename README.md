# Sentiment-Analysis-2

本次作業同HW2，要做情緒分析

請先下載資料集 yelp.csv

https://www.kaggle.com/omkarsabnis/yelp-reviews-dataset

將yelp.csv的資料切成兩部分，80%為train，20%為test

分別利用CNN與LSTM對train的資料建模，對test測試計算Accuracy

可使用Keras(建議)或Tensorflow來完成本次作業



作業流程：

1. 資料前處理(可延用HW2之方法)：

a. 讀取資料僅保留"text"、"stars"兩個欄位，利用分割符號切割字串、建立train&test之DataFrame

    並將stars欄位內值大於等於4的轉成1，其餘轉成0

    1: positive

    0: negative

b. 去除停頓詞stop words 

c. 文字轉向量（Tfidf 、Ｗord2vec …等 ）

2. 建模

a. 分別用CNN與LSTM對train的資料進行建模，可自行設計神經網路的架構

b. 加入Dropout Layer設定Dropout參數(建議0.7)進行比較

c. plot出訓練過程中的Accuracy與Loss值變化

3. 評估模型

a. 利用test的資料對2.所建立的模型進行測試，並計算Accuracy
