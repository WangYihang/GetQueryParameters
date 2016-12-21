#GetQueryParameters
---
项目介绍 : 
> [项目地址](https://coding.net/u/yihangwang/p/GetQueryParameters/git)

在批量检测注入点的时候 , 需要做的第一步就是从页面中提取出来所有的和查询相关的URL以及其对应的查询参数
这个脚本就是为了解决这个问题 , 输入一个页面的URL , 经过脚本分析后 , 会返回这个页面中所有同源的查询参数 , 可以配置过滤条件 , 比如过滤掉非同源的URL , 或者保留子域名URL


---
使用方法 : 
```
Usage : 
	python getQueryParameters.py [URL]
Example : 
	python getQueryParameters.py "http://www.jianshu.com/"
```

---
截图 : 

![图片.png](http://upload-images.jianshu.io/upload_images/2355077-0186f003b80b15db.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片.png](http://upload-images.jianshu.io/upload_images/2355077-6a4b7ee1257681b1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片.png](http://upload-images.jianshu.io/upload_images/2355077-8570d49bffe49656.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---
TODO :
1. 修复`../`和`./`的BUG
2. 增加灵活性 , 将函数进行更高层次的抽取和封装
3. 让用户可以配置过滤条件
4. 使用Pthon的命令行参数解析库  
~~5. 有的链接并不是存在于`herf`中 , 需要解决这个问题(发现有的畸形链接是`//`开头的 , 这种默认为http协议 , 而不是在当前域下的子文件夹)~~
