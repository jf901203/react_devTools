
## Chrome浏览器安装 React Developer Tools和Redux DevTools插件

1. npm install --save-dev redux-devtools-extension

	import {createStore,applyMiddleware} from 'redux'

	import thunk from 'redux-thunk'

	import {composeWithDevTools}  from 'redux-devtools-extension'

	// 通过reducers去创建store对象
	import {counter} from './reducers'
	
	const  store=createStore(
	  counter,
	  composeWithDevTools(applyMiddleware(thunk))
	   //应用上异步中间件 才支持action返回函数的写法 中间件是用来做扩展功能的
	  )
	
	console.log(store)

	export default store