# JavaScript 数据类型

JavaScript中有7种数据类型，字符串（String）、数字（Number）、布尔（Boolean）、数组（Array）、对象（Object）、空（Null）、未定义（Undefined）。

## JavaScript动态类型

JavaScript拥有动态数据类型。这意味着相同的变量可以用作不同的类型。

JavaScript在声明的时候不需要指定对象的类型，在给变量赋值的时候才决定变量是什么对象。

	var x; // x 为undefined
	var x = 4; // x 现在为数字类型
	var x = "x"; // x 现在为字符串

## JavaScript字符串

字符串是储存字符的变量。

#### 字符串语法

	// 声明字符串
	var str = "Hello, world!"  // 使用双引号 声明一个字符串
	var str = 'xxx'	// 使用单引号 声明一个字符串

使用双引号和单引号都能声明字符串，区别在于单引号包裹的字符串可以使用双引号，反正同理。  

	var answer="It's alright";
	var answer="He is called 'Johnny'";
	var answer='He is called "Johnny"';

如果想要在双引号包裹的范围内使用双引号，可以使用转义字符。

	var answer="He is called \"Johnny\"";

#### 使用索引访问字符串中的每个字符

	var str = "string"
	str[0] // s
	str[1] // t
	str[10] // undefined

索引是从0开始，如果索引值超过字符串的长度-1，则是undefined。

#### 字符串长度

可以使用字符串中的内置属性`length`来计算字符串的长度。

	var str = "asdfghjkl"
	str.length // 9

#### 转义字符

代码		    | 输出
------------- | -------------
\'  			| 单引号
\”  			| 双引号
\\			    | 反斜杠
\n  			| 换行
\r  			| 回车
\t  			| 制表符
\b  			| 退格符
\f  			| 换页符

#### 字符串也可以是对象

我们也可以通过`new`创建一个字符串对象

	var x = "str"
	var y = new String("str")
	typeof x 	// String
	typeof y 	// Object
	x == y 		// true
	x === y 	// false 

1. 对于string和number等基础类型 `==`和`===`是有区别的。  

	* 不同类型之前比较，使用`==`先把不同类型转化为同一类型的值后，然后对值进行比较，看值是否相等，`===`如果类型	不同结果就不同，类型相同才会继续进行比较。 
	* 同类型之间的比较，直接对值进行比较
2. 对于Array和Object来说没有区别，是直接比较对象的指针的。

> [String对象的属性和方法](http://www.w3school.com.cn/jsref/jsref_obj_string.asp)

## JavaScript数字

JavaScript只有一种数字类型，数字可以带小数点，也可以不带。

	var x = 20;
	var y = 20.00;
	// 科学计数法
	var a = 123e5 // 12300000
	var b = 123e-5 // 0.00123

数字类型还有想对于的对象的表现形式Number，只有再说。

## JavaScript布尔
布尔（逻辑）只有两个值，true和false。

	var x = true;
	var y = false;

## JavaScript数组
#### 数组3种创建形式

	// 1.
	var cars = new Array()
	cars[0]="Audi";
	cars[1]="BMW";
	cars[2]="Volvo";
	
	// 2.
	var cars=new Array("Audi","BMW","Volvo");
	
	// 3.
	var cars=["Audi","BMW","Volvo"];
	

#### 下标的形式访问数组中的元素

	cars[0] // Audi

如果使用超过数组长度的下标，会返回undefined  

	cars[9] // undefined

如果给超出数组长度位置的复制，则数组会自动扩充到当前长度，中间没有赋值的为undefined

	cars[5] = "BYD" // 现在数组长度为6 cars ["Audi", "BMW", "Volvo", 5: "BYD"] (6) 

## JavaScript 对象

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

	var person = {name:"小明", age:20}

上面声明了一个person对象，有两个属性，name和age

空格和折行无关紧要。声明可横跨多行：

	var person = {
	name:"小明", 
	age:20
	}

访问对象属性的两种方式：

	var name = person.name;
	var name = person["name"]

## Undefined 和 Null

Undefined 这个值表示变量不含有值。  
可以通过将变量的值设置为 null 来清空变量。


**JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。**
	