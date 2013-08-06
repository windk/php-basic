# PHP 训练项目 - 渐进式练习

## 可选地区的信息发布系统 - 

功能：

1. 用户填写 帐号，密码，可以注册  
	<div style="border:1px solid grey;padding:5px;display:inline-block;">
	帐号：<input type="text">  
	密码：<input type="text">  
	重复密码：<input type="text">  
	<input type="submit" value="提交">  
	<div>	
2. 注册以后，可以登录网站，在网站发布信息  
	<div style="border:1px solid grey;padding:5px;display:inline-block;">
	帐号：<input type="text">  
	密码：<input type="text">  
	<input type="submit" value="登录">
	</div>  	
3. 发布信息时可以选择信息的类别，和城市，同时需要填写标题和内容
	<div style="border:1px solid grey;padding:5px;display:inline-block;">
	城市：<select>
	<option>北京</option>
	<option>上海</option>
	<option>广州</option>
	<option>深圳</option>		
	<select>
	类别：<select>
	<option>二手</option>
	<option>房产</option>
	<option>宠物</option>
	<option>招聘</option>		
	<select>
	
	标题：<input type="text" size="50">

	内容：<textarea cols="50" rows="10"></textarea>
		<input type="submit" value="发布">
	</div>
4. 在某个城市的页面，可以 是现实信息的分类和信息的标题列表，根据发布时间倒序排列，比如：北京 `list.php?city=1`

	<div style="border:1px solid grey;padding:5px;display:inline-block;">
		<ul>
			<li>[<a href="#">北京</a>] － [<a href="#">二手</a>] － <a href="#">闲置电脑桌，300自取</a> 2013-07-27</li>
			<li>[<a href="#">北京</a>] － [<a href="#">二手</a>] － <a href="#">美利达自行车，公爵100，500拿走</a> 2013-07-26</li>
			<li>[<a href="#">北京</a>] － [<a href="#">二手</a>] － <a href="#">旧电脑回收，联系电话:0898-98837828</a> 2013-07-25</li>
			<li>[<a href="#">北京</a>] － [<a href="#">房产</a>] － <a href="#">房屋出租，海甸岛1居室</a> 2013-07-24</li>			<li>[<a href="#">北京</a>] － [<a href="#">宠物</a>] － <a href="#">小猪，长不大的小猪</a> 2013-07-24</li>
		</ul>		
	</div>
5. 在某个信息分类页面， 可以显示城市 和 信息标题列表，根据发布时间倒序排列，比如，二手分类 `list.php?category=2`
	<div style="border:1px solid grey;padding:5px;display:inline-block;">
		<ul>
			<li>[<a href="#">北京</a>] － [<a href="#">二手</a>] － <a href="#">闲置电脑桌，300自取</a> 2013-07-27</li>
			<li>[<a href="#">上海</a>] － [<a href="#">二手</a>] － <a href="#">美利达自行车，公爵100，500拿走</a> 2013-07-26</li>
			<li>[<a href="#">深圳</a>] － [<a href="#">二手</a>] － <a href="#">旧电脑回收，联系电话:0898-98837828</a> 2013-07-25</li>
			<li>[<a href="#">广州</a>] － [<a href="#">二手</a>] － <a href="#">求购一个旧茶几</a> 2013-07-24</li>			<li>[<a href="#">北京</a>] － [<a href="#">二手</a>] － <a href="#">二手车，奥托弟弟傲来</a> 2013-07-24</li>
		</ul>		
	</div>
6. 点击标题能够进入具体信息内容页面 `post.php?id=323`
	
	<div style="border:1px solid grey;padding:5px;display:inline-block;">
		<table>
		<tr><th>城市：</th><td>北京</td></tr>
		<tr><th>分类：</th><td>二手</td></tr>	
		<tr><th>标题: </th><td>闲置电脑桌，300自取</td></tr>
		<tr><th>内容：</th><td>琼海椰思宝床垫厂，成立于1992年（即原江广家具厂），是琼海老牌床垫厂之一，现有日本进口围边机，自动串网机等设备，并高薪聘请来广东床垫技师主操床垫加工工作。主要生产家居系列床垫，酒店宾馆系列床垫，及特色床垫系列：“圆型床垫”等，并可为客户定制床头软包，承领酒店案例有：琼海泰和大酒店、琼海龙湾大酒店、琼海茉莉花开酒店、琼海利群宾馆、琼海金源宾馆、琼海登格莱宾馆，琼海国泰宾馆，琼海海丰宾馆，琼海白云山宾馆，琼海金星宾馆，琼海海马家私城等床垫定制及床头软包定制工程。本厂承诺，本厂生产的床垫内胆保用20年。 </td></tr>
		<tr><th>评论：</th><td>[2013-07-20 23:22:23] - [<a href="#">海蓝之星</a>] - 这东西还行</td></tr>
		<tr><th>留言：</th><td><textarea cols="50" rows="10"></textarea><input type="submit" value="提交"></td></tr>		
		</table>	
	</div>
7. 在内容页面，注册用户可以留言， 留言按照留言时间，最近发布的在最上面

考察点：

* PHP 运行方式
	* 基于apache的module
	* 或者nginx和php-fpm
	* 使用web浏览器打开
* 和HTML之间的关系
	* 逻辑与显示
* 页面传值
	* POST
	* GET
* Cookie
	* 如何实现的
* Session
* 和数据库交互

提示：

* 数据库建立时应该选择UTF8字符集
* 城市和分类应该是一个以id为主键的表

附录：
URL:
* 首页:index.php
* 列表页:list.php

城市列表：  
1 － 北京  
2 － 上海  
3 － 广州   
4 － 深圳   
5 － 杭州   
6 － 成都   
7 － 天津   
8 － 南京  

分类列表：  
1 － 二手  
2 － 房产  
3 － 宠物  
4 － 招聘  

可能用到的函数: 

* 数据库链接
 mysql_connect
* [字符串函数](http://www.php.net/manual/en/book.strings.php)
* [数组函数](http://www.php.net/manual/en/book.array.php)
