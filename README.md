# kidsearch
A search engine completed by [Qingsong Lv](https://github.com/1049451037), [Shulin Cao](https://github.com/ShulinCao) and [Yifan Wang](https://github.com/wangyifan0202). Our tutors are [Qian Yin](https://github.com/bnuyinqian) and Xin Zheng.

This repository is based on a national undergraduate scientific research and innovation project: simplified Chinese search engine for kids.

__Sorry this project is not available now, but will be available soon.(maybe in one year)__

# introduction
When we did kidsearch project, we were sophomores. As time going by, we realize that there are more we can do to make it more valuable. 
So we decide to create this github repository. This project aims to tidy up codes of kidsearch which were written by us from 2016 to 2017 and make part of them opened. 
We will try our best to make this project a unified system and provide as many APIs as we can.

We think the best explanation of APIs should be comments of codes, but there will also be some tutorials available soon. 
If you want to get some literal thoughts now, related work may help. 

The initial version of our project is based on Java(Lucene), Python(Crawler), PHP(frontend) and Socket(Communication). The most useful part we think is socket because we added multi-threading in it. 
Since Python is so popular at present, we also use PyLucene to replace Lucene and Django to replace PHP, which can simplify part of socket communications to build another Python version of our project.
Both of the two versions will be open-sourced.

Actually, our project is mainly for simplified Chinese search engine. The reason for using English in documents and comments is that we think this project may also helpful to some other languages.

# environment
This project is aimed to help do some lightweight search engine tasks. So the running environment is mainly on Windows.

# requirement
[Python3.x (x>=5)](https://www.python.org/downloads/release/python-351/), Django(maybe django-rest is also needed?), [PyLucene](http://lucene.apache.org/pylucene/), Apache, MySQL.

Some other python packages are also needed: requests, ...

# goal
Make a wonderful convenient Python package to do tasks about search engine. Here is an ideal example:
```python
import kidsearch as ks
webpages = ks.crawler(['http://www.61tom.com', 'http://www.61baobao.com/'], max_page=1000, max_depth=10)
indexes = ks.make_index(webpages)
results = indexes.search(key_words)
print(ks.show(results))
```

# related work
* [一种基于Python爬虫和Lucene检索的垂直搜索引擎的实现方法介绍 (blog)](http://www.cnblogs.com/itlqs/p/6797789.html)
* [儿童搜索引擎的现状与分析 (paper)](http://www.cqvip.com/QK/71889x/201703/epub1000000740663.html)
* [面向中文搜索引擎的网页结构化信息获取系统的设计与实现 (paper)](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFDLAST2017&filename=XXDL201623077&uid=WEEvREcwSlJHSldRa1FhdXNXYXFuemdtMThHRVFnUkIxM2VzUlpBWitJZz0=$9A4hF_YAuvQ5obgVAqNKPCYcEjKensW4ggI8Fm4gTkoUKaID8j8gFw!!&v=MDEwOTNJOUNZNFI4ZVgxTHV4WVM3RGgxVDNxVHJXTTFGckNVUkwyZVorZHFGeS9nVTcvS1BUWFBZckc0SDlmT3I=)
* [基于Lucene与Socket通信的中文搜索引擎的设计与实现 (paper)](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFDLAST2017&filename=WDZC201707036&uid=WEEvREcwSlJHSldRa1FhdXNXYXFuemdtMThHRVFnUkIxM2VzUlpBWitJZz0=$9A4hF_YAuvQ5obgVAqNKPCYcEjKensW4ggI8Fm4gTkoUKaID8j8gFw!!&v=MDU0MzExVDNxVHJXTTFGckNVUkwyZVorZHFGeS9nVTdyT01pblJiYkc0SDliTXFJOUdZb1I4ZVgxTHV4WVM3RGg=)
* [An Algorithm to Extract and Judge the Main Text Based on the Law of Total Probability (paper)](https://www.researchgate.net/publication/318391632_An_Algorithm_to_Extract_and_Judge_the_Main_Text_Based_on_the_Law_of_Total_Probability)
* [KidSE: A Search Engine Designed for Children which Supports Simplified Chinese (paper)](https://www.researchgate.net/publication/318390755_KidSE_A_Search_Engine_Designed_for_Children_which_Supports_Simplified_Chinese?ev=publicSearchHeader&_sg=aeB0tyixJT-V8czBLUB3qQWfRW1F2qUa2-l93CjHO6Eqaask2Jyy78awh83_nwXKzN3Hrt8_bNJQ0xA)
