* ES
	* ECMAScript
	* js语言的规范
	* 用的js是它的实现
	* js的组成
		* ECMAScript(js基础)
		* 浏览器端扩展
			* BOM
			* DOM
		* 服务器端扩展
			* Node.js
* ES5
	* 严格模式
		1. 理解:
			除了正常(混杂)运行模式，ECMAscript 5添加了第二种运行模式："严格模式"（strict mode）。
		    顾名思义，这种模式使得Javascript在更严格的条件下运行
		2. 目的/作用
			- 消除Javascript语法的一些不合理、不严谨之处，减少一些怪异行为;
			- 消除代码运行的一些不安全之处，保证代码运行的安全；
			- 提高编译器效率，增加运行速度；
			- 为未来新版本的Javascript做好铺垫。
		3. 使用
		    在全局或函数的第一条语句定义为: 'use strict';
		    如果浏览器不支持, 只解析为一条简单的语句, 没有任何副作用
		4. 限制语法
		    1. 声明定义变量必须用var
		    2. 创建eval作用域
		    3. 禁止函数中的this关键字指向全局对象
	* JSON对象
		1. 用于在json对象/数组与js对象/数组相互转换的工具对象
		2. JSON.stringify(obj/arr)
		    js对象(数组)转换为json对象(数组)
		3. JSON.parse(json)
		    json对象(数组)转换为js对象(数组)
	* Object扩展
		1. Object.create(prototype[, descriptors]) : 创建一个新的对象
		    1). 以指定对象为原型创建新的对象
		    2). 创建一个以null为对象原型，并添加一些属性描述
		2. Object.defineProperties(object, descriptors) : 为指定对象定义多个属性
			1). get/set属性
	* Array扩展
		1. Array.prototype.indexOf(value) : 得到值在数组中的第一个下标
		2. Array.prototype.lastIndexOf(value) : 得到值在数组中的最后一个下标
		3. Array.prototype.forEach(function(item, index){}) : 遍历数组
		4. Array.prototype.map(function(item, index){}) : 遍历数组返回一个新的数组
		5. Array.prototype.filter(function(item, index){}) : 遍历过滤出一个子数组
	* Function扩展
		Function.prototype.bind(obj) :
	    	将函数内的this绑定为obj, 并将函数返回
		区别
	    	fn.bind(obj) : 指定函数中的this, 并返回函数
	    	fn.call(obj) : 指定函数中的this,并调用函数
	* Date扩展
		* Date.now() : 得到当前时间值
* ES6
	* 2个新的关键字
		* let/const
		* 块作用域
		* 没有变量提升
		* 不能重复定义
		* 值不可变
	* 变量的解构赋值
		* 将多个数据一次赋值给多个变量
		* 数据源: 数组/对象
		* 目标: [a, b]/{a, b}
	* 各种数据类型的扩展
		* 数值
			 1. 二进制与八进制数值表示法: 二进制用0b, 八进制用0o
	         2. Number.isFinite(i) : 判断是否是有限大的数
	         3. Number.isNaN(i) : 判断是否是NaN
	         4. Number.isInteger(i) : 判断是否是整数
	         5. Number.parseInt(str) : 将字符串转换为对应的数值
	         6. Math.trunc(i) : 直接去除小数部分
		* 字符串
			 1. contains(str) : 判断是否包含指定的字符串
	         2. startsWith(str) : 判断是否以指定字符串开头
	         3. endsWith(str) : 判断是否以指定字符串结尾
	         4. repeat(count) : 重复指定次数
	         5. 模板字符串 : 简化字符串的拼接
	             1). 模板字符串必须用``饮食
	             2). 变化的部分使用${xxx}定义
		* 对象
			 1. Object.is(v1, v2) : 判断2个数据是否完全相等
	         2. Object.assign(target, source1, source2..) : 将源对象的属性复制到目标对象上
	         3. __proto__属性 : 隐式原型属性
	         4. 增强的对象写法
		* 数组
			 1. Array.from(v) : 将伪数组对象或可遍历对象转换为真数组
	         2. Array.of(v1, v2, v3) : 将一系列值转换成数组
	         3. find(function(value, index, arr){return true}) : 找出第一个满足条件返回true的元素
	         4. findIndex(function(value, index, arr){return true}) : 找出第一个满足条件返回true的元素下标
	         5. keys() : 返回包含所有下标的可迭代对象
	         6. values() : 返回包含所有值的可迭代对象
	         7. entries() : 返回包含所有下标和值的可迭代对象
		* 函数
			 1. 箭头函数
	         2. 形参的默认值
	         3. 可变参数
     * set/Map容器结构
		* 容器: 能保存多个数据的对象, 同时必须具备操作内部数据的方法
		* 任意对象都可以作为容器使用, 但有的对象不太适合作为容器使用(如函数)
		* Set的特点: 保存多个value, value是不重复 ====>数组元素去重
		* Map的特点: 保存多个key--value, key是不重复, value是可以重复的
		* API
			* Set()/Set(arr) //arr是一维数组
			* add(value)
			* delete(value)
			* clear();
			* has(value)
			* size
			* 
			* Map()/Map(arr) //arr是二维数组
			* set(key, value)
			* delete(key)
			* clear()
			* has(key)
			* size
	* for--of循环
		* 可以遍历任何容器
		* 数组
		* 对象
		* 伪/类对象
		* 字符串
		* 可迭代的对象
* 静态(工具)方法
	* Fun.xxx = function(){}
* 实例方法
	* 所有实例对象 : Fun.prototype.xxx = function(){} //xxx针对Fun的所有实例对象
	* 某个实例对象 : fun.xxx = function(){} //xxx只是针对fun对象