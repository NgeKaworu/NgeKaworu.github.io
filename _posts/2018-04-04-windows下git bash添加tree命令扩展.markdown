---
layout: post
title: "windows下git bash添加tree命令扩展"
date: 2018-04-04 13:22:11 +0000
categories: 填坑
---

## 动机

>git bash是Windows下的命令行工具。  
>基于msys GNU环境，有git分布式版本控制工具，也主要用于git。  
>GNU环境，就是说如果你喜欢linux/unix的环境，就可以选择使用git bash。  
>里面有你熟悉的linux工具，tar，grep，awk等，且可以安装编译环境gcc，make等  


可是git-bash 居然  
**没有tree命令!!!**  
**没有tree命令!!!**  
**没有tree命令!!!**  
  
window cmd的tree又没有忽略文件夹功能
  
找遍了百度和github只找到一个treer [仓库地址] 可这个代替品不支持**忽略多个文件夹,作者也不更新了**.  

这时我想起了**伯符**临走之前的那句话
>倘内事不决,可问[百度]. 外事不决,可问[谷歌]

emmmm...google it  
  
然后...  
  
搜索结果的第一条就是[解决方案] (看来微软在国外的占有率也不低啊,~~索尼天下第一~~)
  
---
  
## 正文

废话不多说,有能力的可以自己点上面的链接去看看.

首先我们要去下一个Tree for Windows  
[点我下载]  
  
[这是官网]  
md5sum: 9404560896d6b6533a13ded51516a9ec  
下好后解压出来,找到``bin\tree.exe``文件  
然后放在``你的git文件目录下\usr\bin``下  
例如我的是``C:\Program Files\Git\usr\bin``  

然后打开git bash 输入tree --help  

### 常用参数  
```linux
-a 显示所有文件和目录。
-A 使用ASNI绘图字符显示树状图而非以ASCII字符组合。
-C 在文件和目录清单加上色彩，便于区分各种类型。
-d 显示目录名称而非内容。
-D 列出文件或目录的更改时间。
-f 在每个文件或目录之前，显示完整的相对路径名称。
-F 在执行文件，目录，Socket，符号连接，管道名称名称，各自加上"*","/","=","@","|"号。
-g 列出文件或目录的所属群组名称，没有对应的名称时，则显示群组识别码。
-i 不以阶梯状列出文件或目录名称。
-I 不显示符合范本样式的文件或目录名称。
-l 如遇到性质为符号连接的目录，直接列出该连接所指向的原始目录。
-n 不在文件和目录清单加上色彩。
-N 直接列出文件和目录名称，包括控制字符。
-p 列出权限标示。
-P 只显示符合范本样式的文件或目录名称。
-q 用"?"号取代控制字符，列出文件和目录名称。
-s 列出文件或目录大小。
-t 用文件和目录的更改时间排序。
-u 列出文件或目录的拥有者名称，没有对应的名称时，则显示用户识别码。
-x 将范围局限在现行的文件系统中，若指定目录下的某些子目录，其存放于另一个文件系统上，则将该子目录予以排除在寻找范围外。
```
  
[百度]:https://www.baidu.com
[谷歌]:http://google.com
[仓库地址]:https://github.com/derycktse/treer
[解决方案]: https://superuser.com/a/1141489/890933
[点我下载]:http://downloads.sourceforge.net/gnuwin32/tree-1.5.2.2-bin.zip
[这是官网]:http://gnuwin32.sourceforge.net/packages/tree.htm
