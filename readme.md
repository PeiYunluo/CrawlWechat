#scrapy startproject ***  \ \ \
##创建项目
#scrapy genspider [name] "域名"
##创建新的爬虫
#scrapy crawl qsbkspider
##运行爬虫
Spiders(爬虫):它负责处理所有Responses,从中分析提取数据，获取Item字段需要的数据，并将需要跟进的URL提交给引擎，再次进入Scheduler(调度器)
Engine(引擎)：负责Spider、ItemPipeline、Downloader、Scheduler中间的通讯，信号、数据传递等。
Scheduler(调度器)：它负责接受引擎发送过来的Request请求，并按照一定的方式进行整理排列，入队，当引擎需要时，交还给引擎。
Downloader(下载器)：负责下载Scrapy Engine(引擎)发送的所有Requests请求，并将其获取到的Responses交还给Scrapy Engine(引擎)，由引擎交给Spider来处理
ItemPipeline(管道):它负责处理Spider中获取到的Item，并进行进行后期处理（详细分析、过滤、存储等）的地方.
Downloader Middlewares（下载中间件）：你可以当作是一个可以自定义扩展下载功能的组件。
Spider Middlewares（Spider中间件）：你可以理解为是一个可以自定扩展和操作引擎和Spider中间
items.py:爬取下的数据模型
middlewares.py:存放各种中间件
pipelines.py:管道 用items存储进入磁盘
settings.py:爬虫的一些配置信息
scrapy.cfg:项目的配置文件
spiders:所有爬虫
#scrapy genspider -t crawl [name] "域名"

3、输入git命令：
git init
git add .
git commit -m 'first'
''
git remote add origin https://github.com/PeiYunluo/CrawlWechat.git

(ps:新建的仓库地址)
git push origin master
4、等待上传就好了。
5、在github上刷新一下就看到自己的本地项目了
