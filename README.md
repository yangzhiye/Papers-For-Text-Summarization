# Papers-For-Graduation-project

## 论文调研

### 文本摘要相关论文

#### 1. LCSTS: A Large-Scale Chinese Short Text Summarization Dataset [论文地址](http://www.aclweb.org/website/anthology/D/D15/D15-1229.pdf)

1. 爬取并过滤了240W+条微博蓝V发布的[摘要,短文本],这是本系统所采用的语料。
2. 本文提出了word-based和character-based(为了改善UNK问题)两种数据处理的方法,并给出了RNN和RNN+context两种模型做baseline。
3. RNN+Context+Char组合表现最好，ROUGE-1:0.299 ROUGE-2:0.174 ROUGE-L:0.272

* 本文的主要贡献就是提供短文本摘要的训练集，并给出了baseline。[我之前用tfidf提关键句ROUGE-1达到了0.28](https://github.com/yangzhiye/Short-Text-Summarization)，没干过他。感觉长文本和短文本摘要还是有一些区别的，可能短文本摘要要更注重句子压缩，长文本摘要更注重信息提取。先放一放，如果毕设需要使用该数据集就回头再看。

#### 2. The Automatic Creation of Lierature Abstracts [论文地址](http://courses.ischool.berkeley.edu/i256/f06/papers/luhn58.pdf)

1. TFIDF计算关键词->通过关键词的密集程度计算关键句->通过关键句形成摘要

* 1958年的古董文章，打印还把实验室的打印机给整坏了。简单粗暴，在[短文本数据集](https://github.com/yangzhiye/Short-Text-Summarization)和[NLPCC2017-task3新闻数据集](https://github.com/yangzhiye/NLPCC2017-task3)上实现了，效果还不错，可以作为毕设baseline。

#### 3. TextRank:Bringing Order into Texts [论文地址](http://www.aclweb.org/anthology/W/W04/W04-3252.pdf)

1. 使用Textrank方法提取文本中关键词/句

* 使用Textrank提取摘要是很常见的方法，在[NLPCC2017-task3新闻数据集](https://github.com/yangzhiye/NLPCC2017-task3)上实现了，但效果不如tfidf，目测IDF立功。
  