# javascript

###  Javascript基础第一天

### 1.javascript介绍

javascript是一种运行在客户端（浏览器）的编程语言，实现人机交互效果

 作用：1网页特效（监听用户的一些行为让网页作出对应）

​            2:表单验证（针对表单数据的合法性进行判断）

​            3.数据交互（获取后台数据，渲染到前端）

​           4.服务端编程（node.js）

​            5.桌面程序，app等

浏览器分成：渲染引擎和js引擎（chrome v8 号称最快）

浏览器本身不会执行js代码，而是通过内置javascript引擎来执行，js引擎执行代码时**逐行解释**每一句源码

###### 1.1js组成

 ECMAscript（javascript基础）和web APIs

BOM浏览器对象模型，DOM页面文档对象模型

ECMAscript规定了javascript的基础语法如变量，分支语句，循环语句，对象等

BOM：操作浏览器，如页面弹窗，检测窗口宽度，存储数据到浏览器等

DOM：操作文档如对页面元素移动，大小，添加，删除等

###### 1.2javascript书写位置（行内，内部，外部）

![image-20230305102308659](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305102308659.png)

规范：内部和外部写在</body>前面

注意外部<script></script>之间无需写代码，否则会被忽略

**常见关键字：**break、do、instanceof、typeof、case、else、new、var、catch、finally、return、void、continue、for、switch、while、delete、in、try、let、yielddebugger、function、this、withdefault、if、throw

**常见保留字：**abstract、enum、int、short、boolean、export、interface、static、byte、extends、long、super、char、final、native、synchronized、class、float、package、throws、const、goto、private、transient、debugger、implenments、protected、volatile、double、import、public 　

**尽量不要使用：**arguments、Error、Math、String、Array、eval、NaN、super、Boolean、EvalError、Number、synchronized、Date、Function、Object、throws、decodeURI、Infinity、parseFloat、transient、decodeURIComponent、isFinite、parseInt、volatile、encodeURI、isNaN、RangeError、regExp、encodeURIComponent、JSON 

###### 1.3注释

单行注释 // ctrl+/

多行注释 /* */ shift+alt+a

###### 1.4结束符

作用：使用英文;代表语句结束

可写可不写

###### 1.5输出和输入语法

什么是语法：人和计算机打交道的规则约定

输出语法：1.document.write（'要输出的内容'）中文一定要加引号

作用：向body输出内容

如果输出的内容是标签也会被解析成网页元素

2.alert（'警告'）弹出警告对话框

3.console.log('控制台打印')

作用：控制台输出语法，给程序员调试

输入语法

prompt（'用户输入'）

作用显示一个对话框，对话框包含一天文字信息，用来用户输入文字

confirm（'内容'）弹出可判断的窗口

###### 1.6javascript执行顺序

按html文档顺序执行js代码alert（）和prompt（）会跳过页面渲染先被执行

1.7字面量

在计算机科学中，字面量是计算机中描述 事/物

100 数字字面量

'100' 字符串字面量

[]数组字面量

{}对象字面量

### 2.变量

目标：理解变量是计算机储存数据的“容器”

变量就是一个装东西的盒子（变量是计算机中用来储存数据的容器 它可以让计算机变得有记忆）

注意：变量不是数据本身，它们仅仅是一个用来储存数值的容器。

###### 2.1变量基本使用

1.声明变量

要想使用变量，首先创建变量（声明变量/定义变量）

语法 ：let 变量名（标识符）

声明变量有两部分构成：声明关键字，变量名（标识） let即关键字（ let：许可，允许，让 ，要），所谓关键字是系统提供的专门用来声明（定义）变量的词语

2.变量赋值 “=”赋值号

‘= ’赋值运算符

let age

age = 18

所以编程语言都是右边给左边

定义一个变量后，就能初始化（赋值），在变量名之后跟上一个“=”，然后是数值。

注意：通过变量名来获得变量里面的数据

声明的时候可以直接赋值 let age = 18

3.更新变量 

如let  age  = 18

​         age = 90                           //  不允许多次声明一个变量，没有理由重新声明变量



多个变量之间用逗号隔开 （不建议）

4.变量本质

内存：计算机中存储数据的地方，相当于一个空间

变量本质：程序在内存中申请一块用来存放数据的小空间

###### 2.2变量命名于规范

1不能用关键字

2只能用下划线_,字面，数字，$,数字不能用来开头

3字母严格区分大小写

如Abc和 abc是不同的变量

4.起名要有意义

遵守小驼峰命名法 第一个单词首字母小写，其他大写

###### 2.3变量拓展

let和var 的区别

在旧的javascript使用var来声明变量

var现在开发中一般不在使用它

let为了解决var的一些问题

var声明

   1可以先使用在声明

如 console.log(age)

 var  age =19;//undefined

2.声明过的变量可以重复声明

 var  age =19;

 var  age =199;

console.log(age)//199 后面覆盖前面的

**let是声明变量的关键字，特点：**

1. 不允许重复声明
2. 不存在预解析
3. 在大括号中声明的变量只能在大括号中使用，如if、for的大括号中声明的变量

比如变量提升，全局变量，没有块级作用域等

##### 2.4数组

数组：一组数据存储在单个变量名下

let 数组名 =[数据1，数据2......数据n]

数组是有序的（索引号从0开始）

数组名[索引号]

数组是按顺序保存的，所以每个数据都有自己的编号。计算机中的编号（索引号/下标）从0开始

注意：数组可以存储任意类型的数据

元素：数组中保存的每一个数据都叫数组元素

下标：数组中数据的编号

长度：数组中数据的个数，通过数组的length属性获得 （数组长度等于索引号加1）

### 3.常量

使用：const声明变量称为“常量”

当某个变量永远不会改变的时候，就可以使用const来声明，而不是let

命名规范和let一样

注意：常量不允许重新赋值，声明的时候必须赋值（初始化）

不需要重新赋值的数据使用const

let 现在实际开发变量声明方式

**const是声明常量的，特点：**

1. 不允许重复声明
2. 不允许重新赋值（可以给对象中新增属性）
3. 声明的时候必须赋值
4. 不存在预解析
5. 在大括号中声明的变量只能在大括号中使用，如if、for的大括号中声明的变量

### 4.数据类型

计算机中的万事万物都是数据

js属于弱类语言，只有赋值后才知道数据类型

计算机程序可以处理大量数据，为什么要给数据

1.更加充分和高效的利用内存

2.也更加方便程序员使用数据

整体分为两大类·

基本数据类型（简单数据类型）

number  string boolean undefined 未定义 型 null空类型

引用数据类型（复杂数据类型）object 对象（array  function）

###### 4.1数字型

只要是数字都是数字型 ，经常和算术运算符一起（+-*/ %取余）

%经常作为某个数是否被整除

3%2//1

3%5 //3前面数比后面小的余数就是前面的数

同时使用多个运算符编写程序时，会按着某种顺序先后执行，称为优先级

js中优先级越高越先被执行，优先级相同时以书写从左向右执行

1.* / %优先级相同

2.+ - 优先级相同

3.1>2优先级

4.使用括号可以提升优先级

总结先乘除后加减，有括号先算括号里面的

**NaN表示一个计算错误**，他是一个不正确的或者未定义的数字操作所得的结果

NaN是粘性的，**任何对NaN的操作都会返回**NaN 

NaN===NaN false

###### 4.2字符串型

通过单引号''，双引号""，反引号``包裹的数据都叫字符串，单引号和双引号没有本质区别。

注意：变量不能加引号，加引号就是字符串

1.引号必须成对使用

2.单引号或双引号可以互相嵌套，但是不可以自己嵌套自己（口诀 ，外双内单，或者外单内双）

3.必要时可以使用转义符\，输入单引号或双引号 如（'三次''\但''\是'）//三次'但'是

4.+ 

数字相加，字符相连

5.模版字符串

使用拼接字符和变量

使用反引号`加${}  `

###### 4.3布尔型boolean

表示肯定或否定时在计算机中对应的是布尔类型数据。true  false

###### 4.4未定义undefined

未定义是比较特殊的类型只有一个值undefined

只声明不赋值的情况下变量的默认值为undefined，一般很少为某个变量赋值为undefined

undefined做任何操作都是undefined除字符串拼接外

![image-20230305201849010](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305201849010.png)



undefined-2//NaN

###### 4.5null空类型

在js中仅代表无， 空 ，或值未知的特殊值

undefined表示没有赋值

null表示赋值但内容未空（对象数据类型）

官方解释：null作为尚未创建的对象

将来有个变量里面存放的是一个对象，但是对象还没有创建好，可以先给个null

undefined+1//NaN

null+1//1

// .null 空的
var y = null // **第一个作用可以理解为是占位置**
y = 20
console.log(y)

var z = '我是字符串' // **第二个作用理解是清除一个变量的值**
z = null
console.log(z)****

4.6检测数据类型

1.typeof  变量

2.typeof（变量）

检测是否为数字

is NaN（变量）是数字返回false 非数字true

**面试题** 

​        // console.log(typeof typeof 1) // 'number'输出结果是多少?string

### 5.类型转换

使用表单，prompt获取来的数据默认是字符串类型

###### 5.1隐式转换

某些运算被执行时系统内容自动将数据类型进行转换

规则：+号两边只要有一个字符串，都会把另一个转换为字符串 

除了➕以外的算数运算-*/等都会把数据转换为数字类型

+可以作为正号解析可以转换成数字型，任何数据和字符串相加都是字符串

'123'+2fnw//'1232fnw'字符

+'123'//123 数字

###### 5.2显示转换 

**转换为数字**

Number（数据）

+prompt（‘输入’）隐式转换

parseInt（数据）只保留整数

'12.9'//12

'2.3'//2

parseFloat(数据)保留小数

'12.9'//12.9

'2.3'//2.3

parse系列只能取数字在前面的 如

'12px'//12

'ds12px'//NaN

如果字符串内容有非数字，转换失败时结果为NaN即不是一个数字

NaN也是number类型数据，代表非数字

![image-20230305201446145](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305201446145.png)

**转换为字符串**

变量.toString（）

String（变量）

加号拼接字符串

**转换为布尔值**

Boolean（）

' ',NaN,null,undefined,0 ,false返回false

其余为true

标识符指开发人员为变量，属性，函数，参数取的名字（不能是关键字，保留字）

### javascript基础第二天

#### 运算符

###### 1.算术运算符

+-*/%（取模/取余）

先乘除后加减，有括号先算括号里面的

// 在进行浮点数运算的时候，可能会出现精度丢失的问题
0.1 + 0.2 = 0.30000000000000004;
0.2 + 0.2 = 0.4;
// 尽量少用浮点数进行运算，不要让浮点数进行比较。

// 解决办法 : 根据小数点后面的位数量 乘以对应的整数;
0.1 + 0.2  ==> (0.1*10+0.2*10) / 10 = 0.3



###### 2.赋值运算符

目标：能够使用赋值运算符简化代码

赋值运算符：对变量进行赋值的运算符

=  将等号右边的值赋予给左边，要求左边必须是一个容器

+=  -=  *=  /=  %= 

let num=2

num  = num + 2 //**注意：重新赋值不能只写num+2**

/ / num += 2

###### 3.一元运算符

正负号（必须和变量配合使用）

自增++

作用让变量+1

++//num++ 后置递增 （常用）

先返回原值 再自加一

单独使用前值和后置自增效果一样

//++num 前置递增

先自加一，后返回值

自减--

作用让变量-1

--//num--

//--num

**使用场景：经常用于计数来使用**

###### 4.比较运算符

大于号> 左边是否大于右边 

<   左边是否小于右边 >= 左边是否大于或者等于右边 <=  左边是否小于或者等于右边  

== 左右两边值是否相等 

 不等号！=

左右两边是否不全等 !==  

 左右两边是否类型和值都相等===  

比较结果为boolean类型 （true/false）

**=单等是赋值**

**==是判断**

**===是全等**

**注意：开发中判断是否相等，使用===**

布尔值参与运算转换为0/1

比较运算符有隐式转换 双等号只判断值

2 == '2' true

了解：字符串比较 按照  ASCII

从左向右依次比较

如果第一位一样比较第二位，以此类推

注意：NaN不等于任何值，包括自身

涉及到NaN都是false

**尽量不要比较小数**，**因为小数有精度问题**

// 解决办法 : 根据小数点后面的位数量 乘以对应的整数;
0.1 + 0.2  ==> (0.1*10+0.2*10) / 10 = 0.3

注意：**不同类型之间比较会发生隐式转换**

最终把数据隐式转换成number类型再比较

开发中，如果进行精确的比较 ===或者！==

###### 5.逻辑运算符

使用场景：逻辑运算符用来解决多重条件判断

num > 5 && num <  10

&& and

｜｜or

！not

![image-20230303180151365](/Users/xiamu/Library/Application Support/typora-user-images/image-20230303180151365.png)

###### 6.运算符优先级

![image-20230303183346101](/Users/xiamu/Library/Application Support/typora-user-images/image-20230303183346101.png)

#### 表达式和语句

表达式是可以被求值的代码，javascript引擎会将其计算出一个结果

语句

是一段可以执行的代码

**区别**

表达式：因为表达式可被求值，所以它可以写在赋值语句的右侧。如num =3+3

数字 运算符 变量等组成的式子，所有表达式都有返回值

语句：不一定有值，如alert（）if（） for （）和break 等语句就不能被赋值。alert（）弹出对话框 console.log控制台打印输出

某些情况，可以把表达式理解为表达式语句，因为它是在计算结果，但不是必须的成分（如continue语句）

#### 分支语句

##### 程序三大流程控制语句

从上往下执行，顺序结果

根据条件执行代码，分支结构

重复执行的代码，循环结构

·![image-20230303185011343](/Users/xiamu/Library/Application Support/typora-user-images/image-20230303185011343.png)

##### 分支语句

可以让我们有选择性的执行想要代码

###### if分支语句

三种：单分支，双分支，多分支

单分支使用方法

if（条件）{满足条件要执行的代码

}

括号内的条件为true时，进入大括号里面执行代码（false假则不执行）除了0和空 ''字符串

小括号内的结果若不是布尔类型时，会发生隐式转换为布尔类型

如果大括号只有一句语句，大括号可以省略，但是不提倡 

双分支语句

if（条件）{满足条件要执行的代码

}else{不满足条件要执行的代码

}

多分支语句

利用多个条件来选择不同的语句执行，得到不同的结果，多选一过程

if（条件1）{满足条件要执行的代码

}else if（条件2）{满足条件要执行的代码

}else if（条件3）{满足条件要执行的代码

········

}else{不满足条件要执行的代码

}

**if分支嵌套：****分支进行嵌套使用 表示有多种选择**// 分支的嵌套
if(条件1){
	if(条件2){
  	满足条件1和条件2才会执行这里的代码
	}
	else{
  	满足了条件1但是没有满足条件2执行这里的代码
	}
}

var a,b,c;
if(a>b){
    if(a>c){
       alert("变量a最大");
    }else{
        alert("变量c最大");
    }
}else{
    if(b>c){
       alert("变量b最大");
    }else{
        alert("变量c最大");
    }
}

###### 三元运算符

条件？ 满足条件执行的代码：不满足条件执行的代码

一般用来取值（适合简单的if双分支语句）

执行思路：表达式为真返回1，反之

如 9>10 ? 9: 10 // 9

###### switch语句

switch(数据){

case 值1:

代码1

break

case 值2:

代码2

break

case 值3:

代码3

break

··········

default：

代码1

break

}

解释：找到跟小括号里面数据**全等**case值，并执行代码

若没有全等===的则执行default

switch case语句一般用于等值判断，不合适于区间判断

switch case一般 需要配合break关键字使用 没有break会造成穿透

#### if多分支语句和switch的区别

1.共同点

都能实现多分支选择，多选1

大部分情况下可以互换

2.区别

switch·····case语句通常处理case为比较确定的情况，而if····else语句更加灵活，通常用于范围判断（等于某个范围）

switch·····case语句进行判断后直接执行到程序的语句，效率高，而if·····else语句有几种判断条件，就得判断多少次

switch一定要注意 必须===全等，一定注意数据类型，同时注意break否则会贯穿（穿透效果）

结论

当分支比较少时，if····else语句执行效率高

当分支比较多时，switch·····case语句执行效率高，而且结构更清晰



##### **断点调试**

按f12打开开发者工具

点sources一栏

选择代码

打完断点要刷新浏览器

watch 输入需要检测的变量

![image-20230308101711003](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308101711003.png)

###### while循环 

循环：重复执行一些操作

基本语法

while（循环条件）{

重复执行代码（循环体）

}

跟if语句很像，都要满足小括号里的条件为true才会进入循环体执行代码

while大括号里代码执行完毕后不会跳出，而是继续回到小括号里面判断条件是否满足，若满足又执行大括号里的代码，小括号判断条件，直到括号内条件不满足，即跳出  

**while循环三要素：**

循环的本质就是以某个变量为起始值，然后不断的产生变化量，慢慢靠近终止条件的过程

1.变量起始值

2.终止条件（没有终止条件，循环会一直执行，造成死循环）（操作表达式）

3.变量变化量（用自增或者自减）

###### 退出循环

break退出整个循环

continue退出本次 循环，继续下一次循环

区别：continue一般用于排除或者跳过某一个选项时候，可以使用continue

break一般用于结果已经得到，后续的循环不需要的时候可以使用

##### **第二天基础词汇**

let    声明变量

typeof   检测数据类型

if   条件语句如果

else   否则 

switch    分支语句   

case   选项

default      默认语句

while    

break    退出循环

continue    继续下一次循环

### javascript基础第三天

##### for循环基本使用

###### 1.for循环语法

作用：重复执行代码

好处：把声明起始值，循环条件，变化值写在一起，

for（ 变量起始值；终止条件；变量变化量）{

循环体}

**或**for(声明变量并赋初始值;条件表达式;每重复一次后变量的变化规律){
    重复执行的代码块
}

（**初始化变量**，就是用let声明的普通变量，通用于作为计算器使用）

（**条件表达式**就是用来决定每一次循环是否继续执行，就是**终止条件**）

（**操作表达式是**每次循环最后执行的代码，经常用于计数器变量进行更新）**递增或递减**

// 演变1：把初始值放在循环体的外面(可以写在外面但是注意不要把分号带走)
var i=1
for(;i<=100;i++){
    console.log(i)
}

// 演变2：变量的变化放在循环的下面
for(var i=1;i<=100;){
    console.log(i)
    i++ // while循环的写法
}

// 演变3：尝试用for循环写一个死循环?
for(;;){
    console.log('死循环了')
}

##### for循环最大的价值：循环数组



**退出循环**

continue//退出本次循环，本次循环中continue下面的语句不在执行

break//退出整个循环 

for（；；）{}//死循环

while（true）{}

**for和while区别** 

![image-20230304162236658](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304162236658.png)

##### 循环嵌套

**双重循环**

![image-20230304162618896](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304162618896.png)

外层循环一次，里层循环全部

##### 数组

数组：Array是一种可以按顺序保存数据的数据类型

使用：如果有多个数可以用数组保存起来，然后放到一个变量中，管理非常方便 

1.**声明语法**

.字面量声明数组

let 数组名[ 数据1，数据2·······数据n]  

.使用new Array 构造函数声明  

let arr=new Array（数据1，数据2·······数据n）

![image-20230304174906231](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304174906231.png)

**取值语法**

数组名[下标]

![image-20230304175100961](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304175100961.png)

##### 遍历数组

![image-20230304175216886](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304175216886.png)

 let arr = ['马超', '赵云', '张飞', '关羽', '黄忠', '猪头']

​        for (let i = 0; i < arr.length; i++) {

​            document.write(`${arr[i]}\n`) `

​        }

![image-20230304184759019](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304184759019.png)

如果有替换原来的数组元素，不能直接给数组名赋值，否则里面的数组没有了

**数组的长度会自动检测元素变化** 

**改**

let arr=[]

Console.log( arr)//[]

Console.log( arr[0])//undefined

  arr[0]=1

arr[1]=5

Console.log( arr)//[1，5]

![image-20230304185904250](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304185904250.png)

**增**

  数组.push（元素）推

 arr.unshift()添加在开头 同push 用法

![image-20230304190046892](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304190046892.png)

![image-20230304190755448](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304190755448.png)

**重点记住arr.push()**

**删**

数组.pop（）方法从数组中删除最后一个元素，并返回该元素的值

arr.pop()不带参数

arr.shift()方法从数组中删除第一个元素 ，并返回该元素的值 不带参数

arr.splice（）方法删除指定元素   **开发常用，如抽奖，删除指定商品** 

![image-20230304193412267](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304193412267.png)



![image-20230304193539122](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304193539122.png)

// 1.删除数组中的值 数组.splice(开始的下标,删除的个数)
var arr = [1,2,3]
arr.splice(0,1) // 表示从第一个值选择开始 删除一个值
console.log(arr) // [2,3]

// 2.可以添加新的值 数组.splice(开始的下标,0,添加的值)
arr.splice(0,0,4) // 表示开始下标是0 删除0个 添加一个4
console.log(arr) // [4,2,3]

arr.splice(0,2,1,2,3,4,5) // 开始下标是0 删除2个 后面这些12345是添加的
console.log(arr) // [1, 2, 3, 4, 5, 3]

arr.splice(0,0,11,12,13)
console.log(arr) // [11, 12, 13, 1, 2, 3, 4, 5, 3]

// 注意：会改变原数组，返回一个新数组

**冒泡排序**

![image-20230304205730601](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304205730601.png)

![image-20230304214221342](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304214221342.png)

![image-20230304214242986](/Users/xiamu/Library/Application Support/typora-user-images/image-20230304214242986.png)

### javascript第四天基础

**函数封装**

函数的封装是把一个或多个功能通过函数的方式装起来，对外只提供一个简单的函数接口

![image-20230305102002483](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305102002483.png)

**函数：**

function，是被设计为执行特定的代码块

**说明**

函数可以把具有相同或相似逻辑的代码“包裹起来”，通过函数调用执行这些“包裹”的代码逻辑，这么做的优势是**精简代码方便复用提高开发效率**

alert（），prompt（），console.log（）都是**js函数**，只不过**封装好了**，我们直接使用

**函数的使用**语法

语法：就是规则

function 函数名(){

函数体

}

![image-20230305104220364](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305104220364.png)

![image-20230305104234210](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305104234210.png)

 **函数调用语法**

函数名（）//**函数不调用，自己不执行**

//函数一次声明可以多次调用，每次函数调用**函数体**里面的代码会重新执行一次

函数体是函数的构成部分，它负责将相同或相似代码“包裹”起来，直到函数调用函数体内的代码才会被执行。函数的功能代码都要写在函数体当中![image-20230305105311809](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305105311809.png)

**函数的复用代码和循环重复代码的不同**

循环代码写完即执行，不能很方便控制执行位置

随时调用，随时执行，可重复调用 

函数不是用来替换for的 可以用来配合for做更好的事情的

  **函数传数**

 若函数完成 功能需要调用者传入数据，那么就需要用有参数的函数，这样可以**提高函数的灵活性**

**语法**

function 函数名（参数列表/形参）{//形式上的参数

函数体

}

 函数名（参数列表/实参）//实际上的参数

**参数列表**

传入数据列表

声明这个函数需要传入几个数据

多个数据用逗号隔开

![image-20230305114240896](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305114240896.png)

形参只在函数内有效所以不需要声明

实参等于形参正常输出

实参多于形参会取决于**形参个数**，多的实参与函数体内的结果不产生任意的影响，但这时候**函数会默认提供一个内置对象**

实参少于形参 **多的形参定义为undefined ，最终结果为NaN******（声明变量未给值 默认undefined）**

 解决可以给**形参默认值**

![image-20230305120122144](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305120122144.png)

**函数的返回值**

![image-20230305124534688](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305124534688.png)

 **return   **



![image-20230305124953324](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305124953324.png)

![image-20230305125537784](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305125537784.png)

**函数返回值的总结**

1. 使用方法：return  函数的结果

   return将函数内部的执行结果交给外部使用

   函数后面可以没有return，这种情况函数默认返回值undefined

   

2. 注意事项

- 函数返回值return后面的代码不会再去执行，可以理解为return可以终止当前程序，所以return后面的数据不要换行
- return返回出去的值在浏览器中看不见的，只有使用变量接收后才可以看得见

**函数的嵌套【拓展】**	

1. **由于函数的调用可以写在页面的任意地方，在另外一个函数里面调用执行一个函数也是可以的**

**为什么要让函数有返回值**

函数执行后得到的结果，结果是调用者想要拿到的（函数内部不需要输出结果，而是返回结果）

对执行结果的扩展性更高，可以让其他程序使用这个结果

**注意：**

函数只是实现某种功能，最终的结果需要返回函数的调用者时 通过return实现

return**后面的数据不要换行写**

return**只能返回一个值** 多个值返回最后一个数值

解决方法用 数组包裹

**伪数组**

如 [n+n,n-n,n x n,n/n ]

具有数组length属性

按照索引方式进行存储

**注意**

1.两个函数函数名相同， 后面覆盖前面的函数

2.函数内部arguments的使用（内置对象），里面装着所有的实参（只有函数有，并且所有函数都内置好了aruments）

break：结束循环（for while switch）

return：结束函数体内代码 并返回值

##### 作用域

作用域的使用提高程序逻辑的局限性，增强了程序的可靠性，减少了名字冲突

![image-20230305170028551](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305170028551.png)

 **变量作用域同理**

![image-20230305170357701](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305170357701.png)

**全局变量：在全局作用域下的变量，在全局使用**

**局部变量：在局部作用域下的变量，在函数内部使用**（局部作用域分为块级作用域和函数作用域）![image-20230305171105459](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305171105459.png)

**注意：**

**函数的形参也可以看做是局部变量**

**如果在函数内部（局部作用域或者块级作用域），没有声明，只赋值了的也是全局作用域 不建议使用** 如：

function fn（）{

num=10

}

全局 ，局部区别

全局作用域 关闭才会销毁，占内存

局部作用域 程序执行完了就会销毁，节约内存

js没有块级作用域，es6新增块级作用域

![image-20230305172227421](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305172227421.png)

##### **块级作用域**

在ES6阶段，出现了块的概念，新增了块级作用域，同时新增了let、const命令。块级作用域简言之就是**使用一对大括号{}包裹**的一段代码，通过单独的大括号、if块、while块、for块、try/catch/finallyd等都会产生块级作用域



##### **作用域链**

**只要有代码，就至少有一个作用域**

**写在函数内部的局部作用域**

**如果函数中还有函数，那么在这个作用域中就有可以诞生出一个作用域**

**访问原则：能够访问到的情况下 先局部，局部没有在全局**

##### 匿名函数

​    function （）{}

没有名字的函数，无法直接使用

**使用方式**

**函数表达式**

let  fn=function(){ }

fn()

![image-20230305181039111](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305181039111.png)



**立即执行函数**

避免全局变量之间的污染

**方法一**

（function(){}）（）;**多个立即函数必须加；隔开**。第二个小括号 相当于调用

**方法二**

（function(){}（）)//不需要调用立即执行 ，其实不在上调用了            第二个 小括号 相当于调用 

#### 预解析var中

1.js引擎会把js里面所有的var变量还有function函数提前到**当前**作用域的最前面

代码执行，按照代码写的顺序从上往下执行

2.预解析分为函数预解析和变量预解析

1.变量预解析就是把所有声明提升到**当前的作用域最前面**不提升赋值

匿名函数调用必须写在函数下面

如

fun（）

var fun=function（）{}

解析

fun（）

var fun

fun=function（）{}报错//Cannot access 'fun' before initialization,初始化前无法访问“fun”

2.函数预解析就是把所有函数提升到**当前的作用域最前面**不调用函数

##### **逻辑中断**

 **只存在&&与和｜｜或中**

 当有多个表达式（值不是布尔值时）时左边的表达式值可以确定结果时，就不在运算右边表达式的值 

**逻辑与**

**特点一假则假**

**1.第一个真时返回第二个**

**2.第一个假时返回第一个**

**逻辑或**

**特点一真则真**

**1.第一个真时返回第一个**

**2.第一个假时返回第二个**

![image-20230305194653253](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305194653253.png)

![image-20230305194719723](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305194719723.png)

let dpr= window.devicePixelRatio ||1

用来检测像素比

![image-20230305195319124](/Users/xiamu/Library/Application Support/typora-user-images/image-20230305195319124.png)

### javascriot基础第五天

**对象**

##### 1.什么是对象

object：js**里的一种数据类型**

可以理解是一种**无序集合**，注意数组是有序的

**可以详细的描述事物**

![image-20230306100638606](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306100638606.png)

**对象是一组无序的相关属性和方法的集合，所以事物都是对象**，如字符串，数组，函数

##### 2.对象使用

let 对象名={}

let 对象名=new Object{}//构造函数

属性：**事物的特征**（名词），在对象中用属性来表示

方法：**事物的行为**（动词），在对象中用方法来表示

**对象表达结构更清晰，更强大**

let 对象名={

属性名：属性值，

方法名：函数名 ，

}

**new**创建

let 对象名=new Object{};

对象名.属性名=属性值;

对象名.方法名=函数名 

##### 变量和属性区别

1.都是用来存储数据的

2.不同点

变量：单独声明赋值，使用的时候直接写变量名，单独存在

属性：在对象里面不需要声明，使用的时候**对象.属性**或**对象['属性']**

##### 函数和方法区别

1.**都是实现某种功能做某事**

2.函数单独声明并调用 函数名单独存在的 函数名（）

3.方法在对象里面调用

对象名.方法（）



![image-20230306101754124](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306101754124.png)

**使用对象**

对象本质是无序的数据集合，操作数据**增 删 改 查**

**查询**

 对象.属性

 对象[' 属性名 ']

![image-20230306104934011](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306104934011.png)



**改**

对象.属性=值

**增**

对象.新属性名=新值

**注意**：增和改的语法一致，，对象有没有这个属性，**没有就算增，有就算改**

**删除**（**了解）**

delete 对象名.属性名



##### 3.遍历对象



**for遍历对象的问题**

**对象里面是无序的键值对，没有规则，不像数组里面有规则的下标**

**对象没有像数组一样的length属性，所以无法确认长度**

##### for ···in

let arr=[1,2,34,4]

for（let k in arr）{//一般写k/key

console.log（k）//数组的下标 索引号'0 '  '1'  '2' ' 3'**字符串**型

console.log（arr[k]）//'1' '2' '34' '4'

}//不推荐遍历数组

**.遍历对象 for in**

![image-20230306114013584](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306114013584.png) ![image-20230306113920051](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306113920051.png)

##### 4.内置对象

内置对象就是javascript语言自带的一些对象，这些对象供开发人员使用，并提供一些常用的或最基本的（属性和方法）

Console.log()

Dcoument.write() 

**数学对象**

![image-20230306134313642](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306134313642.png)

Math.ceil:向上取整

Math.floor:向下取整

Math.pow：幂运算

Math.max()

Math.min()

Math.abs() 绝对值

**随机生成Math.random（）0-1之间的随机数（包含0不包括1）**

**取0到10得随机数**

Math.floor（Math.random（）*（10+1））

![image-20230306163841659](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306163841659.png)

![image-20230306164048550](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306164048550.png)



** **

##### **5.方法**

![image-20230306105233455](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306105233455.png)



**方法调用**

 let obj={

umane：‘'阿萨说',

song:function (x,y){//形参

console.log(x+y)

}

}

obj.song(1，2)//实参

document.write（）//实参

![image-20230306111421445](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306111421445.png)

##### **数组概念&方法**

1. **数组的reverse / concat / join / sort / splice  方法**

// 1.数组的反转方法：数组.reverse() 
let arr = [3,2,1]
arr.reverse()
console.log(arr) // [1,2,3]

// 2.数组的拼接方法：数组.concat(需要拼接的值)
let arr1 = arr.concat(4)
console.log(arr1) // [3,2,1,4]
// (1)拼接数组方法会返回一个新的数组 需要使用变量去接收
// (2)如果想拼接多个值的时候,之间需要使用逗号隔开
// (3)数组拼接方法不仅仅可以拼接数据,还可以拼接其他的数据类型(数组)

// 拼接字符串方法：数组.join("符号")
var arr = ["我","你"]
var arr1 = arr.join("*********")
console.log(arr1) // 可以拼接数组中的多个值 然后转换为字符串

// 4.数组排序方法:数组.sort()
var arr = [1,5,4,7,9,2,10,22,33,40]
var arr1 = arr.sort()
console.log(arr1) 
var arr2 = arr1.reverse()
console.log(arr2)
// (1)默认是升序,从小到大的
// (2)如果想从大到小,需要反转一下
// (3)只能判断第一位数,10以下的排序

// 5.截取数组方法：数组.slice(开始的下标,结束的下标)
var arr = [1,2,3,4,5,6,7]
var arr1 = arr.slice(1,4) 
console.log(arr1) // [2,3,4]
var arr2 = arr.slice(1) 
console.log(arr2) // [2, 3, 4, 5, 6, 7]
var arr3 = arr.slice(-3,-2)
console.log(arr3) // [5]
// (1)截取方法也会返回一个新的数组,需要使用变量去接收
// (2)[ 开始下标,结束下标 ) 包含开始,不包含结束
// (3)截取数组只写一个参数的时候表示从当前下标开始后面的全部都要选中
// (4)当两个参数为正的时候:当第一个参数比第二个参数大的时候返回空
// (5)当两个参数为负的时候:第二个参数一定要比第一个大,从后往前数

**2.数组indexOf / lastIndexOf方法**

// 1.通过数组的值获取相对应下标出现的第一次位置：数组.indexOf(值)
var arr = [1,2,3,3,3,3,4,5,6,7,3,2,1]
var res = arr.indexOf(2) // 输出的是1 表示数组值2从左到右出现的第一次是下标为1的位置
console.log(res)

// 2.通过数组的值获取相对应下标出现的最后一次位置 数组.lastIndexOf(值)
var arr = [1,2,3,3,3,3,4,5,6,7,3,2,1]
var res = arr.lastIndexOf(1)
console.log(res) // 从左到右 最后一次出现的下标

// 注意：如果没找到就会返回-1

3.**数组的splice删除方法**

// 1.删除数组中的值 数组.splice(开始的下标,删除的个数)
var arr = [1,2,3]
arr.splice(0,1) // 表示从第一个值选择开始 删除一个值
console.log(arr) // [2,3]

// 2.可以添加新的值 数组.splice(开始的下标,0,添加的值)
arr.splice(0,0,4) // 表示开始下标是0 删除0个 添加一个4
console.log(arr) // [4,2,3]

arr.splice(0,2,1,2,3,4,5) // 开始下标是0 删除2个 后面这些12345是添加的
console.log(arr) // [1, 2, 3, 4, 5, 3]

arr.splice(0,0,11,12,13)
console.log(arr) // [11, 12, 13, 1, 2, 3, 4, 5, 3]

// 注意：会改变原数组，返回一个新数组

4.**数组every / some /  filter / map  / forEach /  reduce方法**

// 1.判断数组中的每一个值是否满足需求：数组.every(function(值,下标,数组){})
var arr = [1,2,3,4,5] 
// 判断数组中的值是否都大于0
var res = arr.every(function(value){
    return value>0
})
console.log(res)

// 2.判断数组中的至少有一个值是否满足需求：数组.some(function(值,下标,数组){})
var arr = [1,2,3,4,5] //
// 判断数组中的值至少有一个大于4
var res = arr.some(function(value){
    return value>5
})
console.log(res)

// 3.filter过滤器,过滤数组(可以将满足条件的元素过滤到一起重新组成一个新的数组):数组.filter(function(值){})
var arr = [1,2,3,4,5,6,7]
// 判断数组中大于1的数字 重新的组成一个新的数组
var res = arr.filter(function(value){
    return value > 1
})
console.log(res)

// 4.**【重点】map方法**:将数组中的每一个值都交给函数去处理,处理之后的结果进行返回输出即可：数组.map(function(){})
var arr = [1,2,3,4,5]
var res = arr.map(function(value){
// 将数组中的值都加1
    value += 1
    return value
})
console.log(res)

// 5.forEach专门用来遍历数组的：数组.forEach(function(值){})
// for循环遍历
var arr = [1,2,3,4,5,6]
for(var i=0;i<arr.length;i++){
  console.log(i,arr[i])
}
// forEach遍历
arr.forEach(function(value,index){
  console.log(index,value)
})

// 6.reduce方法表示可以遍历数组，每次都会返回一个新的值：数组.reduce(function(previous,next){})
var arr = [1,2,3,4,5]
arr.reduce(function(previous,next){
    console.log(previous,next)
})
// reduce方法的优势：利用reduce实现数组的求和
var arr = [1,2,3,4,5]
var res = arr.reduce(function(previous,next){
    return previous + next
})
console.log(res)

##### **字符串概念&方法**

1. **this的指向问题**

   // this指向 **默认是指向全局的 window**
   function fn(){
       console.log(this) // 在严格模式下this指向的是undefined
   }
   fn()

   **字符串的创建方式**

   // 1.声明式
   var str = " "

   // 2.构造函数创建 
   var str = new String('')

**通过阿斯克码表，我们可以得出一些字符串比较的规律**

1. 字母比数字大

2. 小写字母比大写字母大

3. 字母越靠后越大

   5.**字符串的基本操作**

// 1.字符串也可以通过下标获取字符
var str = '你好吗';
// 输出下标为1的字符，每个字符都有对应的下标，所以，字符串也可以进行遍历。
console.log(str[1]); // 好

// 2.字符串是只读数据类型，不能添加新字符，不能修改字符串中的字符，不能删除某个字符
var str = '你好吗'
// 修改下标为1的字符
str[1] = "帅"
console.log(str); // 你好吗

### 字符串的方法使用

1. **charAt / charCodeAt / toLowerCase / toUpperCase**

   // 1.charAt(下标) 通过下标获取到相应字符
   var str = "abc123"
   var res = str.charAt(0) 
   console.log(res) // 获取到的是字符a

   // 2.charCodeAt(下标) 通过下标获取到相应的字符的ASCII
   var str = '12345'
   var res = str.charCodeAt(1) // 下标是1，获取到的字符就是2
   console.log(res) //  让2字符串转换为相应的ASCII是50 

   // 3.String.fromCharCode(ASCII) 通过ASCII获取到字符
   console.log(String.fromCharCode(97)) // a

   // 4.toLowerCase() 转换为小写
   console.log("HELLO",toLowerCase()) // hello

   // 5.toUpperCase() 转换为大写
   console.log("hello",toUpperCase()) // HELLO

2. **indexOf  /  lastIndexOf /  concat**

// 1.indexOf() 字符串出现的第一次位置
// 2.lastIndexOf() 字符串出现的最后一次位置
var str = '123321'
var res1 = str.ndexOf('1')
var res2 = str.lastIndexOf('1')
console.log(res1,res2)

// 3.concat字符串的拼接：字符串.concat(被拼接的字符串)
var str = '小明'
var res = str.concat('你好')
console.log(res) // 小明你好

 **split  / slice**

/* 
  一：split 字符串的分割
  1.语法:str.split("分割符号")
  2.用法:将字符串分割为很多段，返回一个新的数组
  3.注意:
  (1)小括号内如果什么都没有的时候,完整输出为数组
  (2)小括号内如果有引号
  		- 没有分割符号的时候,全部分割组成一个新的数组
      - 有分割符号但是这个分割符号不在字符串中,字符串就会完整输出为数组
  (3)还可以在分割符号后面使用一个数字类型 表示保留几个数据 
*/
var str = "hello world"
var res = str.split(" ") 
console.log(res) // ['hello', 'world']
var res1 = str.split()
console.log(res1) // ['hello world']
var res2 = str.split(" ")
console.log(res2) // ['hello', 'world']
var res3 = str.split("?")
console.log(res3) // ['hello world']
var res4 = str.split("",3)
console.log(res4) // ['h', 'e', 'l']

/*  
	二：slice 字符串截取方法
 1.语法：字符串.slice(开始下标,结束的下标)
 2.特点:
 (1)包含开始下标的 不包含结束下标 => [开始下标,结束下标)
 (2)第二个参数可以不写,表示选中从开始下标后面的所有字符
 (3)两个参数可以为负数:第一个参数要小于第二个参数,如果大于的话会返回空值
*/
var str = '千锋教育'
var res = str.slice(0,2)
console.log(res) // 千锋

1. **substr / substring** 

2. /*  
   	一：substr 截取字符串
     (1)语法:字符串.substr(开始的下标,截取的个数)
     (2)包含开始下标,截取字符的个数
     (3)第二个参数可以省略的,表示从开始下标后面所有都会被选中
   */
   var str = '千锋教育'
   var res = str.substr(2)
   console.log(res) // 教育

   /*  
   	二：substring 截取字符串
    1.语法：substring(开始下标,结束下标)
    2.特点
    (1)包含开始下标的 不包含结束下标 => [开始下标,结束下标)
    (2)第二个参数可以不写,就表示从开始下标到后面所有字符都被选中截取下来
    (3)当开始下标等于结束下标的时候会输出空
    (4)当开始下标大于结束下标的时候,两个参数会互换位置再进行截取
    (5)当下标为负数的时候,默认会转换为0,再进行截取
   */
   var str = '千锋教育'
   var res = str.substring(-2,2)
   console.log(res) // 千锋

   **trimStart / trimEnd  / trim** 

   1. // 1.trimStart 截取字符串的开始空格
      // 2.trimEnd 截取字符串的结尾空格
      // 3.trim 截取字符串的头尾空格
      var str = " username "
      console.log(str.trimStart()) 
      console.log(str.trimEnd())
      console.log(str.trim())

      

##### 拓展

![image-20230306201447305](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306201447305.png)

**数据类型**

![image-20230306201757794](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306201757794.png)



**栈和堆**

![image-20230306202051983](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306202051983.png)

![image-20230306202324619](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306202324619.png)

![image-20230306202439459](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306202439459.png)

![image-20230306202459455](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306202459455.png)

![image-20230306203139033](/Users/xiamu/Library/Application Support/typora-user-images/image-20230306203139033.png)

# 第二部分

## Web **APIS**

### **Web APIS第一天获取元素**

变量声明

**常量**

const**语义化更好**

实际开发中也是，react框架，基本const

数组 ，对象用const声明 **复杂数据类型**

栈里面存的地址 堆存数组

复杂数据类型只要地址没有修改就没有变**就可以用const**，如数组添加数据，修改数据还是那个数组（增删改查不会改变地址，**重新赋值才会**）

 ![image-20230308145056803](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308145056803.png)

![image-20230308145702018](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308145702018.png)

##### 作用和分类

**作用：就是使用js去操作html和浏览器**

**分类：DOM（文档对象模型），BOM（浏览器对象模型）**

**DOM（文档对象模型）**

![image-20230308151038054](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308151038054.png)

##### DOM树

![image-20230308151519648](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308151519648.png)

##### DOM**对象**

![image-20230308152110809](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308152110809.png)

#####  获取DOM对象

document.body//body

document.documentElement//html

**重点**

**获取匹配的第一个元素**

**可以直接修改**

document.querySelector（'css选择器'）

**字符串**

返回值

第一个元素，一个htmlElement对象

**获取匹配的多个元素**

document.querySelectorAll（'css选择器'）

**不可以直接修改**因为**返回伪数组**

  ![image-20230308160421328](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308160421328.png)![image-20230308153853131](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308153853131.png)

 console.dir**打印我们返回的元素对象**





<div class="backtop">
        <img src="./images/close2.png" alt="">
        <a href="javascript:;"></a>
    </div> 
//div.children[0]img



**了解**

![image-20230308160657821](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308160657821.png)

#### 操作元素的内容

对象.**innerText**

**不解析标签**

![image-20230308162254234](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308162254234.png)

对象.**innerHtml**

**解析标签**

**![image-20230308162338922](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308162338922.png)**

#### 操作元素属性

![image-20230308174307368](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308174307368.png)

 ![image-20230308174557801](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308174557801.png)

![image-20230308175459178](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308175459178.png)

对象.style['css属性']='css属性值'

对象.style.css属性（小驼峰命名）='css属性值'

![image-20230308182627429](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308182627429.png)

增 元素.className='box'

**多个会覆盖掉**解决

元素.className=' nav box'

删 元素.className=' '

![image-20230308183943128](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308183943128.png)

toggle （）有还是没有，有就删除，没有就添加

![image-20230308202411952](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308202411952.png)

 表单.value 改变文本内容

![image-20230308203345732](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308203345732.png)

**只能接受布尔值**

表单.disabled=true 禁用

表单.checked=true 选中

表单.checked='true'选中//隐式转换

 type,value,checked,selected,disabled

##### 自定义属性

**data**

![image-20230308204749218](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308204749218.png)

##### 定时器

**间歇函数**

循环定时器 setInterval 

单次定时器setTimeout

![image-20230308210304415](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308210304415.png)

setInterval（函数名，间隔时间）

![image-20230308211619242](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308211619242.png)

![image-20230308210748607](/Users/xiamu/Library/Application Support/typora-user-images/image-20230308210748607.png)

 // 清除setInterval单次定时器
 clearInterval(定时器名称);

**定时器得到的是数字**

**拓展**

```js
// 单次定时器，只能执行一次
 setTimeout(function () { },time);
 // - 参数1：function 必需。函数，过time时间之后执行的业务逻辑。
 // - 参数2：time 可选。执行或调用 function 需要等待的时间，以毫秒ms计。默认为 0。1s=1000ms
 
 // 清除setTimeout单次定时器
 clearTimeout(定时器名称);
```

### **Web APIS第二天事件基础**

##### 事件监听（绑定）

**事件是在编程时系统内发生的动作或者发生的事情**

如用户在网页上单击一个按钮

**事件监听**

就是让程序检测是否有事产生，一旦事件触发，就是事件触发，就立即调用一个函数做出函数响应，也称为绑定事件或注册事件

如鼠标经过，点击播放轮播图

![image-20230309111856140](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309111856140.png)

![image-20230309111935157](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309111935157.png)

  

![image-20230309143211385](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309143211385.png)

##### 事件类型

![image-20230309143308652](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309143308652.png)

  ![image-20230309193947927](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309193947927.png)

字符串有长度

![image-20230309195814199](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309195814199.png)

##### 事件对象

  ![image-20230309195923941](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309195923941.png)

 ![image-20230309200315499](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309200315499.png)

![image-20230309201037313](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309201037313.png)

![  ](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309201539473.png)

##### 变量名.trim()去除左右的空格

##### 环境对象

每个函数里面都有**this**  环境对象

**普通**函数里面this指向window

**this指向函数的调用者**

![image-20230309212017159](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309212017159.png)

##### 回调函数

![image-20230309212258386](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309212258386.png)

 ![image-20230309212631821](/Users/xiamu/Library/Application Support/typora-user-images/image-20230309212631821.png)

### Web APIS第三天事件流

**：checked选择被勾选的复选框**

####  事件流（捕获 冒泡）

![image-20230310111458002](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310111458002.png)

##### 事件捕获

![image-20230310112055461](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310112055461.png)

**同名事件 从大到小，从父到子**

##### 事件冒泡

![image-20230310112340020](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310112340020.png)

![image-20230310140925222](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310140925222.png)

![image-20230310140941791](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310140941791.png)

##### 阻止冒泡

![image-20230310114448737](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310114448737.png)

##### 解绑事件

![image-20230310121016500](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310121016500.png)

![image-20230310121031921](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310121031921.png)

![image-20230310125650370](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310125650370.png)

![image-20230310125732303](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310125732303.png)

##### **事件委托**

**优点：减少注册次数，提高程序性能**

**原理：事件委托其实是利用事件冒泡的特点**

**给父元素注册事件，当我们触发子元素的时候，会冒泡到父元素身上，从而触发父元素的事件**

**实现：** **事件对象.target.tagName可以获得真正触发事件的元素**

![image-20230310143357341](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310143357341.png)

  

##### 阻止默认行为

![image-20230310160737431](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310160737431.png)

#### 其他事件

##### 页面加载事件

![image-20230310161428775](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310161428775.png)

![image-20230310161415031](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310161415031.png)

  ![image-20230310161847896](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310161847896.png)



##### 页面滚动事件

![image-20230310162333921](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310162333921.png)

![image-20230310173810582](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310173810582.png)

**可以赋值**

**获取html**

document.documentElement.scrollTop

=**获取的是数字**

![image-20230310173440817](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310173440817.png)

![image-20230310180058526](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310180058526.png)

##### 页面尺寸事件

![image-20230310181141728](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310181141728.png)

包含padding

![image-20230310181944285](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310181944285.png)

#### 元素的尺寸和位置

![image-20230310184014531](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310184014531.png)

 ![image-20230310195257395](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310195257395.png)

![image-20230310195308548](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310195308548.png)

html {

​    scroll-behavior: smooth;

}![image-20230310213729994](/Users/xiamu/Library/Application Support/typora-user-images/image-20230310213729994.png)

### Web APIS第四天操作DOM

#### 日期对象

**用来表示时间的对象**

**可以得到当前系统的时间**

##### 实例化

**只要用new来进行操作的都叫实例化**

**创建一个时间对象并获取时间**

**const date=** **new Date()** 

### 时间对象

**js内部专门提供了一个可以创建设置日期对象的内置函数，叫做Date函数**

**时间对象的创建**

![image-20230311112135245](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311112135245.png)

   星期天 0
1.通过日期对象获取月份 date.getMonth()+1 // js中计算的时候是从0开始数的 0~11结果后面应该+1

**日期的格式化**

**1.转换成年月日 toLocaleDateString()**
**2.转换成时分秒 toLocaleTimeString()**
**3.转换为年月日时分秒 toLocaleString()**
const date = new Date()
console.log(date.toLocaleDateString())
console.log(date.toLocaleTimeString())
console.log(date.toLocaleString())

**设置日期对象**

如：date.getHours(12)                              

#### **时间戳的设置**

![image-20230311122921054](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311122921054.png)

**倒计时**

**获取标准时间**
const date = new Date(0)
console.log(date) // 不加0是当前时间，加0返回的是标准时间//Thu Jan 01 1970 08:00:00 GMT+0800 (中国标准时间)

 有了标准时间可以设置获取时间戳

**第一种方法**：**date.getTime()**
const  date = new Date()
console.log(date.getTime()) // **可以获取当前时间,再把当前时间转换为时间戳** 
const date = new Date('2022-10-1 00:00:00')
console.log(date.getTime()) // **可以自定义时间，再把自定义时间转换为时间戳** 

**第二种方法**：Date.parse('时间')
const date = new Date()
console.log(Date.parse('2022-10-1 00:00:00')) 

**第三种：使用+号**
const date = +new Date() 
console.log(date) 



**第四种：Date.new（）**

const date = new Date()

console.log(Date.new（））

![image-20230311124129112](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311124129112.png)

![image-20230311130502937](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311130502937.png)

####  异步代码执行机制 

定时器

**1非异步执行代码**

●按照从上到下的顺序，从左到右的顺序执行

●依次执行每一句代码，如果上一句代码没有执行完毕，下一句代码就等待

**2异步执行代码**

●当代码执行遇到异步的时候，会把该代码放在异步队列中等待

●等到所有的同步代码执行完毕后，再开始执行异步队列中的代码

**两种定时器就是异步代码**

console.log("开始")

setInterval(function(){

​		console.log('我是定时器')

},0)

console.log("结束")

// 总结：先执行定时器外面的代码，再执行定时器里面的代码(事件轮询)

#### 节点操作

##### DOM节点

![image-20230311150632833](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311150632833.png)

**元素节点所有的标签**

##### 查找节点

![image-20230311151152940](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311151152940.png)

*父节点查找*

**子元素.parentNode**//父

**返回最近一级的父节点 找不到返回为null**

**子元素.parentNode.parentNode**//爷

*子节点查找*

父元素.chidNodes

**获取所有子节点，包括文本节点（空格，换行），注释节点等**

**父元素.children**

**仅获取所有元素节点**

**返回的还是一个伪数组**

**选择的是亲儿子**

*兄弟节点查找*

![image-20230311153841210](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311153841210.png)

##### 增加节点

document.createElememt('div')

****

![image-20230311161529477](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311161529477.png)

![image-20230311155711220](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311155711220.png)

![image-20230311160635757](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311160635757.png)



**如果ul.children[i]（insertBefore（li，ul.children[0]））元素获取不到, 会默认以appendChild形式添加**

##### 克隆节点

![image-20230311163821479](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311163821479.png)

![image-20230311164516171](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311164516171.png)

**true深克隆**

**false浅克隆**

##### 删除节点

![image-20230311164950848](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311164950848.png)



##### 改节点

**元素.innerText**

**元素.innerHTML**

#### M端事件

![image-20230311165922094](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311165922094.png)

#### js插件swiper

![image-20230311170312985](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311170312985.png)

**package文件**

![image-20230311174811440](/Users/xiamu/Library/Application Support/typora-user-images/image-20230311174811440.png)

### Web APIS第五天操作BOM

####  BOM（浏览器对象模型）

![image-20230312091139441](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312091139441.png)

let 和const是挂在自己作用域下的

#### 定时器-延时函数

**setTimeout**

![image-20230312091935606](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312091935606.png)

#### js执行机制

![image-20230312092748223](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312092748223.png)

![image-20230312093048839](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312093048839.png)

![image-20230312093138083](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312093138083.png)

![image-20230312093733695](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312093733695.png)

![image-20230312094656587](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312094656587.png)

#### location对象

 ![image-20230312095649658](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312095649658.png)

![image-20230312103129951](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312103129951.png)

![image-20230312103740169](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312103740169.png)

**hash页面不跳转**获取

spa**单页面**

路由组件

**通过#后面的值拿到**

![image-20230312103815354](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312103815354.png)

//类似f5**刷新页面**

//location.reload(true)ctrl+f5

#### navigator对象

![image-20230312104845953](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312104845953.png)

**//检测userAgent（浏览器信息）**

**!(function () {**

**const userAgent = navigator.userAgent**

**// 验证是否为Android或iPhone**

**const android = userAgent.match(/(Android);?[\s\/]+([\d.]+)?/)**

**const iphone = userAgent.match(/(iPhone\sOS)\s([\d_]+)/)**

**// 如果是Android或iPhone，则跳转至移动站点**

**if (android || iphone) {**

**location.href = 'http://m.itcast.cn'**

**}**

**})();**





// 浏览器的名称、版本等信息，关于浏览器的信息，window下面的对象navigator记录
console.log(navigator.appCodeName) // 返回浏览器的代码名
console.log(navigator.appName) // 返回浏览器的名称
console.log(navigator.appVersion) // 返回浏览器的平台和版本信息
console.log(navigator.cookieEnabled) // 返回指明浏览器是否启用cookie的布尔值
console.log(navigator.platform) // 返回运行浏览器的操作系统平台
**console.log(navigator.userAgent) // 返回由客户机发送服务器的user-agent头部的值**

#### history对象

![image-20230312110600950](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312110600950.png)

// 1.history.back() 返回到上一个页面,相当于浏览器的后退按钮
// 2.history.forward() 前进到下一个页面(下一个页面必须是点击以后的页面)，相当于浏览器的前进按钮
// 3.history.go(数值) 正负数都可以(前进和后退的页面数量) ****

#### 本地存储

 ![image-20230312111249194](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312111249194.png)

![image-20230312111449578](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312111449578.png)

![image-20230312112423005](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312112423005.png)

![image-20230312112206238](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312112206238.png)

![image-20230312112440643](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312112440643.png)

##### **存储复杂数据类型**

![image-20230312113445230](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312113445230.png)

![image-20230312113859880](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312113859880.png)

**JSON.stringify（）存**

**JSON.parse（）取**

![image-20230312114208198](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312114208198.png)

![image-20230312114447532](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312114447532.png)

![image-20230312114351670](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312114351670.png)

#### 数组中的map方法/join方法

![image-20230312152326554](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312152326554.png)

 //map 方法也是遍历 处理数据 可以返回一个数组

![image-20230312153255433](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312153255433.png)

![image-20230312155854351](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312155854351.png)

**map也称为映射**和旧数组有关联

### Web APIS第六天操作正则表达式

![image-20230312204456090](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312204456090.png)

![image-20230312204513340](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312204513340.png)

#### 语法

##### 1.定义正则表达式语法

const 变量名=/表达式/

1.先定义规则

const reg=/前端/

**2.判断是否有符合规则的字符串**

![image-20230312210018426](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312210018426.png)

![image-20230312205947217](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312205947217.png)

![image-20230312210437438](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312210437438.png)

**test重点**

##### 元字符

![image-20230312210619564](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312210619564.png)

**边界符**

表示位置，开头和结尾，必须用什么开头，用什么结尾

![image-20230312211525249](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312211525249.png)

![image-20230312211459895](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312211459895.png)

**量词**

表示重复次数

![image-20230312211936171](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312211936171.png)

 逗号左右两侧不能加空格

![image-20230312213128353](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312213128353.png)



**字符类**

![image-20230312213607675](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312213607675.png)

![image-20230312214036295](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312214036295.png)

{}重复离他最近的[0-9]

[a-zA-Z0-9]只能输入数字或者英文

![image-20230312214820283](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312214820283.png)

![image-20230312214841089](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312214841089.png)

##### 预定义

![image-20230312224648299](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312224648299.png)

####  修饰符

![image-20230312225502389](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312225502389.png)

 ![image-20230312225648520](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312225648520.png)

![image-20230312230025127](/Users/xiamu/Library/Application Support/typora-user-images/image-20230312230025127.png)

**|或的意思**



**change事件**内容发生了变化**时触发**

![image-20230313105055695](/Users/xiamu/Library/Application Support/typora-user-images/image-20230313105055695.png)

![image-20230313115100296](/Users/xiamu/Library/Application Support/typora-user-images/image-20230313115100296.png)

#    javascript进阶

### javascript进阶第一天

#### 作用域

![image-20230315104039935](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315104039935.png)

![image-20230315104323608](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315104323608.png)

![image-20230315104623579](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315104623579.png)

#### 作用域链

**本质是变量查找机制**

![image-20230315105038218](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315105038218.png)

#### js垃圾回收机制

![image-20230315105629064](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315105629064.png)

![image-20230315110015770](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315110015770.png)

![image-20230315110128430](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315110128430.png)

![image-20230315110606314](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315110606314.png)

![image-20230315110848170](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315110848170.png)

![image-20230315110947692](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315110947692.png)

![image-20230315111049003](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315111049003.png)

#### 闭包

![image-20230315112058144](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315112058144.png)

**里层函数使用外层函数变量形成闭包**

![image-20230315114032484](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315114032484.png)

closure

![image-20230315113815057](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315113815057.png)

![image-20230315115424657](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315115424657.png)

![image-20230315115609536](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315115609536.png)

#### 变量提升

![image-20230315120853376](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315120853376.png)

#### 函数进阶

##### 函数提升

![image-20230315121432778](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315121432778.png)

![image-20230315121416319](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315121416319.png)

##### 函数参数

###### 动态参数

**arguments只存在函数里面**

**是一个伪数组**

![image-20230315122647819](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315122647819.png)

###### **剩余参数**

![image-20230315122929266](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315122929266.png) 

![image-20230315123521746](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315123521746.png)

#### 展开运算符

![image-20230315130750612](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315130750612.png)

**求数组最大值和合并数组**

![image-20230315131210558](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315131210558.png)

![image-20230315131245134](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315131245134.png)

##### 箭头函数

![image-20230315133857946](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315133857946.png)

###### 基本语法

![image-20230315134747651](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315134747651.png)

![image-20230315134656525](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315134656525.png)

const fn=()=>{

}

fn()

![image-20230315135242057](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315135242057.png)

![image-20230315135353158](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315135353158.png)

###### 箭头参数

![image-20230315152512540](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315152512540.png)

###### 箭头函数this

![image-20230315153437628](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315153437628.png)



![image-20230315153857318](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315153857318.png)

![image-20230315154023736](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315154023736.png)

![image-20230315154606457](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315154606457.png)

![image-20230315154811423](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315154811423.png)

#### 解构赋值

##### 数组解构

![image-20230315155212034](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315155212034.png)

  ![image-20230315155747210](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315155747210.png)

![image-20230315160356112](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315160356112.png)

![image-20230315162251849](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315162251849.png)

![image-20230315162315253](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315162315253.png)

![image-20230315162627550](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315162627550.png)

##### 对象解构

![image-20230315162758105](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315162758105.png)

 ![image-20230315163625638](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315163625638.png)

**数组对象的解构**

![image-20230315163832122](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315163832122.png)

![image-20230315164518700](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315164518700.png)

![image-20230315164704265](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315164704265.png)

##### 变量数组forEach方法 （加强版的数组）

**适合遍历数组对象**

![image-20230315170648968](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315170648968.png)

##### 筛选数组filter方法

![image-20230315175207455](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315175207455.png)

![image-20230315175406716](/Users/xiamu/Library/Application Support/typora-user-images/image-20230315175406716.png)

## javascript进阶第二天

#### 深入函数

##### 构造函数

![image-20230316092006715](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316092006715.png)

![image-20230316092201985](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316092201985.png)

**命名第一个单词字母以大写字母开头**

**只能由new操作符来执行**

 ![image-20230316093140610](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316093140610.png)

![image-20230316094020941](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316094020941.png)





![image-20230316095949033](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316095949033.png)

![image-20230316100031201](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316100031201.png)



#### 内置构造函数

**基本包装类型**

![image-20230316101122021](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316101122021.png)

![image-20230316101215825](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316101215825.png)

**object**

![image-20230316101835867](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316101835867.png)

**Object.vlaues（o）属性值**![image-20230316102152577](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316102152577.png)

![image-20230316102234580](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316102234580.png)

**array**

 ![image-20230316102759563](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316102759563.png)

 ![image-20230316103109426](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316103109426.png)

![image-20230316103425957](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316103425957.png)

![image-20230316103944213](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316103944213.png)

![image-20230316110833187](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316110833187.png)

Callback **回调函数**

![image-20230316112558182](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316112558182.png)

**伪数组转换为真数组** 

**Array.from（）**

**string**

![image-20230316132724944](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316132724944.png)

![image-20230316142122011](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316142122011.png)

![image-20230316143009505](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316143009505.png)



**number**

![image-20230316144803623](/Users/xiamu/Library/Application Support/typora-user-images/image-20230316144803623.png)

### javascript进阶第三天

#### 面向对象

![image-20230317084949327](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317084949327.png)

![image-20230317085001748](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317085001748.png)

#### 构造函数

![image-20230317090641872](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317090641872.png)

 ![image-20230317090435131](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317090435131.png)

![image-20230317091053068](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317091053068.png)

#### 原型

![image-20230317091800235](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317091800235.png)



**构造函数里面的this指向实例对象 **

**原型对象里面的this指向实例对象**

![image-20230317092555300](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317092555300.png)

##### 数组扩展方法

![image-20230317094414509](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317094414509.png)

##### **constructor属性**

![image-20230317102223993](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317102223993.png)

![image-20230317102329851](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317102329851.png)

##### 对象原型

![image-20230317121253372](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317121253372.png)

![image-20230317120410525](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317120410525.png)

**只读的**，**不能获取赋值**

##### 原型继承

![image-20230317133654372](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317133654372.png)

![image-20230317140747154](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317140747154.png)

##### 原型链

![image-20230317163137166](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317163137166.png)

**只要是对象就有-proto-**指向原型对象

**只要是原型对象就有constructor**指向构造函数

![image-20230317163630531](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317163630531.png)

![image-20230317163815895](/Users/xiamu/Library/Application Support/typora-user-images/image-20230317163815895.png)

原型链就是一个查找规则，可以查找一些属性和方法

沿着一条路来走，查看当前有没有该属性，如果没有就查找它的上一层原型

### javascript进阶第四天

##### 深浅拷贝

![image-20230318101859768](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318101859768.png)

![image-20230318103447511](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318103447511.png)

![image-20230318103530735](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318103530735.png)

#####  深拷贝

![image-20230318103900462](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318103900462.png)

**递归函数**

![image-20230318104843918](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318104843918.png)

![image-20230318105043685](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318105043685.png)

****

![image-20230318153907721](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318153907721.png)

浅拷贝

![image-20230318112235118](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318112235118.png)

****

深拷贝

![image-20230318121416586](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318121416586.png) 

**深拷贝新对象不会对旧对象影响，用递归函数，普通拷贝时候没有问题直接赋值，当遇到数组再次调用函数，遇到对象再次调用递归，先数组后递归**

****

![image-20230318115806986](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318115806986.png)



****

 **第二种方法**

![image-20230318154505537](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318154505537.png)

****

**第三种**

![image-20230318154918230](/Users/xiamu/Library/Application Support/typora-user-images/image-20230318154918230.png)



##### 异常处理

**throw抛异常**

![image-20230319102018966](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319102018966.png)



 **try/catch捕获异常**

![image-20230319104111325](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319104111325.png)

![image-20230319104002195](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319104002195.png)

**debugger**

![image-20230319104737585](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319104737585.png)

#### this指向

**普通函数this指向**

![image-20230319105143937](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319105143937.png)

![image-20230319105653101](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319105653101.png)

****

**箭头函数this指向**

![image-20230319105738787](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319105738787.png)



****

**![image-20230319110005475](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319110005475.png)**

![image-20230319111059793](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319111059793.png)

**原型对象里面函数和构造函数里面的this指向实例**

![image-20230319111227259](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319111227259.png)

####  改变this

**call（）**

**使用较少**

![image-20230319113631440](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319113631440.png)

![image-20230319113946843](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319113946843.png)

****

**apply（）**

**重点**

![image-20230319114047729](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319114047729.png)

![image-20230319120209099](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319120209099.png)

![image-20230319115848199](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319115848199.png)

****

**bind（）**

![image-20230319120325170](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319120325170.png)

**![image-20230319121900255](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319121900255.png)**

![image-20230319121935593](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319121935593.png)

#### 防抖

![image-20230319155830845](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319155830845.png)

![image-20230319161222147](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319161222147.png)

****

![image-20230319161533883](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319161533883.png)

****

![image-20230319162438166](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319162438166.png)

![image-20230319163309248](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319163309248.png)

**函数调用只执行一次，想要下次鼠标经过调用，return接收函数传递给函数调用者**

#### 节流

![image-20230319171300719](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319171300719.png)

![image-20230319171413199](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319171413199.png)

![image-20230319172521598](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319172521598.png)

![image-20230319173201649](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319173201649.png)

****

****

![image-20230319173358926](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319173358926.png)

****

![image-20230319175027369](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319175027369.png)

![image-20230319175047269](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319175047269.png)

![image-20230319180034596](/Users/xiamu/Library/Application Support/typora-user-images/image-20230319180034596.png)

****

****

**数据库**

![image-20230323115315314](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323115315314.png)

### Http与cookie

#### Http协议

**规定数据传输**

**协议：规定数据在传送过程中保证数据的安全和完整**

**http协议规定双方指：客服端 - 服务器**

#### **http规定的三个过程：**

**1.建立连接**

![image-20230323155656731](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323155656731.png)

**三次握手**

三次握手是网络客户端跟网络服务器之问建立连接，并进
行通信的过程。相当于客户端和服务器之间你来我往的3个步骤。

- 第一次握手是建立连接，客户端发送连接请求报文，并
  传送规定的数据包；
- 第二次握手是服务器端表示接收到连接请求报文，并回
  传规定的数据包；
- 第三次握手是客户端接收到服务器回传的数据包后，给服务器端再次发送数据包。这样就完成了客户端跟服务器的连接和数据传送_

![image-20230323162117828](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323162117828.png)

**2.传输**

**客户端>服务器>请求**

![image-20230323163050147](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323163050147.png)

![image-20230323155432853](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323155432853.png)

****

 **服务器>客服端>响应**

**响应状态码**

**1开头的表示正在请求**

**2开头的表示各种成功**

**3开头的表示重定向或缓存**

**4开头的表示客户端请求**

**5开头的表示服务器错误**

![image-20230323155536335](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323155536335.png)



**3.断开连接**

![image-20230323155454986](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323155454986.png)

四次挥手表示当前这次连接请求已经结束，要断开这次连接。

第一次挥手是客户端对服务器发起断开请求

第二次挥手是服务器表示收到这次断开请求

第三次挥手是服务器表示已经断开连接

第四次挥手是客户端断开连接。

#### 会话技术

**问题：http协议是一种无状态的协议 每次请求之间都是独立的，互相没有联系的**

**会话技术解决问题**

可以将第一次请求的时候的数据，存储在浏览器，下一次请求从浏览器中获取这个数据 - cookie

也可以将第一次请求的时候的数据，存储在服务器，下一次请求从服务器中获取这个数据 - session 

#### cookie

**存在浏览器不安全的，浏览器可以直接找到**

 ![image-20230323172146528](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323172146528.png)

![image-20230323172420218](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323172420218.png)

![image-20230323172809790](/Users/xiamu/Library/Application Support/typora-user-images/image-20230323172809790.png)

****



****

## AJAX(async javascript and xml)

**异步的js和XML**

**ajax作用：发送http请求**

**ajax最大的优点：在发送http请求时不刷新页面 /跳转页面-悄悄的发送了请求**



### ajax代码

#### 1.创建ajax对象

![image-20230324173158916](/Users/xiamu/Library/Application Support/typora-user-images/image-20230324173158916.png)

#### 2.ajax是异步

**open（）方法有第三个参数 是可选项-代表是否异步**

**true异步 ，false同步**



![image-20230324182211059](/Users/xiamu/Library/Application Support/typora-user-images/image-20230324182211059.png)

 **![image-20230324183430330](/Users/xiamu/Library/Application Support/typora-user-images/image-20230324183430330.png)**

![image-20230324201608416](/Users/xiamu/Library/Application Support/typora-user-images/image-20230324201608416.png)

![image-20230324204352645](/Users/xiamu/Library/Application Support/typora-user-images/image-20230324204352645.png)

**注册流程**

![image-20230324220400096](/Users/xiamu/Library/Application Support/typora-user-images/image-20230324220400096.png)

#### promise

![image-20230325112546253](/Users/xiamu/Library/Application Support/typora-user-images/image-20230325112546253.png)

![image-20230326162501452](/Users/xiamu/Library/Application Support/typora-user-images/image-20230326162501452.png)

#### es7

##### async/await

async 异步的

await 同步的

![image-20230326172823937](/Users/xiamu/Library/Application Support/typora-user-images/image-20230326172823937.png)

![image-20230326173112654](/Users/xiamu/Library/Application Support/typora-user-images/image-20230326173112654.png)

#### 跨域

![image-20230326182340780](/Users/xiamu/Library/Application Support/typora-user-images/image-20230326182340780.png)

![image-20230326185855066](/Users/xiamu/Library/Application Support/typora-user-images/image-20230326185855066.png)

img link iframe script
