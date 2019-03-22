# douban-movie
预览地址:https://rustincohle2016.github.io/douban-movie/index.html

# 技术
HTML+CSS使用
原生JS应用
应用jQuery
移动端调试
豆瓣免费api接口（数据获取）
# 功能实现
移动端原生页面
单页应用实现
底部tab实现（包括字体图标实现
底部Tab页面的切换


解决问题:
# 问题1
- 在打开githubpages展示时出现:Mixed Content: The page at ‘xxx’ was loaded over HTTPS, but requested an insecure resource ‘xxx’. This request has been blocked; the content must be served over HTTPS.
- 解决办法:在网页头部加入
```
	<meta http-equiv="Content-Security-Policy" content="upgrade-insecure-requests">

```
- 问题反思:可能是将JS脚本写入了HTML中,导致HTTP的请求被屏蔽掉了

#问题2
- callback&&callback()没能理解


- 解决办法:
callback&&callback()是JS的技巧,所要表达的意思是如果存在回调函数就执行！
这是利用了 JS &&符号的一个小技巧
&& 符号在前面为假时就不会执行后面的语句了
所以这个就相当于    
```
if(callback){

callback();

}
```

- 问题3 
跨域报错：
解决方法:使用跨域方法,如jsonp，在api的url地址上加上对应路由：&callback=abc 来测试,如果能接收到则说明支持jsonp解决（在请求的datatype进行请求）

# 学到知识

将挂载页面及对应页面各自封装成对象,将页面功能封装成函数,通过调用对象的值进行调用.此类思想在框架中广泛使用.