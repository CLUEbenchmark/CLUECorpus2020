# CLUECorpus2020

## 语料介绍

通过对<a href='http://commoncrawl.org'>Common Crawl</a>的中文部分进行语料清洗，最终得到100GB的高质量中文预训练语料。具体的数据介绍和我们的实验分析参见我们的<a href=''>技术报告</a>。
数据特点：
1. 可直接用于预训练、语言模型或语言生成任务。
2. 发布专用于简体中文NLP任务的小词表。

## 词表介绍

Google原始中文词表和我们发布的小词表的统计信息如下：

| Token Type | Google | CLUE |
| :----:| :----: | :----: |
| Simplified Chinese | 11378 | 5689 |
| Traditional Chinese | 3264 | ✗ |
| English | 3529 | 1320 |
| Japanese | 573 | ✗ |
| Korean | 84 | ✗ |
| Emoji | 56 | ✗ |
| Numbers | 1179 | 140 |
| Special Tokens | 106 | 106 |
| Other Tokens | 959 | 766 |
| Total | 21128 | 8021 |

## 实验效果

使用小数据集在BERT-base上的效果对比：

| Model        | Vocab  | Data        | Steps | AFQMC  | TNEWS'  | IFLYTEK'  | CMNLI  |  AVG   | 
| :----:| :----: | :----: | :----: |:----: |:----: |:----: |:----: |:----: |
| BERT-base    | Google | Wiki (1 GB) | 125K  | 69.93% | 54.77%  | 57.54%    | 75.64% | 64.47% |
| BERT-base    | Google | C5 (1 GB)   | 125K  | 69.63% | 55.72%  | 58.87%    | 75.75% | 64.99% |
| BERT-base    | CLUE   | C5 (1 GB)   | 125K  | 69.00% | 55.04%  | 59.07%    | 75.84% | 64.74% |
| BERT-base mm | Google | C5 (1 GB)   | 125K  | 69.57% | 55.17%  | 59.69%    | 75.86% | 65.07% |
| BERT-base    | Google | C5 (1 GB)   | 375K  | 69.85% | 55.97%  | 59.62%    | 76.41% | 65.46% |
| BERT-base    | CLUE   | C5 (1 GB)   | 375K  | 69.93% | 56.38%  | 59.35%    | 76.58% | 65.56% |
| BERT-base    | Google | C5 (3 GB)   | 375K  | 70.22% | 56.41%  | 59.58%    | 76.70% | 65.73% |
| BERT-base    | CLUE   | C5 (3 GB)   | 375K  | 69.49% | 55.97%  | 60.12%    | 77.66% | 65.81% |

更多实验结果和分析可以参考：<a href='https://github.com/CLUEbenchmark/CLUEPretrainedModels'>CLUEPretrainedModels</a>

## 数据下载

申请方式：
将使用语料研究目的和用途，计划、研究机构和申请者介绍，发送到邮箱，并承诺不向第三方提供。

邮箱: CLUEbenchmark@163.com，标题是：CLUECorpus2020 100G语料库

## 反馈和支持

可以提交issue，加入讨论群(QQ:836811304)

或发送邮件 CLUEbenchmark@163.com

Research supported with Cloud TPUs from Google's TensorFlow Research Cloud (TFRC)


