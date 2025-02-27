#  中英文关键词抽取
欢迎使用关键词抽取，支持多种关键词抽取算法，涵盖内容如下图所示：
![image](images/main.png)



## 介绍

关键词抽取支持多种算法，算法如下：
- [中英文关键词抽取](#中英文关键词抽取)
  - [介绍](#介绍)
  - [API](#api)
    - [1.TF-IDF](#1tf-idf)
    - [2.TextRank](#2textrank)
    - [3.KeyBERT](#3KeyBERT)
    - [4.Word2Vec](#4Word2Vec)
    - [5.LDA](#5LDA)
  - [路线](#路线)
  - [注意](#注意)




---
## API



### 1.TF-IDF


```python
from keyword_extract import KeywordExtract

input_list = [
    "自然语言处理是人工智能领域中的一个重要方向。它研究人与计算机之间如何使用自然语言进行有效沟通。"
]
key_extract = KeywordExtract(type="TF-IDF")
# 基于TF-IDF进行关键词的抽取
print(key_extract.infer(input_list))
```

### 2.TextRank


```python
from keyword_extract import KeywordExtract
   
input_list = ["自然语言处理是人工智能领域中的一个重要方向。它研究人与计算机之间如何使用自然语言进行有效沟通。"]
key_extract = KeywordExtract(type="TextRank")
# 基于TextRank进行关键词的抽取
print(key_extract.infer(input_list))

```
### 3.KeyBERT


```python
from keyword_extract import KeywordExtract
  
input_list = ["自然语言处理是人工智能领域中的一个重要方向。它研究人与计算机之间如何使用自然语言进行有效沟通。"]
key_extract = KeywordExtract(type="KeyBERT")
# 基于KeyBERT进行关键词的抽取
print(key_extract.infer(input_list))

```

### 4.Word2Vec


```python
from keyword_extract import KeywordExtract

input_list = ["自然语言处理是人工智能领域中的一个重要方向。它研究人与计算机之间如何使用自然语言进行有效沟通。"]
key_extract = KeywordExtract(type="Word2Vec")
# 基于Word2Vec进行关键词的抽取
print(key_extract.infer(input_list))

```

### 5.LDA


```python
from keyword_extract.lda_model.lda import LDA
 
input_list = ["自然语言处理是人工智能领域中的一个重要方向。它研究人与计算机之间如何使用自然语言进行有效沟通。"]
lda_model = LDA(type="LDA")
# 基于LDA 进行关键词的抽取,topic_num是主题的个数
print(lda_model.infer(input_list, topic_num=3))

```

## 路线

* [X] 支持TF-IDF关键词抽取算法
* [X] 支持TextRank关键词抽取算法
* [X] 支持KeyBERT关键词抽取算法
* [X] 支持Word2vec的关键词抽取算法
* [X] 支持LDA的关键词抽取算法
* [] 支持pip的安装




## 注意

