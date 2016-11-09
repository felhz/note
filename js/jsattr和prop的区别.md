###1.浏览器的读写操作,只会关注property属性.

###2.当我们通过代码控制attributes属性来同步property属性时
	并不是每个属性都会同步.(由于布尔值转化的问题)
	属性值为布尔值的属性,attriute和proterty会实时同步????
				1.没有人为的干扰proterty时,会同步
				2.干扰了proterty后,就不会同步
	属性值不为布尔值的属性attriute和proterty会实时同步
		
###3.那些我们可以通过浏览器端通过实际操作来改变的属性最好使用prop()

###4.  nodeType，nodeName，nodeValue是任何节点都共有的属性
	id，name，value  是具体节点的属性

	   元素节点：
	         nodeType:1
	         nodeName:标签名
	         nodeValue:null
	   属性节点：
	         nodeType:2
	         nodeName:属性名
	         nodeValue:属性值
	   文本节点：
	         nodeType:3
	         nodeName:#text
	         nodeValue:文本值
	         
	    //  nodeType、nodeName 是只读的.
		//  而 nodeValue 是可以被改变的。 
		//  以上三个属性, 只有在文本节点中使用 nodeValue 读写文本值时使用最多. 
		

