# Query
仿jq框架，实现常用功能
## 实现功能
+ jq选择器$()
+ $(function(){})页面加载完成自动运行
+ $().eq()选择单个元素
+ on,off事件绑定和解绑
+ append添加元素
+ find寻找下级元素
+ parent寻找父级元素
+ parents寻找父级及以上元素
+ child寻找子级元素
+ index获取当前元素在父元素中索引
+ html修改或获取元素内容
+ css修改或获取元素内联样式
+ attr修改或获取元素内联属性
+ val修改或获取元素value
+ siblings获取当前元素兄弟元素

## 注意内容
+ 选择器获取的内容为自定义数组，但是通过eq获取到的是真正的dom节点，和jq的选择器有本质的不同
+ jq获取子级元素为children，但是该选择器获取子级元素为child
+ on,off目前没有实现事件委托，用法仅限于$().on('event', 'handler')
+ 提供切片方法，Function.prototype.before,Function.prototype.after，可以在方法执行前后无限制累加运行
+ 重写伪数组concat,forEach,from方法，返回NodeArray伪数组对象，选择器获取的元素伪数组可以直接使用