# 自然语言与机器翻译大作业
*from 张靖男-2001865*
## Part1 准备数据

#### **准备环境**

* python3.6 
* pypinyin==0.37.0
* jieba==0.42.1
* Levenshtein==0.12.0 

#### **数据爬取**

  python spider.py

#### **清洗数据**

  python heqilai.py
  python clean.py
  python quchong.py
  python siju.py

#### **划分训练集和测试集**

  python train_test.py

## Part2 训练及生成

#### **准备环境**

* python3.6 
* tensorflow_gpu==1.10.0
* cuda9.0+cudnn
* pypinyin==0.37.0
* tornado==5.0.2
* Levenshtein==0.12.0 

#### **数据预处理**

python prepare_data.py

#### **训练**

python train.py -y 五言或七言 -c 藏头或藏尾

例如：python train.py -y 7 -c "TOU"

#### **生成**

python generate.py -k 藏头（尾）词 -y 五言或七言 -c 藏头或藏尾

例如：python generate.py -k "江南好" -y "七言" -c "藏头"

#### 界面展示

python start.py

## Part3 诗歌评价 

#### **准备环境**

* python3.6 
* tensorflow_gpu==1.10.0
* cuda9.0+cudnn
* pypinyin==0.37.0
* Levenshtein==0.12.0 
* jieba==0.42.1

#### 计算各方面评价的权值

python get_weights.py

#### 对诗歌进行评价

python access.py -i 输入文件路径 -o 输出文件路径

例如：python access.py -i data/评价/access.txt -o data/评价/res.txt
