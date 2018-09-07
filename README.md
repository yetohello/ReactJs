# 生命周期函数：
### 指某一时刻组件会走动调用自动执行的函数
---
例：

```javascript
//在组件即将被挂载到页面的时刻自动执行
componentWillMount (){
	console.log('componentWillMount')
};
```
```javascript
// 在组件被挂载到页面的时刻自动执行
componentDidMount (){
	console.log('componentDidMount')
}
```
```javascript
// 在组件更新之前的时刻自动执行
shouldComponentUpdate (){
	console.log('shouldComponentUpdate')；
	return true;  
	//return false; 阻止组件跟新
}
```
# 生命周期函数的四大阶段
----
### 1.Initialization : 初始化
    * setup props and state 初始化数据
### 2.Mounting : 挂载
    * componentWillMount 挂载前
    * render
    * componentDidMount  挂载后
### 3.Updation : 组件更新
    * props ：
	    * componentWillReceiveProps : 当一个组件从父组件接受参数，只要父组件的render函数重新被执行了，子组件的这个函数就会被执行

	    * shouldComponentUpdate : 组件更新之前 返回布尔值

	    * componerntWillUpdate :  组件更新之前，在shouldComponentUpdate()之后，true执行，false不执行
	    * render :
	    * componentDidUpdate : 组件更新完成之后
    * state :
	    * shouldComponentUpdate : 组件更新之前 返回布尔值
	    * componerntWillUpdate :  组件更新之前，在shouldComponentUpdate()之后，true执行，false不执行
	    * render :
	    * componentDidUpdate : 组件更新完成之后
		
### 4.Unmounting : 去除
    * componentWillUnmount : 当组件即将被从页面中去除的时候执行
