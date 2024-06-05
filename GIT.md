#### GIT

* git:管理软件开发项目中的源代码文件

* scm：Software Configuration Management软件配置管理

​	软件配置管理(SCM)是指通过执行版本控制、变更控制的规程，以及使用合适的配置管理	软件来保证所有配置项的完整性和可跟踪性。配置管理是对工作成果的一种有效保护，

* VSS：Visual Source Safe

  美国微软公司出品的版本控制系统，简称VSS（并不适合多人协作的工作场景，且收费）

* CVS：Concurrent Versions Sysytem（升级版本：**S**ub**v**ersio**n**）

  老牌的额版本控制系统，它是基于客户端/服务器的行为使得其可容纳多用户，构成网络也很方便，简称为CVS

#### 1.概念

##### 1.1 版本控制

###### 1.1.1 版本分两大类：

 - 软件版本![image-20240529163823596](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240529163823596.png)
 - 文件版本![image-20240529163902274](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240529163902274.png)

1.1.2 版本控制软件的基础功能

* 保存和管理文件
* 提供客户端工具进行访问
* 提供不同版本文件的比对功能

##### 1.2 集中式版本控制

![image-20240529170757913](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240529170757913.png)

##### 1.3 分布式版本控制

分布式版本控制优于集中式版本控制的点就在于：中央服务器宕机或是网络故障，依然可以在本地进行开发不影响进程（但依赖网络，如果网络慢则同步非常慢，且占用本地资源）

![image-20240529172453776](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240529172453776.png)

##### 1.4 多人协作开发

规定行由规定人员开发

#### 2  GitHub Desktop

本地开发时展示的用户信息：

![image-20240530104128929](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530104128929.png)

文件操作状态：比如新增、修改则会在下图区域显示

![image-20240530111130006](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530111130006.png)

将本地文件提交到仓库当中：

![image-20240530111959019](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530111959019.png)

移除仓库时不勾选:
Also move this repository to Recycle Bin则只会在软件中删除该仓库，本地文件还会保留，这时将本地仓库拖拽到软件中，又会在软件中存在

![image-20240530150847362](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530150847362.png)

##### 2.1 文件操作

在本地修改后还需要在软件进行提交操作：

![image-20240530161503112](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530161503112.png)

如果修改了文件提交后，则不会在git覆盖源文件，而是写入新的修改后文件（不同版本号）：

![image-20240530164701501](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530164701501.png)

![image-20240530170326704](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530170326704.png)

![image-20240530170457932](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530170457932.png)

文件删除（仍需要提交）：

![image-20240530170928546](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530170928546.png)

##### 2.2 分支原理

###### 2.2.1 概念

版本越多，占用仓库资源，且提交频繁、杂乱，容易造成为止风险

![image-20240530174432226](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530174432226.png)

解决办法（分别在仓库副本操作，最后再合并）：![image-20240530174700333](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530174700333.png)

![image-20240530175219792](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240530175219792.png)

![image-20240531111617394](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531111617394.png)

###### 2.2.2 分支创建

![image-20240531111429748](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531111429748.png)

选择不同分支会展示不同分支下的文件内容。main分支合并：![image-20240531113307077](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531113307077.png)

分支合并后：

![image-20240531113513523](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531113513523.png)

尝试制造冲突文件：

![image-20240531114213468](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531114213468.png)

需要手动干预解决冲突之后才能顺利合并

###### 2.2.3 合并标签

合并没有描述标签，可以右键历史记录手动Create Tag：

![image-20240531114546440](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531114546440.png)

实现效果：![image-20240531114654258](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531114654258.png)

###### 2.2.4  网站效果

![image-20240531153353127](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531153353127.png)![image-20240531153353127](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531153353127.png)

版本号：

![image-20240531153433460](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531153433460.png)

![image-20240531153641135](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531153641135.png)

![image-20240531153753452](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531153753452.png)

删除仓库在setting的最底部：

![image-20240531153948321](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531153948321.png)

下载线上仓库的内容：![image-20240531160850494](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531160850494.png)

本地仓库推送到远程仓库：

![image-20240531161055757](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531161055757.png)

###### 2.2.5 Gitee

和Github一样但是Gitee是中文版的

###### 2.2.6 README

README是对仓库资源的重要的描述信息

* 注意：github不是无法托管dox等等文档，而是没有提供这类数据的比对功能。主要为代码托管平台

* Ignore：在上传时可以选择ignore所有的备份文件或选中文件![image-20240531163932741](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531163932741.png)

###### 2.2.7 小图标细节

红色图标：删除

黄色图标：修改

绿色图标：新增

![image-20240531164314899](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531164314899.png)

![image-20240531164517477](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240531164517477.png)

###### 2.2.8 版本号

每一个系统库都有属于自己的版本号

SHA-1:40位

定位仓库的文件位置：2位（文件夹）+38位（文件名）

使用git自带工具才能看到文件名里面对应的正确内容：（Cat-file表示查看文件，-p表示友好查看）

![image-20240603154929471](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603154929471.png)

tree后跟的是当前版本号

parent是上一次提交的版本号![image-20240603155628250](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603155628250.png)

![image-20240603160008346](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603160008346.png)

100表示的是普通文件，644表示的是文件的权限，blog表现的是当前的文件块对象![image-20240603160020885](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603160020885.png)

* 为何版本号和github对不上？

解答：关联关系：

![image-20240603170610666](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603170610666.png)

版本号与分支的关系、也是能够区分最新版本的途径

![image-20240603172915104](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603172915104.png)

![image-20240603173605037](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603173605037.png)

###### 2.2.9 命令

git的指令了解![image-20240603173932326](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240603173932326.png)

* 仓库指令

**git -v** 查看安装版本

**git init** 创建仓库（首先建立一个文件夹，文件夹名字就是库名，然后在这个文件夹下执行该命令。以这种方法创建的会比git工具创建的少了一个.gitattributes文件。而且工具会自动执行一次初始化提交，会首先指向master主分支）

**git clone +http地址** 克隆仓库

![image-20240604150237057](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240604150237057.png)

![image-20240604150253028](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240604150253028.png)

**git clone +http地址 仓库名** 克隆仓库但改名

* 配置指令

**git config user.name 用户名**

**git config user.email 邮件**

以上是针对当前仓库的配置，如果需要对所有仓库进行配置：

**git config --global user.name 用户名**

**git config --globaluser.email 邮件**

**git status** 暂存区的状态

![image-20240604151147669](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240604151147669.png)

**git add 文件名** 把该文件放入暂存区作比对操作（还可以用通配符如git add *.txt）

**git rm --cached** 文件名 把该文件从暂存区放入工作区（只是逻辑上放，并不是真正的移过去）

**git commit -m 新增文件** -m表示的是提交信息的参数

**git log** 相当于github里面查看History

**git restore 文件名** 误删恢复（从存储区恢复到暂存区）

**git revert 版本号** 恢复到之前某版本

* 分支操作

**git branch user** 增加分支（基于提交）

**git branch -v** 查看所有分支、查看当前分支

**git checkout user** 切换分支

**git checkout -b order** 创建分支并切换到新创建的分支

**git branch -d 分支名** 删除分支

* 分支冲突

**git merge 次分支名** 分支合并（需要先切换到主分支）

解除了冲突后提交冲突文件，则会提示合并成功，无需再次进行合并操作

* 标签操作

提交版本号过长、且不清晰具体是什么操作

**git tag uptfile 版本号**

也就是给版本增加别名，创建分支也通用

* 远程仓库

**git remote add origin 远程仓库地址** 本地仓库关联远程地址

使用ssh是需要提供安全证书的

**ssh-keygen -t rsa -C 远程仓库ssh地址** 做安全认证、生成安全认证文件

然后去到网站添加刚刚生成的公钥（在c盘的用户下.ssh的文件）

##### 3 gitlab集成（极狐）

![image-20240604164109295](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20240604164109295.png)

极狐是安装在linux操作系统上的

