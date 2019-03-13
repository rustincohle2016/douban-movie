# douban-movie
预览地址:https://rustincohle2016.github.io/douban-movie/index.html




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

