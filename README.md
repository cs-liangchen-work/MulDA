# MulDA
复现MulDA论文中自己感兴趣的点。
MulDA: A Multilingual Data Augmentation Framework for Low-Resource Cross-Lingual NER

### 实验数据：
conll2002+conll2003
包含：英语，德语，西班牙语，荷兰语。

### 实验1：
使用conll2002+conll2003所有的语料训练xlm-r模型
测试集语言 | F1   
-|-
eng | 0.902148 |
de | 0.850924 |
esp | 0.893634 |
ned | 0.909061 |

