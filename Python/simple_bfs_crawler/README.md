## 一个简易的Python爬虫系统
### pool.txt中写入的是初始链接池
### 抓取策略：宽度优先搜索
### 有四种抓取模式：
#### 1.全站抓取+最多网页个数限制；
#### 2.全站抓取+最大深度限制；
#### 3.全网抓取+最多网页个数限制；
#### 4.全网抓取+最大深度限制
### 运行crawler.py文件开始爬取
### 抓取过的网页就不会再重复抓取了，会保存原来的目录结构
### 运行Extract_Index.py可以得到抓取的网页的本地目录（经过一定的字符串替换可以得到原始的URL链接）

<br>

## 环境要求
### Python3.5.1, requests, bs4


## TODO list
### 当前的全站抓取策略是：一个网页只能链接出跟它相同域名的页面（相对目录也可以）。
### 待添加功能：全站抓取的策略是限定域名池，只有在这些域名池里的域名才会被链接到。