## 面向对象

使用`hasOwnProperty`判断对象属性是否存在

> obj.hasOwnProperty(name)

如果你需要通过变量来访问对象的属性值，请用中括号操作符，点操作符不支持变量。

如:

```javascript
function update(id, prop, value) {
	if(prop!="tracks" && value!==""){
		collection[id][prop]=value;//此处当变量使用时, 需要用中括号,而不能是用点
	}else if(prop=="tracks" && value !==""){
		collection[id][prop].push(value);
	}else if(value===""){
		delete collection[id][prop];
	}
  console.log(collection[id][prop]) ;
}
```

