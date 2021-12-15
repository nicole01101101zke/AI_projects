seq2seq_en_de_10000.ipynb这份代码理论上可以在本地运行或在colab上运行。

本地运行，部分与colab相关的代码块可以删除。

在colab上运行，需要使用谷歌浏览器，登陆有效的谷歌账号和能够访问colab网站。

##### 1.在笔记本设置中选择GPU和高RAM运行时，保证训练时有充足的大规模并行算力和内存

##### 2.设置依赖文件路径

为了保证colab可以访问需要用到的外部文件（主要是训练集、验证集和测试集文件），需要挂载谷歌云里的文件夹。

用colab打开我们的.ipynb文件，运行下面的代码执行单元：

```python
from google.colab import drive
drive.mount('/content/drive')
```

在输出栏会出现一个链接和一个输入框，进入链接复制授权码，将其粘贴回输入框，点回车键完成授权步骤。

##### 3.数据集

数据集全部在/content/drive/MyDrive/AI/project3/dataset/路径下

训练集使用news-commentary-v11.de-en.en和news-commentary-v11.de-en.de的前10000条

验证集使用dev中的newstest2010.en和newstest2010.de

测试集使用test中的newstest2016-ende-src.en.sgm和newstest2016-ende-ref.de.sgm

##### 4.环境配置

各种模块版本与当前colab pytorch默认的版本一致即可。
