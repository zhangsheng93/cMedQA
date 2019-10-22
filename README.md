首先谢谢前辈辛苦做的数据集，方便我们追随者使用。在使用数据集时发现两个问题 像前辈反映一下。用的版本1
 1、一个是train_candidates.txt   test_candidates.txt  dev_candidates.txt  ，在利用question.csv 和answer.csv 联合 读取时 （padas 以及python  自己的read wrtie 手写的）， 个别question_id  在question.csv  不存在，并且还挺多。以至于
 本该150万条（50万*30）的训练集 读完样本个数只有18万（187259）
 本该20万（2000*100）的dev  test 读完样本个数只有2.1万 和2.6万  （21200 26500）  三者都比预期少了将近10倍，
 也就train_candidates.txt   test_candidates.txt  dev_candidates.txt   有效数据0.1，不知道前辈们清楚么
2、 读完后，发现train_candidates.txt  生成训练数据中好多（q,a+,a-） 对应q 的正答案a+  和问题根本不相关；
对于test_candidates.txt  dev_candidates.txt  读取后 ，（q,a,id,label）label为1的答案，本来该是正答案，结果也和q bu相关。目前没统计类似情况的分布程度，但这对实验会没影响么。


# cMedQA v1.0
This is the dataset for Chinese community medical question answering. The dataset is in version 1.0 and is available for non-commercial research. We will update and expand the database from time to time. In order to protect the privacy, the data is anonymized and no personal information is included.

# Update

The newest version of cMedQA now comes to v2.0. You can [click here](https://github.com/zhangsheng93/cMedQA2)


# Overview

| DataSet | #Ques | #Ans | Ave. #words per Question |  Ave. #words per Answer| Ave. #characters per Question | Ave. #characters per Answer |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|Train|50,000|94,134|97|169|120|212|
|Dev|2,000|3,774|94|172|117|216|
|Test|2,000|3,835|96|168|119|211|
|Total|54,000|101,743|96|169|119|212|

* **questions.csv**  All Questions and their content.
* **answers.csv**  All Answers and their content.
* **train_candidates.txt** **dev_candidates.txt** **test_candidates.txt** The split of training set, development set and test set respectively.

# Paper
**Chinese Medical Question Answer Matching Using End-to-End Character-Level Multi-Scale CNNs** [link to the paper](http://www.mdpi.com/2076-3417/7/8/767)

Please cite our paper when you use the dataset.
```
@article{zhang2017chinese,
  title={Chinese Medical Question Answer Matching Using End-to-End Character-Level Multi-Scale CNNs},
  author={Zhang, Sheng and Zhang, Xin and Wang, Hui and Cheng, Jiajun and Li, Pei and Ding, Zhaoyun},
  journal={Applied Sciences},
  volume={7},
  number={8},
  pages={767},
  year={2017},
  publisher={Multidisciplinary Digital Publishing Institute}
}
```
