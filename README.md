# Blog
URL：

# 前言

  从很久之前就打算了自己搭一个博客，终于闲下来（开始学习）做一个来记录自己学习历程和心得的博客  
通过各种Google最后选择通过GitHub和Hexo来实现（省钱省事）

## Git和Github的绑定 
  这个环节全网教程很多，跟科学上网一样属于基础的东西，当然我之前也是经历很多曲折才搞定，那些什么SSH，add，pull，合并冲突等等都花了不少时间，虽然我现在也只能照着做（狗头）  
虽然这些事情很花时间，但当你最后解决某个问题后，带来的成就感和喜悦感不亚于拿五杀的快乐

## 安装node.js和Hexo
这个过程也比较耗时间，简单但是繁琐，因为之前在电脑里面搞过eclipse来跑java代码，所以node.js就直接跳过，按照教程把环境变量搞好就基本上没问题了  
### Hexo
首先新建一个仓库，命名为你的名字加github.io，如图
![image](https://github.com/anqi399/blog/blob/main/images/newrepository.png)  
然后开始安装Hexo，先找个盘新建文件夹命名为Blog，鼠标右键Git Bush Here，通过npm命令安装  
`npm install -g hexo-cli`  
完成后进行初始化  
`hexo init`  
然后静态部署  
`hexo g`  
最后就可以打开看看了  
`hexo s`  
![images](https://github.com/anqi399/blog/blob/main/images/hexo_s.jpg)  
根据提示，浏览器输入http://localhost:4000 然后就可以看到首页了，看完了记得Ctrl+C关闭  
接下来要将Hexo与你的github合起来，打开之前的Blog文件夹，里面有一个_config.yml 文件，用记事本打开，在末尾添加你的仓库地址，如下     
```
deploy:
  type: git  
  repository: https://github.com/anqi399/anqi399.github.io //你的仓库地址  
  branch: master
```
tips: 仓库地址在你的仓库页，点击Clone，然后就会显示HTTPS的地址  

然后再回到Blog文件下，打开GIt Bash，进行Git的插件部署  
`npm install hexo-deployer-git --save`  
再继续输入下面三条命令（搬砖），主要是清楚默认环境，然后给你初始化一个新的    
```
hexo clean   #清除缓存文件 db.json 和已生成的静态文件 public
hexo g       #生成网站静态文件到默认设置的 public 文件夹(hexo generate 的缩写)
hexo d       #自动生成网站静态文件，并部署到设定的仓库(hexo deploy 的缩写)
```
这个步骤完成后就可以打开你的浏览器，输入你的地址，例如我的：https://anqi399.github.io/，  注意这里和仓库地址有点不一样，不需要前面的地址了。  

到这一步，前期工程就已经完成了，后面剩下的就是域名和美化问题，如果你觉得github.io不够个性化（因为是github提供的网页），没有那种输入woshishuaige.com高端，那么就需要花点钱买个域名。

## 域名
## 花钱
  阿里云、腾讯云等等都可以，刚开始找个大平台比较简单放心，我选择的是[万网](https://wanwang.aliyun.com/ "万网链接")-阿里云  
大概流程就是，登陆注册（这里可以直接支付宝扫码登陆，然后实名就可以直接解决了），然后选择你自己喜欢的域名，后缀就看你个人爱好，一般.com和.cn比较贵，其他的便宜，我选择的.top首年才9块钱，试试水。
接着建一个个人信息模板，填填邮箱电话还有上传身份证之类的，搞完后等待认证通过就行，一般来说挺快的，我十几分钟就收到通过短信通知了。最后，付款就可以了。
