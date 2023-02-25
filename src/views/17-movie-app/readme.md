## 问题1：搜索请求发出去之后没法获取更新数据

不能把函数作为依赖，否则会无限执行。如果是在useEffect作用域以外的函数作为了依赖，那么每次渲染页面都会重新创建函数，依赖改变再次触发副作用。

除非把函数定义在effect内部。

##  问题2：hover时没法让overview浮现

必须是在父元素上添加hover事件。

## 问题3：不知道如何让窗口刷新

直接window.location.reload()就行，如果怕看不到效果，可以通过输出语句和setTimeout()来判断。