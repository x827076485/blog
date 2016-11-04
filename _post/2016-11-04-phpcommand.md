---
layout: default
title: php
---
<h2>{{page.title}}</h2>
<h1 ><font color="blue">php常用命令</font></h1>
<p>{{ page.date | date_to_string }}</p>
<p>1、  查看php的版本、配置<br/>
在命令行中输入php –v 即可查看当前php的版本。<br/>
Java代码   <br/>
1.	PHP 5.2.17(cli) (built: Feb  2 2011 11:19:21)  
2.	Copyright (c) 1997-2010 The PHP Group  
3.	Zend Engine v2.2.0, Copyright (c) 1998-2010 Zend Technologies  
4.	with Zend Optimizer v3.3.9, Copyright (c) 1998-2009, by Zend Technologies  
5.	with eAccelerator v0.9.6.1, Copyright (c) 2004-2010 eAccelerator, by eAccelerator  
 
其他的选项有： –m、-i。笔者在这里就不给出例子了。<br/>
-m 会显示当前php加载的有效模块。<br/>
-i 则输出无html格式的phpinfo。<br/>
使用 –ini 选项可以输出当前php加载ini配置文件的数量、路径信息。<br/></p>
<p>2、  在命令行中运行php程序
从命令行运行php非常简单。但有些注意事项需要各位了解下。诸如$_SESSION之类的服务器变量是无法在命令行中使用的，其他代码的运行则和web服务器中完全一样^_^。<br/>
Php代码   <br/>
1.	< ? php  <br/>
2.	echo “运行php命令行echo”; <br/> 
3.	?>  <br/>
把上面的代码另存为hello.php 。在命令行中敲入 php –f hello.php。<br/>显示结果如下：<br/>
<br/>运行php命令行echo<br/><br/>
 
在命令行中执行php文件的好处之一就是可以通过脚本实现一些计划任务的执行。而毋须通过web服务器^_^。
当然，我们也可以直接在php中调试代码：输入php –r 指令，会出现一个”>”符号。这表示已经进入到php的shell中，可以直接写代码，并执行。<br/>
Java代码   <br/>
1.	-bash-3.2$ php -r '  <br/>
2.	> for($i=0;$i<2;$i++){  <br/>
3.	> echo "Number: {$i}\n";  <br/>
4.	> }  <br/>
5.	> '  <br/>
6.	Number: 0  <br/>
7.	Number: 1  <br/>
 
还可以使用php –a 命令打开交互模式，输入一行代码，php会实时输出结果。</p>
<p>3、  检测php语法、高亮输出<br/>
不用执行代码，我们可以在命令行下检测php文件的语法错误。<br/>
Java代码   <br/>
1.	-bash-3.2$ php -l hello.php  <br/>
2.	No syntax errors detected in hello.php  <br/>
程序员经常会需要将php代码高亮原样输出，使用php –s 即可<br/>
Java代码   <br/>
1.	-bash-3.2$ php -s hello.php  <br/>
2.	< code><span style="color: #000000">  <br/>
3.	< span style="color: #0000BB">&lt ;?php<br />< /span><br/>  
4.	<  span style="color: #007700">echo & nbsp;< /span><br/>  
5.	< span style="color: #DD0000">'ddd'< /span><br/>  
6.	< span style="color: #007700">;<br />< /span><br/>
7.	< span style="  color: #0000BB">?&g t; < br />< /span>  
8.	< /span>  </p>
<p>4、查看php手册
从php5.1.2开始，程序员们可以在php命令行下查看手册了，输入php –rf function。会打印出该函数的语法简介
Java代码   
1.	-bash-3.2$ php --rf strip_tags  
2.	Function [ <internal:standard> function strip_tags ] {  
3.	   
4.	- Parameters [2] {  
5.	Parameter #0 [ <required> $str ]  
6.	Parameter #1 [ <optional> $allowable_tags ]  
7.	}  
8.	}  
 
如果要查看类使用 –rc；查看扩展使用 –re。<br/></p>
<p>5.在当前目录创建端口。S为大写 <br/>
php -S localhost:8081 localhost:8081 -t ./ <br/>
在xxxxx目录创建端口。S为大写 <br/>
php -S localhost:8081 localhost:8081 -t E:/xxxx/xxx <br/></p>
<p>{{ page.date | date_to_string }}</p>