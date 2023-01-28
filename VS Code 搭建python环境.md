
#### 为什么

 为什么需要配置环境，配置环境意味着什么，配置环境是为了能够运行python项目，那么配置环境，就意味着要把python运行所需的条件，都创造好。


#### 是什么

 python运行需要的条件是什么呢？python是解释型的语言，需要知道python解释器就可以了。如果自己在电脑上运行pyhon程序的话，就是打开cmd，输入命令执行，输入命令又分为两种情况，直接输入类似
 ```
 python xxx.py
 ```
 这个时候会出现两种情况，一种是：直接报错，不知道python命令是什么；一种是：执行成功。为什么会是这两种情况呢，那就要看cmd执行命令的时候，是怎么做的，对于cmd来讲，能识别的命令是windows自带的，一部分是用户自己配置的，用户以环境变量的方式来配置。这里的python就属于用户自定义的，如果要能使cmd能够执行python命令，那么就需要配置环境变量，配置好环境变量之后，cmd就可以支持python命令了。上面运用python出现的两种不同情况的区别就在于是不是配置了环境变量。
 
 同理对于VS Code来说，要想让VS Code能够运行python项目，那么就是要告诉它，python解释器在哪里。

 #### 怎么做

怎么做，具体来说就是如何给VS Code做配置，告诉VS Code python的解释器在哪里，最终抽象成为，加一个配置。VS Code加配置一般都是在命令面板里面，如果不知道的话，也可以直接搜索，配置好，就OK。具体配置在这里：

![1](https://github.com/hyqing/athena/raw/master/image/create%20env.png)

***难点：***

如果pyhon有依赖包怎么办，也就是说python如何找到依赖的包，python解释器会按照确定的目录去找，如果能找到就继续执行，找不到就报错，找不到包

1. 程序的根目录（即当前运行python文件的目录）
2. PYTHONPATH环境变量设置的目录
3. 标准库的目录
4. 任何能够找到的.pth文件的内容
5. 第三方扩展的site-package目录

在VS Code里面，采用的是第一种，用venv来做，这里有个最佳实践：

1.先创建一个venv，这里需要先打开，创建环境，然后再选择环境的依赖

第一步：
![](https://github.com/hyqing/athena/raw/master/image/create%20env.png)

第二步：
![](https://github.com/hyqing/athena/raw/master/image/select%20env%20base.png)


2.再选择python解释器为刚刚创建的环境

![](https://github.com/hyqing/athena/raw/master/image/select%20interperter1.png)  