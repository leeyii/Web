# CSS

##目录

* CSS语法
* 选择器 
	- id选择器
	- class选择器


##CSS语法

选择器：通常是需要改变样式的HTML元素  
每条声明由一个属性和一个值组成， 每条声明之间由分号分隔。

	h1/*这是属性*/ {
	    color:red;			/*这是一条声明*/
	    text-align:center 	/*属性：值*/[]()
	}        
为了增强CSS的可读性，每条声明可以换行

CSS注释

	/* 这是注释 */

## CSS选择器

###id选择器

id选择器：  
id选择器可以为特定id的HTML标签指定特定的样式  
id选择器以`#`开头  
id选择器属性不要以数字开头，在某些浏览器中不兼容

	#para1
	{
	    color:red;
	    text-align:center
	}

###class选择器

class用于描述一组元素的样式，class选择器可以在多个元素中使用