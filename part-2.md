



## 改进项目(待完善)

* 增加发布表单项目

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
<select>  <br>

标题：<input type="text" size="50"><br>

内容：<textarea cols="50" rows="10"></textarea><br>

联系人：<input type="text" size="10">
联系电话：<input type="text" size="15"><br>
	<input type="submit" value="发布">
</div>
* 增加用户个人页面，显示这个用户发布的信息
* 增加搜索功能，在列表页能够搜索(城市和分类选择仍然需要可用)
* 增加信息管理后台
	* 能够删除信息(假删)
	* 由于发布的信息不一定没有非法内容，所以为信息增加一个状态：是否审核
* 为信息增加刷新功能(让信息发布时间变成现在)，后台要能查到用户的刷新记录
* 增加用户积分功能，积分通过发帖得到，每次发帖获得5积分，每次刷新获得5积分
* 为信息增加编辑功能
* 将用户信息缓存起来(`memcache`), 不必每次都去查数据库
* 将用户发布的信息缓存起来(`memcache`), 不必每次都去查数据库
	
* PHP 实践
	* [PHP之道](http://wulijun.github.io/php-the-right-way/)
	* [PHP最佳实践](http://youngsterxyf.github.io/2013/06/01/php-best-practices/)
* 安全
	* 输入输出过滤
	* SQL注入
* Javascript 相关
	* 验证输入 	
* 版本管理软件
* 统计

## 继续改进(待完善)
* 调用js插件
* 使用memcached缓存
* SQL优化



--- 
## 推荐书籍
PHP入门

1. Programming PHP 3th
2. Web开发入门经典:使用PHP6、Apache和MySQL
3. PHP与MySQL动态网站开发(第4版)

提高

1. 深入PHP(面向对象模式与实践第3版)
2. PHP+MySQL专家编程

---
## 推荐网站
PHP

* [PHP之道](http://wulijun.github.io/php-the-right-way/)
* [PHP最佳实践](http://youngsterxyf.github.io/2013/06/01/php-best-practices/)
* [Laruence](http://www.laruence.com/)

CSS


JS

* [jqfundamentals](http://jqfundamentals.com/)
* <http://learn.jquery.com/>
