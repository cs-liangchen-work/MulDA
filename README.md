# MulDA
复现MulDA论文中自己感兴趣的点。

MulDA: A Multilingual Data Augmentation Framework for Low-Resource Cross-Lingual NER

论文给出的原链接：https://github.com/ntunlp/mulda

### 实验数据：
conll2002+conll2003
包含：英语，德语，西班牙语，荷兰语。

### 实验1：XLM-R的baseline
使用conll2002+conll2003所有的语料训练xlm-r模型
测试集语言 | F1   
-|-
eng | 0.902148 |
de | 0.850924 |
esp | 0.893634 |
ned | 0.909061 |

仅仅使用英语
测试集语言 | F1   
-|-
eng | 0.903604 |
de | 0.672925 |
esp | 0.762153 |
ned | 0.775129 |


### 实验2：百度翻译API
英语->其他语言
PER0 was born in LOC1 进行翻译。
实体直接翻译，论文中的不想实现了。

全部英语实体：
  en+其他语言：
测试集语言 | F1   
-|-
eng | 0.894705 |
de | 0.697220 |
esp | 0.697220 |
ned | 0.776541 |

  仅仅其他语言：
测试集语言 | F1   
-|-
eng | 0.859633 |
de | 0.690036 |
esp | 0.679265 |
ned | 0.767588 |

实体替换为相应的语言之后：
  en+其他语言：
测试集语言 | F1   
-|-
eng |  |
de |  |
esp |  |
ned |  |

  仅仅其他语言：
测试集语言 | F1   
-|-
eng |  |
de |  |
esp |  |
ned |  |

### 实验3：mbart
标签BIOES线性化之后，
生成是前面添加语言类型：
使用训练的ner模型对生成后的进行筛选。

仅仅使用原始英语语料：
测试集语言 | F1   
-|-
eng |  |
de |  |
esp |  |
ned |  |

原始英文语料+翻译得到的其他语料（按照论文，实体都是英文的）：

测试集语言 | F1   
-|-
eng |  |
de |  |
esp |  |
ned |  |

