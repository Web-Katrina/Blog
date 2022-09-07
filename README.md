# Blog
2022年前端面试经验汇总

https://muyiy.cn/blog/2/2.2.html#%E5%88%86%E6%9E%90

数组去重：https://juejin.cn/post/7103425593915473927

ajax：https://juejin.cn/post/7104926475752570887

基础web：https://juejin.cn/post/7104923510710992926

面试题：
https://juejin.cn/post/7107272007989297165  
https://juejin.cn/post/7016593221815910408

vue3：
https://v3.cn.vuejs.org/guide/migration/introduction.html#%E7%94%A8%E4%BA%8E%E8%BF%81%E7%A7%BB%E7%9A%84%E6%9E%84%E5%BB%BA%E7%89%88%E6%9C%AC

面试题

css选择器权重

! important --- 10000
内联样式 --- 1000
id选择器 --- 100
属性、伪类、类名选择器 --- 10
标签选择器 --- 1
通配符选择器 --- 0
权重值是256进制的
同一行的选择器权重值相加，权重值较高的样式会覆盖权重值较低的样式

css中visibility:hidden和display:none的区别

作用不同
visibility:hidden将元素隐藏，但是在网页中该占的位置还是占着。
display:none将元素的显示设为无，即在网页中不占任何的位置
使用后HTML元素有所不同
visibility:hidden使用该属性后，HTML元素（对象）仅仅是在视觉上看不见（完全透明），而它所占据的空间位置仍然存在，也就是说它仍具有高度、宽度等属性值。
display:none 使用该属性后，HTML元素（对象）的高度、宽度等各种属性值都将“丢失”。
定义不同
visibility属性指定一个元素是否可见
display属性用于定义建立布局时元素生成的显示框类型

css什么操作下会脱离文档流
1、float 浮动布局
2、position:absolute;绝对定位
3、position:fixed;固定定位
position:relative 相对定位不会脱离文档流，
相对定位
不会影响元素本身的特性，不会使元素脱离文档流；
如果没有定位偏移量，对元素本身没有任何影响
css中伪类和伪元素有哪些
伪类
概念：为处于某个状态的已有元素添加对应的样式，这个状态是根据用户行为而动态改变的。
它可以用于
设置鼠标悬停在元素上时的样式
为已访问和未访问链接设置不同的样式
设置元素获得焦点时的样式
1）状态伪类：基于元素当前状态进行选择的
元素的样式会根据其状态呈现不同的样式，当元素处于某状态时会呈现该样式，而进入另一状态后，该样式也会失去。
常见的状态伪类：
 :link 应用于未被访问过的链接；    
 :hover 应用于鼠标悬停到的元素；
 :active 应用于被激活的元素；
 :visited 应用于被访问过的链接，与:link互斥。
 :focus 应用于拥有键盘输入焦点的元素
注意：
这几个伪类同时出现在一个元素的操作上，顺序不能改变，否则很大程度上会产生紊乱，造成效果失效！
a:hover 必须在 CSS 定义中的 a:link 和 a:visited 之后，才能生效。(意思是必须先写a:link 和 a:visited再写 :hover）
a:active 必须在 CSS 定义中的 a:hover 之后才能生效。(意思是必须先写a:hover再写 :active）
另外伪类名称对大小写并不敏感

2）结构性伪类：css3新增选择器
利用dom树进行元素过滤，通过文档结构的互相关系来匹配元素，能够减少class和id属性的定义，使文档结构更简洁。
常见的结构性伪类：
:first-child 选择某个元素的第一个子元素；
:last-child 选择某个元素的最后一个子元素；
:nth-child(n) 匹配属于其父元素的第 n个子元素，不论元素的类型；
:nth-last-child() 从这个元素的最后一个子元素开始算,选匹配属于其父元素的第 n个子元素，不论元素的类型；
:nth-of-type() 规定属于其父元素的第n个 指定 元素；
:nth-last-of-type() 从元素的最后一个开始计算,规定属于其父元素的指定 元素；
:first-of-type 选择一个上级元素下的第一个同类子元素；
:last-of-type 选择一个上级元素的最后一个同类子元素；
:only-child 选择它的父元素的唯一一个子元素；
:only-of-type 选择一个元素是它的上级元素的唯一一个相同类型的子元素；
:checked匹配被选中的input元素，这个input元素包括radio和checkbox。
:empty 选择的元素里面没有任何内容。
:disabled匹配禁用的表单元素。
:enabled匹配没有设置disabled属性的表单元素。
:valid匹配条件验证正确的表单元素。
:in-range选择具有指定范围内的值的 <input> 元素。
:optional选择不带 "required" 属性的 <input> 元素。
:focus选择获得焦点的 <input> 元素。

伪元素
概念：创建一些不在文档树中的元素，并为其添加样式。(就是选取某些元素前面或后面这种普通选择器无法完成的工作,虽然用户可以看到这些文本，但是这些文本实际上不在文档树中。)
它可以用于
设置元素的首字母、首行的样式
在元素的内容之前或之后插入内容
所有的伪元素：


注意：
CSS3 规范中有一部分要求，为了区分伪类和伪元素，伪元素使用两个冒号 (::)， 伪类使用一个冒号 (:)
::first-line 伪元素只能应用于块级元素。
以下属性适用于 ::first-line 伪元素：
字体属性
颜色属性
背景属性
word-spacing
letter-spacing
text-decoration
vertical-align
text-transform
line-height
clear
::first-letter  伪元素只能应用于块级元素。
下面的属性适用于 ::first-letter 伪元素：
字体属性
颜色属性
背景属性
外边距属性
内边距属性
边框属性
text-decoration
vertical-align（仅当 "float" 为 "none"）
text-transform
line-height
float
clear

实现三角形
1.引入字体图标
2.利用border实现
div {
    width:0;
    height:0;
    border-top:100px solid orange;
    border-left:100px solid transparent;
    border-right:100px solid transparent;
    border-bottom:100px solid transparent;
}
3.利用border+旋转rotate
div {
    width:8px;
    height:8px;
    border-top:1px solid #666;
    border-right:1px solid #666;
    transform:rotate(45deg);
}
4.利用CSS的线性渐变属性linear-gradient
div {
    height:100px;
    width:100px;
    // 从左上到右下，从红色开始渐变到50%位置是透明色渐变开始结束
    background-image:linear-gradient(to bottom right,red 50%,transparent 50%)
}

transform、transition和animation的区别
https://juejin.cn/post/6844904016388816910
transform
定义：transform主要是用于给元素做变换，主要由以下几种变换：rotate(旋转),scale(缩放),skew(扭曲),translate(移动)和matrix(矩阵变换)。
transition
定义：用来定义某个css属性或者多个css属性的变化的过度效果。
属性定义及使用说明：

transition-property:
属性值：
none：没有属性获得过渡效果
all：所有属性的变化都获得过渡效果
property：特定属性变化获得过渡效果，如：width，height，opacity等。
transition-timing-function:
transition-timing-function: linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n)
属性值：
linear: 规定以相同速度开始至结束的过渡效果（等于 cubic-bezier(0,0,1,1)）;
ease: 规定慢速开始，然后变快，然后慢速结束的过渡效果（cubic-bezier(0.25,0.1,0.25,1)）;
ease-in: 规定以慢速开始的过渡效果（等于 cubic-bezier(0.42,0,1,1)）;
ease-out: 规定以慢速结束的过渡效果（等于 cubic-bezier(0,0,0.58,1)）;
ease-in-out: 规定以慢速开始和结束的过渡效果（等于 cubic-bezier(0.42,0,0.58,1)）
cubic-bezier(n,n,n,n): 在 cubic-bezier 函数中定义自己的值。可能的值是 0 至 1 之间的数值
animation
定义：animation动画的定义，先通过@(-webkit-)keyframes定义动画名称及动画的行为，然后再通过animation的相关属性定义动画的执行效果。
用来定义多个中间态的一系列的动画过渡效果。
属性定义及使用说明：

其中animation-name指向的是@keyframes定义的动画。
@keyframes:
@keyframes animationname {keyframes-selector {css-styles;}}


总结：
transform,transition和animation的区别：
transform本身是没有 过渡效果的，它只是对元素做大小、旋转、倾斜等各种变换，通过和transition或者animation相结合，可以让这一变换过程具有动画的效果，它通常只有一个到达态，中间态的过渡可以通过和transition或者animation相结合实现，也可以通过js设置定时器来实现。
transition一般是定义单个或多个css属性发生变化时的过渡动画，比如width,opacity等。当定义的css属性发生变化的时候才会执行过渡动画，animation动画一旦定义，就会在页面加载完成后自动执行。
transition定义的动画触发一次执行一次，想要再次执行想要再次触发。animation定义的动画可以指定播放次数或者无限循环播放。transition：需要用户操作，执行次数固定。
transition定义的动画只有两个状态：开始态和结束态，animation可以定义多个动画中间态，且可以控制多个复杂动画的有序执行。

BFC块级格式化上下文
什么是BFC？
一个BFC区域包含创建该上下文元素的所有子元素，但是不包括创建了新的BFC的子元素的内部元素，BFC是一块块独立的渲染区域，可以将BFC看成是元素的一种属性，拥有了这种属性的元素就会使它的子元素与世隔绝，不会影响到外部其他元素。
BFC形成条件
根元素<HTML>
float属性不为none
position为absolute、fixed
display为inline-block、table-cell
display:flow-root或者flow-root list-item
overflow为hidden、scroll、auto
BFC特性
内部的块级盒子会在垂直方向，一个接一个的放置
两个盒子垂直方面的间距由margin决定。属于同一个BFC的两个相邻盒子的外边距会发生折叠。
BFC的区域不会与浮动盒重叠
BFC就是页面上一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。
计算BFC的高度时，浮动元素也参与计算。
BFC应用
阻止父子外边距合并  overflow:auto 
阻止块级元素与浮动元素的覆盖  overflow:auto 
清除浮动
更多上下文
IFC：内联格式化上下文
FFC：弹性盒格式化上下文
GFC：网格格式化上下文

前端性能优化
尽量减少http请求（合并公共资源、使用雪碧图、合并代码块、按需加载资源）
资源压缩与合并（html压缩，css压缩，js的压缩，文件合并）
使用内容传送网络CDN
避免空src或者href值
使用字体图标iconfont代替图片图标
善用缓存，不重复加载相同的资源
减少反复操作dom
减少重绘和重排
公用css类
高效的js代码
减少循环和循环嵌套以减少js执行时间

防抖与节流的区别
防抖：
触发高频率事件时n秒后只执行一次，如果n秒内再次触发，则会重新计算时间。
节流：
高频事件触发，每次触发事件时设置一个延迟调用方法，并且取消之前延时调用的方法。
区别
区别：降低回调执行频率，节省计算资源。
防抖：是将多次执行变为最后一次执行
节流：是将多次执行变成每隔一段时间执行
函数防抖一定连续触发的事件，只在最后执行一次
函数节流一段时间内只执行一次

Map与Set的区别
Map
Map对象保存键值对。任何值（对象或者原始值）都可以作为一个键或一个值。构造函数Map可以接受一个数组作为参数。
Map和Object的区别：
一个Object的键只能是字符串或者Symbols，但一个Map的键可以是任意值。
Map中的键值是有序的（FIFO原则），而添加到对象中的键不是。
Map的键值对个数可以从size属性获取，而Object的键值对个数只能手动计算。
Object都有自己的原型，原型链上的键名有可能和你自己在对象上的设置的键名产生冲突。

Map对象的属性
size：返回Map对象中所包含的键值对个数
Map对象的方法
set(key,val): 向Map中添加新元素
get(key): 通过键值查找特定的数值并返回
has(key): 判断Map对象中是否有Key所对应的值，有返回true，否则返回false
delete(key): 通过键值从Map中移除对应的数据
clear(): 将这个Map中的所有元素删除
const m1 = new Map([['a',111],['b',222]])
console.log(m1) // {"a" => 111,"b" => 222}
m1.get('a') // 111

const m2 = new Map([['c',3]])
const m3 = new Map(m2)
m3.get('c') // 3 通过键值查找特定的数值并返回
m3.has('c') // true
m3.set('d',555) // 向Map中添加新元素
m3.get('d') // 555 
遍历方法
keys() : 返回键名的遍历器
values() : 返回键值的遍历器
entries() : 返回键值对的遍历器
forEach() : 使用回调函数遍历每个成员
const map = new Map([['a',1],['b',2]])
for(let key of map.keys()){
    console.log(key)
}
// "a"
// "b"
for(let value of map.values()){
  console.log(value)  
}
// 1
// 2
for(let item of map.entries()){
    console.log(item)
}
// ["a",1]
// ["b",2]
// 或者
for(let [key,value] of map.entries()){
  console.log(key,value)  
}
// "a" 1
// "b" 2
// for...of...遍历map等同于使用map.entries()
for(let [key,value] of map){
    console.log(key,value)
}
// "a" 1
// "b" 2
map与其他数据结构的相互转换
map转换为数组（使用扩展运算符）
const arr = [[{'a':1},111],['b':222]]
const myMap = new Map(arr)
[...myMap] // map转数组。 [[{'a':1},111],['b':222]]
Map与对象的互换
const obj = {}
const map = new Map(['a',111],['b',222])
for(let [key,value] of map){
    obj[key] = value
}
console.log(obj) // {a:111,b:222}
JSON字符串要转换成Map可以先利用JSON.parse()转换成数组或者对象，然后再转换即可。

Set
Set对象允许你存储任何类型的值，无论是原始值或者是对象引用。它类似于数组，但是成员的值都是唯一的，没有重复的值。
Set本身是一个构造函数，用来生成Set数据结构。Set函数可以接受一个数组（或者具有iterable接口的其他数据结构）作为参数，用来初始化。

Set中的特殊值
Set对象存储的值总是唯一的，所以需要判断两个值是否恒等。有几个特殊值需要特殊对待：
+0与-0在存储判断唯一性的时候是恒等的，所以不重复
undefined 与 undefined是恒等的，所以不重复
NaN 与NaN是不恒等的，但是在Set中认为NaN与NaN相等，所以只能存在一个，不重复。
Set实例对象的属性
size：返回Set实例的成员总数。
Set实例对象的方法
add(value) : 添加某个值，返回Set结构本身（可以链式调用）。
delete(value) : 删除某个值，删除成功返回true，否则返回false。
has(value) : 返回一个布尔值，表示该值是否为Set的成员。
clear() : 清除所有成员，没有返回值。
const mySet = new Set(['a','a','b',1,2,1])
console.log(mySet) // {'a','b',1,2}
mySet.add('c').add({'a':1})
console.log(mySet) // {'a','b',1,2,'c',{a:1}}
console.log(mySet.size) // 6

mySet.has(2) // true
遍历方法
keys() : 返回键名的遍历器
values() : 返回键值的遍历器
entries() : 返回键值对的遍历器
forEach() : 使用回调函数遍历每个成员
由于Set结构没有键名，只有键值（或者说键名和键值是同一个值），所以keys方法和values方法的行为完全一致。
const set = new Set(['a','b','c'])
for(let item of set.keys()){
    console.log(item)
}
// a
// b
// c
for(let item of set.values()){
    console.log(item)
}
// a
// b
// c
for(let item of set.entries()){
    console.log(item)
}
// ["a","a"]
// ["b","b"]
// ["c","c"]

// 直接遍历set实例，等同于遍历set实例的values方法
for(let i of set) {
    console.log(i)
}
//a
//b
//c
set.forEach((value,key) => console.log(key + ':' + value))
//a:a
//b:b
//c:c
Set对象作用
数组去重（利用扩展运算符）
const mySet = new Set([1,2,3,4,4])
[...mySet] // [1,2,3,4]
合并两个set对象
let a = new Set([1,2,3])
let b = new Set([4,3,2])
let union = new Set([...a,...b]) // {1,2,3,4}
交集
let a = new Set([1,2,3])
let b = new Set([4,3,2])
let intersect = new Set([...a].filter(x => b.has(x)))
// {2,3} 利用数组的filter方法
差集
let a = new Set([1,2,3])
let b = new Set([4,3,2])
let difference = new Set([...a].filter(x => !b.has(x))) // {1}


原型与原型链
https://blog.csdn.net/chilanzi/article/details/123532561
原型：
一个可以被复制（或者叫克隆）的一个类，通过复制原型可以创建一个一模一样的新对象，也可以说原型就是一个模版，在设计语言中更准确的说是一个对象模版
原型是定义了一些公用的属性和方法，利用原型创建出来的新对象实例会共享原型的所有属性和方法
所有引用类型都有一个__proto__ （隐式原型）属性，属性值是一个普通的对象
所有函数都有一个prototype（原型）属性，属性值是一个普通的对象
所有引用类型的__proto__ 属性指向它构造函数的prototype
说说对原型的理解：
在JavaScript中，每当定义一个对象（函数也是对象）时候，对象中都会包含一些预定义的属性。其中每个函数对象都有一个prototype属性，这个属性指向函数的原型对象，使用原型对象的好处是所有对象实例共享它所包含的属性和方法。

什么是原型？
每个对象拥有一个原型对象，通过 proto 指针指向其原型对象，并从中继承方法和属性，同时原型对象也可能拥有原型，这样一层一层，最终指向null（Object.prototype.__proto__指向的是null）。这种关系被称为原型链，通过原型链一个对象可以拥有定义在其他对象中的属性和方法
prototype 和 proto 区别是什么？
prototype是构造函数的属性
__proto__ 是每个实例都有的属性，可以访问[[prototype]]属性
实例的__proto__ 与其构造函数的prototype指向的是同一个对象
显式原型：
prototype 每一个函数在创建之后，便会拥有一个prototype属性，这个属性指向函数的原型对象，显式原型的作用是用来实现
基于原型的继承与属性的共享
隐式原型：
__proto__ 上面说的这个原型是JavaScript中的内置属性prototype，此属性继承自object对象，但Firefox、Safari和Chrome在每个对象上都支持一个属性__proto__，隐式原型的作用是用来构造原型链，实现基于原型的继承


原型链：
原型链是原型对象创建过程的历史记录，当访问一个对象的某个属性时，会先在这个对象本身属性上查找，如果没有找到，则会去它的 __proto__ 隐式原型上查找，即它的构造函数的prototype，如果还没有找到就会再在构造函数的prototype的 __proto__ 中查找，这样一层一层向上查找就会形成一个链式结构
当查找一个对象的属性时，JavaScript会根据原型链向上遍历对象的原型，直到找到给定名称的属性为止，直到到达原型链顶部仍然没有找到指定的属性，就会返回undefined。
也可以理解为原型链继承时查找属性的过程是先查找自身属性，当自身属性不存在时，会在原型链中逐级查找所有从原型或更高级原型中的得到、执行的方法，其中的this在执行时，指向当前这个触发事件执行的对象。
原型和原型链的区别：
原型是为了实现对象间的联系，解决构造函数无法数据共享而引入的一个属性，而原型链是一个实现对象间联系即继承的主要方法。

构造函数：
实例的构造函数（constructor）指向其构造函数
function Person(name){
    this.name = name
}
const person = new Person('lm')
console.log(person.constructor === Person)  // true
实例的构造函数并不是自身属性，而是从原型对象上继承的属性
function Person(name){
    this.name = name
}
const person = new Person(lm);
console.log(person.constructor === Person) // true
console.log(Person.prototype.constructor === Person) // true

console.log(person.hasOwnProperty('constructor'))
// false:constructor属性并不是自身的属性，而是继承来的
原型对象：
__proto__(隐式原型)：每个对象（除了null）都具有的属性，该属性指向该对象的原型
prototype(显式原型)：只有函数对象才有的属性，该属性指向函数的原型对象
例子：
const arr = [1,2,3];
const obj = {
    name:'lm'
}
function add(a,b){
    return a+b
}
console.log(arr)
console.log(obj)
console.log(add)

红框框中的[[ prototype ]] 和 __proto__意义相同，都是指对象的内部属性
而所有函数都拥有prototype属性，所以可以通过 f.prototype得到，那么自然也不需要通过 [[ prototype ]]显示出来（毕竟prototype是显式原型，而__proto__是隐式原型）

箭头函数没有prototype属性

访问原型：
通过实例对象访问原型对象有3种方法
obj.__proto__
obj.constructor.prototype
Object.getPrototypeOf(obj)
function Person(name){
    this.name = name
}
const person = new Person('lm');

const proto1 = person.__proto__
const proto2 = person.constructor.prototype
const proto3 = Object.getPrototypeOf(person)

const proto = Person.prototype // 原型

console.log(proto1 === proto)  // true: 第一种方法
console.log(proto2 === proto)  // true: 第二种方法
console.log(proto3 === proto)  // true: 第三种方法
比较安全的做法是Object.getPrototypeOf(obj)
以下部分会涉及一丢丢原型链的知识
__proto__属性是私有属性，存在浏览器兼容性问题，缺乏非浏览器环境的支持
如果obj的constructor属性被覆盖，那么obj.constructor.prototype将会失败。（因为obj自身是没有constructor属性的，是通过原型链去它的原型上获取constructor属性，所以覆盖该属性时，将不会再去原型链上查找）
function Person(name){
    this.name = name
}
function Temp(name){
    this.name = name
}
const person = new Person('lm');
person.constructor = Temp
const proto = Person.prototype  // 原型
console.log(person.__proto__ === proto)  // true: 第一种方法
console.log(person.constructor.prototype === proto)  // false:第二种方法
console.log(Object.getPrototypeOf(person) === proto) // true:第三种方法

设置原型：
设置原型对象有3种方法
obj.__proto__ = prototypeObj
Object.setPrototypeOf(obbj,prototypeObj)
Object.create(prototypeObj)
const proto = {
    // 原型对象
    name:'prototype'
}
// 第一种方法
const obj1 = {}
obj1.__proto__ = proto // 设置原型
console.log(obj1.name) // prototype
console.log(obj1.__proto__ === proto) // true

// 第二种方法
const obj2 = {}
Object.setprototypeOf(obj2,proto) // 设置原型
console.log(obj2.name) // prototype
console.log(obj2.__proto__ === proto) // true

// 第三种方法
const obj3 = Object.create(proto) // 创建对象并设置原型
console.log(obj3.name) // prototype
console.log(obbj3.__proto__ === proto)  // true
检测原型：
使用obj1.isPrototypeOf(obj2)方法判断obj1是否为obj2的原型
const proto = {
    // 原型对象
    name:'prototype'
}
const proto1 = {
    name:'prototype'
}
const obj = {}
obj.__proto__ = proto // 设置原型

console.log(proto.isPrototypeOf(obj))  // true
console.log(Object.prototype.isPrototypeOf(obj))  // true

console.log(proto1.isPrototypeOf(obj))  // false
prototype  、__proto__   、constructor之间的关系：


function Person(name){
    this.name = name    
}
const person = new Person('lm');
console.log(person.__proto__ === Person.prototype); //true 因为创建person对象的构造函数是Person，
// 所以person对象的隐式原型（__proto__）指向Person函数的原型（prototype）

console.log(Person.prototype.constructor === Person) // true
同一个构造函数创建的多个实例的原型是一个
function Person(name){
    this.name = name
}
const person1 = new Person('lm');
const person2 = new Person('lm');

console.log(person1 === person2) // false :不是同一个对象
console.log(person1.__proto__ === person2.__proto__) 
// true ：同一个构造函数创建的实例对象的原型是同一个

原型链：
由上面的知识可知道，实例对象具有属性__proto__ ，会指向原型对象。而原型对象也是对象，所以也会有属性__proto__ ，也会继续指向它的原型对象。
实例对象在查找熟悉过时，如果查找不到，就会沿着 __proto__ 去他的原型上查找，还找不到，则继续去原型的原型上查找，直到找到或到最顶层为止。这就是原型链的概念。

对象本身的方法（第一层：把方法当成属性）
function Person(name){
    this.name = name;
    this.listenMusic = function(){
        console.log('听音乐')    
    }
}
const person = new Person('clz')
console.log(person)
console.log('实例对象本身是否有listenMusic方法',person.hasOwnPerty('listenMusic'))
person.listenMusic()



对象的原型上添加方法（第二层）
function Person(name){
    this.name = name
}
Person.prototype.listenMusic = function(){
    console.log('听音乐')
}
const person = new Person('clz')
console.log(person)
console.log('实例对象本身是否有listenMusic方法',person.hasOwnProperty('listenMusic'))
person.listenMusic()


原型的原型上的方法（第三层）
function Person(name){
    this.name = name
}
Person.prototype.__proto__.listenMusic = function(){
    console.log('听音乐')
}
const person = new Person('clz')
console.log(person)
person.listenMusic()


但是呢，没法玩第四层，因为已经到顶了（Object.prototype 没有原型（原型为null））
function Person(name){
    this.name = name
}
Person.prototype.__proto__.__proto__.listenMusic = function(){
    console.log('听音乐')
}
const person = new Person('clz')
console.log(person)
person.listenMusic()

person --> Person.prototype --> Object.prototype --> null
那么，这里就来看看第三层是不是真的是Object.prototype
function Person(name){
    this.name = name
}
Person.prototype.__proto__.listenMusic = function(){
    console.log('听音乐')
}
const person = new Person('clz')
console.log(person)

console.log(Person.prototype.__proto__ === person.__proto__.__proto__)
console.log(person.__proto__.__proto__ === Object.prototype)  // 这里就是判断处
person.listenMusic()

原型链的简单图：


原型链的作用：
为对象设置默认值
利用原型为对象设置默认值。当原型属性与私有属性同名时，删除私有属性之后，可以访问原型属性，即可以把原型属性值作为初始化默认值。
function Person(name){
    this.name = name
}
Person.prototype.name = '赤蓝紫'
const person = new Person('clz')
console.log(person.name)  // clz
delete person.name
console.log(person.name) // 赤蓝紫
扩展原型方法：
Array.prototype.test = function(){
    console.log('扩展原型方法：有风险')
}
const arr = [1,2,3]
arr.test() // 扩展原型方法：有风险


JS中new操作符的原理
https://zhuanlan.zhihu.com/p/388517633

虚拟滚动
https://www.jianshu.com/p/0ea012f9a7db
https://blog.csdn.net/qq_45165744/article/details/124784740

图片懒加载原理及实现
https://blog.csdn.net/qq_44947815/article/details/125286969

require与import的区别
https://zhuanlan.zhihu.com/p/121770261
导出方式：
require对应导出的方法是module.exports
import对应的导出方法是export default，export
语法：
require是Common.js的语法
import是ES6的语法标准
加载方式：
require是运行时加载模块里的所有方法（动态加载）
import 是编译的时候调用（静态加载），不管在哪里引用都会提升到代码顶部
引入：
require是Common.js的语法，引入的是整个模块里的对象
import可以按需引入模块里的对象
导出：
require 导出是值的拷贝
import导出的是值的引用

Webpack
https://juejin.cn/post/7103905057694810125
前端代码代码方面：
兼容浏览器：less，postcss，css-loader；bue-loader
编译高级语法或语法：babel-loader，@babel/preset-env，@babel/preset-typescript；polyfill，core-js，regenerator-runtime
减少代码体积，压缩代码：terserPlugin压缩js；minicssExtractPlugin css抽离，CssMinizerPlugin压缩css；压缩代码compressionPlugin
优化代码，使得=加载更快：thread-loader多线程，splitChunks将代码拆分；treeShaking，usedExprts标记，sifeEffects识别代码是否有副作用，PurgeCSSPlugin去除多余css；代码懒加载import()，预加载preLoad，预获取prefetch

module，chunk，bundle区别？
module是开发中的单个模块，各个源码文件，webpack一切皆模块
chunk是代码分割出来的代码块，多模块合并成的，比如entry，output中的多模块，splitChunk
bundle是输出的打包文件
loader，plugin区别？
loader：
loader是转换器，对特定类型进行转换，如将less等转为css
loader本质是一个函数，对接收的内容进行转换，返回转换后的结果，因为webpack只认识js，所以对其他类型进行转换的预处理工作
loader在module.rules中配置，是一个数组；数组中的每一项都是一个对象，包含test，use(loader，options)等属性
plugin：
plugin是扩展插件，对webpack现有内容的扩展，是一个扩展器，基于事件流框架Tapable
在webpack生命周期中会广播出很多事件，plugin可以在合适的时机，通过API来提供相应的输出
plugin在plugin中配置，是一个数组；数组中的每一项都是一个实例，参数通过构造函数传入
常用的loader，plugin有哪些？
常用的loader：
关于css的loader:
多线程执行less-loader，thread-loader
less转css，less-loader
添加浏览器前缀，postcss-loader
css-loader，importLoaders执行前几个loader
将css呈现在页面style-loader
module: {  
rules: [    
    // 处理css    
    {      
        test: /\.css$/,      
        use: [        
            'style-loader',        
            {          
                loader: 'css-loader',          
                options: {            
                    importLoaders: 1,            
                    esModule: false          
                 }        
             },        
             'postcss-loader'      
          ],      
          sideEffects: true,    
     },    
     // 处理less    
     {      
         test: /\.less$/,      
         // webpack使用多个loader是从右到左，从下到上      
         use: [        
             'style-loader',        
             {          
                 loader: 'css-loader',          
                 options: {            
                     importLoaders: 2,            
                     esModule: false          
                 }        
             },        
             'postcss-loader',        
             {          
             loader: 'thread-loader',          
             options: {            
                 // 一个 worker 进程中并行执行工作的数量            
                 // 默认为 20            
                 workerParallelJobs: 2          
             }        
            },        
            'less-loader'      
            ]    
            },  
          ]
        },

2. 常见的plugin：
HtmlWebpackPlugin()-webpack.base.js
处理静态文件，生成html文件，也可以使用已经定义好的
CleanWebpackPlugin()-webpack.prod.js
将上次打包的文件删除，生成这次构建的文件
DefinePlugin()-webpack.dev.js-webpack.prod.js
定义全局变量webpack.dev.js
CopyWebpackPlugin()-webpack.prod.js
有的资源不需要打包，直接拷贝到静态目录
VueLoaderPlugin()-webpack.base.js
vue-loader15版本时需要安装插件，vue热更新使用vue-loader+插件
关于css，mini-css-extract-plugin,webpack.prod.js
mini-css-extract-plugin抽离css
与MiniCssExtractPlugin.loader一起在生产环境使用，开发环境不需要
关于css，css-minimizer-webpack-plugin,wabpack.prod.js
压缩css
生产环境进行压缩，mode:production时包含了css-minimizer-webpack-plugin，不用单独写，开发环境不需要压缩
与minimizer配合使用，只要有压缩的就需要minimizer为true
关于css,purgecss-webpack-plugin,webpack.prod.js
css的treeshaking,对于有的css没有被使用，但是打包的时候都会打包，这时可以将未使用的代码treeshaking，不进行打包
关于js,terser-wabpack-plugin,webpack.prod.js
terser-webpack-plugin压缩js代码
terser-webpack-plugin依据的是terser工具，主要是解析识别js，去除空格
production默认压缩js，不用配置
terser-webpack-plugin与minimizer配合使用，只要有压缩的就需要minimizer为true
以前使用uglify压缩js，但是压缩不了es6，现在使用terserplugin
ModuleConcatenationPlugin()-webpack.prod.js
ModuleConcatenationPlugin作用域提升scope hoisting
production已包含此插件，不需要配置
inline-chunk-html-plugin,webpack.prod.js
将代码注入到index.html中，代码少的话，不需要再次发送请求
与htmlwebpackplugin一起使用
compression-webpack-plugin,webpack.prod.js
压缩资源，打包到服务器上部署的是压缩后的代码
speed-weasure-webpack-plugin,webpack.base.js
查看打包时间，通过打包时间可看到哪块使用时间长，可对应进行优化，红色的代表时间长
webpack-bundle-analyzer,webpack.prod.js
对打包内容的分析，可查看大小等
dll库：DllPlugin,DllReferencePlugin,add-asset-html-webpack-plugin
有的共享资源可以抽成dll库，不需要每次都打包，将来使用的时候直接引入库；比如在vue肿，每次都需要打包vue，如果把vue抽离成库，将来使用的时候直接导入库就行
webpack5后，不使用dll打包速度也很快
lgnorePlugin()-webpack.prod.js
避免打包一些资源，例如引入moment，但是只使用其中的中文，英文语言，其他的不使用，这个时候可以避免打包moment

babel与webpack的区别
babel是新语法编译工具，不关心模块化
webpack是打包构建工具，是多个loader，plugin的集合
如何产出一个第三方lib？
使用output产出library暴露出
libraryTarget，不同平台下的模块化规范
library，暴露的名字
globalObject，用于改变this指向

babel-polyfill和babel-runtime的区别？
babel-polyfill会污染全局
babel-runtime不会污染全局，产出第三方lib需要使用babel-runtime

webpack如何实现懒加载？为何要进行懒加载？
有的页面一次性加载时，加载比较慢，这时候可以进行按需加载，也就是懒加载，通过完成某些操作后再加载另外一些代码。这样加快了页面的初始加载速度，减轻了总体体积，是一种很好的网页优化方式。
懒加载一般伴随着代码分离，代码分离能够把代码分离到不同的bundle中，然后可以按需加载或并行加载这些文件。代码分离可以用于获取更小的bundle，以及控制资源加载优先级。
代码分离方式：
1.多入口
entry:{
    // 代码拆分，第一种：多入口，不常用
    login:'./src/js/login.js',
    hmr:'./src/js/hmr.js'
},
output:{
    filename:'js/[name].build.js',
    path:path.resolve(--dirname,'dist')
}
打包出来是两个文件，login.build.js；hmr.build.js
2.多入口，添加依赖防止重复。
entry: {
  // 第二种，防止重复，使用dependOn在多个chunk之间共享模块；添加依赖，lodash,jquery就是依赖，打包出来的shared包括lodash,jquery
  login: {import:'./src/js/login.js', dependOn: 'shared'},
  hmr: {import:'./src/js/hmr.js', dependOn: 'shared'},
  shared: ['lodash', 'jquery']
},
output: {
  filename: 'js/[name].build.js',
  path: path.resolve(__dirname, 'dist')
},
打包出来是四个文件，login.build.js；hmr.build.js；shared.build.js（包含loadsh，jquery）；还是shared.txt
去除依赖的txt文件
const TerserPlugin = require('terser-webpack-plugin')
optimization:{
    minimizer:[
        new TerserPlugin({
            // 第二种拆分，拆分打包后会有.txt文件，去除txt文件
            extractComments:false,        
        })    
    ],
},
3. 单文件入口，通过splitchunks分离代码
splitchunks可以将公共的依赖模块提取到已有的入口chunk中，或者提取到一个新生成的chunk
entry: {
  // 第三种,单文件入口，通过splitchunks拆分公共的依赖模块
  index: './src/index.js'
},
output: {
  filename: 'js/[name].build.js',
  path: path.resolve(__dirname, 'dist')
},
optimization: {
  splitChunks: {
    chunks: 'all'
  }
},
打包出来一个文件index.build.js
chunks : ' all '同步异步都进行拆分
4. 懒加载：触发相应条件进行动态导入
例如在lazyload.js中加载lazy1.js文件
const oBtn = document.createElement('button')
oBtn.innerHTML = '点击加载元素'
document.body.appendChild(oBtn)

// 按需加载
oBtn.addEventListener('click', () => {
  import('./lazy1').then(({ default: element }) => {
    console.log(element)
    document.body.appendChild(element)
  })
})
webpack4在导入CommonJS模块时，将不再解析module.exports的值，所以需要获取default中的值。
进入浏览器显示lazyload.js的打包文件，不显示lazy1.js的打包文件，等点击加载元素后才会显示，缺点：发送请求，如果文件很大，用户能够感知到页面加载

preLoad预加载，prefetch预获取
preload与prefetch区别：
preload chunk会在父chunk加载时，以并行方式开始加载。prefetch chunk会在父chunk加载结束后开始加载
preload chunk具有中等优先级，并立即下载。prefetch chunk在浏览器闲置时下载
preload chunk 会在父chunk中立即请求，用于当下时刻。prefetch chunk会用于未来的某个时刻。
用法：
webpackChunkName: 打包后的名字
webpackPrefetch



箭头函数与普通函数的区别
箭头函数与普通函数相比，缺少了caller，arguments，prototype
声明方式不同，匿名函数
this指向不同（它没有自己的this对象，内部的this就是定义时上层作用域中的this。）
// ES6
function foo() {  
    setTimeout(() => {    
        console.log('id:', this.id);  
    }, 100);
}
// ES5
function foo() {  
    var _this = this;  
    setTimeout(function () {    
        console.log('id:', _this.id);  
    }, 100);
}
箭头函数的this永远不会变，call、apply、bind也无法改变
var name = 'lili'
var person = {
    name: 'nanjiu',
    say: function() {
        console.log('say:',this.name)
    },
    say2: () => {
        console.log('say2:',this.name)
    }
}
person.say.call({name:'小明'}) // say: 小明
person.say2.call({name:'小红'}) // say2: lili
箭头函数没有原型prototype
let fn = name => {
    console.log(name)
}
let fn2 = function(name) {
    console.log(name)
}
console.log(fn.prototype) // undefined
console.dir(fn2.prototype) // {constructor: ƒ}
箭头函数不能当成一个构造函数
没有new.target
箭头函数没有自己的arguments，可以使用rest参数代替
箭头函数不能重复函数参数名称
https://juejin.cn/post/7069943937577779214

Promise三种状态的变化
Promise 的三种状态：
 pending、fulfilled、rejected（未决定，履行，拒绝），同一时间只能存在一种状态，且状态一旦改变就不能再变。promise是一个构造函数，promise对象代表一项有两种可能结果（成功或失败）的任务，它还持有多个回调，出现不同结果时分别发出相应回调。

初始化状态：pending
当调用resolve（成功），状态：pending => fulfilled
当调用reject（失败），状态：pending => rejected
作用：
 1.主要用于异步计算
 2.可以将异步队列化，按照期望的顺序执行，返回符合预期的结果
 3.可以在对象之间传递和操作promise，帮助我们处理队列
延伸问题：什么是异步什么是同步
  同步：1、2、3、4个任务按顺序执行，1执行完毕后2才会开始执行
  异步：1、2、3、4个任务，假如1任务时间比较长，在执行1任务的同时开始执行其他任务，再通过回调 或者事件继续执行1任务，和交付任务的事件顺序无关。
普通异步处理：ajax异步请求、事件监听
容易出现的问题：回调地狱，剥夺return的能力，虽然说可以解决，但是代码结构嵌套程度深，处理复杂，不易于维护。
promise处理异步方式的区别：
1.函数除闭包外不能保存状态，而promise是一个对象可以方便的保存状态
2.并为剥夺return的能力，因此无需层层传递callback，进行回调获取数据
3.代码风格容易理解，便于维护
4.多个一部等待合并便于解决

.then和.catch连续调用容易出现的问题：
多个.then和catch同时连续调用时，一旦出现catch就会绕过中间所有的.then处理直接进入后面的catch中，（状态转变成了rejected状态）
Promise.all()批量处理容易出现的问题：
1.批量处理时，Promise.all([arr1,arr2])将多个数组包装成一个新的Promise实例，返回的就是一个普通的prominse对象
2.批量处理时只有当所有的子prominse执行完成并且都时成功状态时，才会返回一个数组集合结果，其中任何一个子promise处理失败就会转为rejected（失败）状态。
3.失败时返回的是第一个失败的promise对象
Promise.race()批量处理
参数传递处理于Promise.all()一样，区别是只要一个子promise成功，Promise状态就会转变为resolve（成功）状态
https://www.jianshu.com/p/aeb794362c23

浏览器的缓存机制（强制缓存 && 协商缓存）
https://juejin.cn/post/6978668841593225230


 
浏览器缓存机制
将已访问过的资源进行缓存，以便下次访问时能直接访问，减少请求次数，减少带宽，从而更快的加载页面。


HTTP相关的Header
- Expires：响应头，该资源的过期时间。
-Cache-Control：请求头/响应头，缓存控制字段。
-Etag（HTTP1.1）：响应头，资源标识，服务器存储，资源被修改后Etag也会随之发生变化。
-If-None-Match(HTTP1.1)：请求头，服务器会将If-None-Match与被请求资源的最新Etag进行比对。
-Last-Modified(HTTP1.0)：响应头，资源最后一次修改时间。
-If-Modified-Since(HTPP1.0)：请求头，资源最后一次修改时间。

缺陷：
如果资源更新的速度是秒以下单位，那么该缓存是不能被使用的，因为它的时间单位最低是秒。
如果文件是通过服务器动态生成的，那么该方法的更新时间永远是生成时间，尽管文件可能没有变化，所以起不到缓存的作用。

一. 强制缓存
判断是否过期（服务器会通知浏览器一个缓存时间，相关头部信息在Cache-Control和Expires中），如果时间未过期，则直接从缓存中取，即“强缓存”。
Expires
HTTP1.0使用的字段，表示缓存的到期时间，即有效时间+当时服务器的时间。
缺陷
用户可以修改客户端本地时间，而导致浏览器判断缓存失效，重新请求该资源，同时，还导致客户端与服务器的时间不一致，导致缓存失败。
Cache-Control
max-age：设置缓存的最大周期，与Expires相反，时间是相对于请求的时间。
s-maxage：和max-age相同，仅用于共享缓存，如CDN缓存。
public：相应可以被任何对象缓存，即使是通常不可缓存的内容。
private：缓存只能被单个用户缓存，不能作为共享缓存（即代理服务器不可缓存）。
no-cache：可以缓存在客户端，但每次都必须去服务器检查新鲜度，来决定从服务器获取最新资源（200）还是读取缓存（304），即协商缓存。
no-store：不允许在客户端存储，每次都要从服务器请求新的资源。

二. 协商缓存
如果未命中强缓存，即强缓存失效（可能是Cache-Control设置了no-store或no-cache），则判断协商缓存。

Last-Modified & If-Modified-Since(HTTP1.0)
第一次请求资源后，服务器会返回该资源最后一次修改的时间；再次请求时，服务器会把If-Modified-Since 和Last-Modified字段进行比对。相同，则表示未修改，返回304状态码；不同，则表示修改了，返回数据和200状态码（没有发送请求）
由于服务器更新资源的时间单位为秒，即无法识别一秒内进行多次修改的情况。如果资源更新的速度不到1ms，则无法生成新的最后修改时间。所以出现了一组新的字段 Etag 和 If-None-Match 。
Etag & If-None-Match(HTTP1.1)
Etag是HTTP1.1的属性，由服务器生成并返回给客户端。优先级高于Last-Modified。
第一次发起HTTP请求时，服务器返回一个Etag。
第二次发起同一个请求时，客户端会发送一个 If-None-Match，它的值就是Etag，服务器就会把这个Etag和服务器的Etag进行比较。
如果相同，就将 If-None-Match的值设置为false，返回304，使用缓存；如果不同，就将 If-None-Match的值设置为true，返回200和数据。

http2.0与http1.0的区别
https://blog.csdn.net/qq_40927884/article/details/88613140

https与http的区别
https://juejin.cn/post/6904227431939342344
http:
http是超文本传输协议，数据明文传输，所以会被抓包导致信息泄漏，有安全风险问题！
https：
https是具有安全性的SSL加密传输协议。其作用：建立一个信息安全通道，来确保数据的传输，确保网站的真实性。

http的弊端：
无法保证消息的保密性
无法保证消息的完整性和准确性
无法保证消息来源的可靠性

https解决的问题：https协议因为采用密文传输，要比http协议安全。
信任主机的问题
通讯过程中的数据泄密和被窜改。
https的缺点：
缓存不如http高效，会增加数据开销
https协议需要ca证书，费用较高，功能越强大的证书费用越高。
SSL证书需要绑定IP，不能再用同一个IP上绑定多个域名，IPV4资源支持不了这种消耗。
https协议的工作原理
客户端在使用https方式与Web服务器通信时有以下几个步骤：
客户端使用https url访问服务器，则要求web服务器建立SSL链接。
web服务器接收到客户端的请求之后，会将网站的证书（证书中包含了公钥），传输给客户端。
客户端和web服务器端开始协商SSL链接的安全等级，也就是加密等级。
客户端浏览器通过双方协商一致的安全等级，建立会话密钥，然后通过网站的公钥来加密会话密钥，并传送给网站。
web服务器 通过自己的私钥解密出会话密钥。
web服务器 通过会话密钥加密与客户端之间的通信。

对称加密与非对称加密
https://blog.csdn.net/guairena/article/details/114978149

跨域问题（相关原理、解决跨域方案）
https://juejin.cn/post/7125660136495906824

vue生命周期详解
https://blog.csdn.net/weixin_45791692/article/details/124045505
Vue的生命周期就是vue实例从创建到销毁的全过程，也就是new Vue()开始就是vue生命周期的开始。Vue实例有一个完整的生命周期，也就是从开始创建、初始化数据、编译模板、挂载DOM -> 渲染、更新 ->渲染、卸载等一系列过程，称为Vue的生命周期。钩子函数是Vue生命周期中每个阶段对外开放让程序员操作Vue的接口。Vue有8个钩子函数。

beforeVreate(创建前)
这个时候，在实例被完成创建出来，el和data都没有初始化，不能访问data、method，一般在这个阶段不进行操作。
beforeCreate(){
    console.log('----beforeCreate----')
    console.log(this.msg) // undefined
    console.log(this.$el) // undefined
}
created(创建后)
这个时候，vue实例中的data、method已被初始化，属性也被绑定，但是此时还是虚拟dom，真实dom还没生成，$el还不可用。这个时候可以调用data和method的数据及方法，created钩子函数是最早可以调用data和method的，故一般在此对数据进行初始化。
created(){
    console.log('----created----')
    console.log(this.msg) // msg
    console.log(this.$el) // undefined
}
beforeMount(挂载前)
此时模板已经编译完成，但还没有渲染至页面中（即为虚拟dom加载为真实dom），此时el存在则会显示el。在这里可以在渲染前最后一次更改数据的机会，不会触发其他的钩子函数，一般可以在这里做初始化数据的获取。
当vue实例中，el为挂载目标，未对el进行定义，则this.el显示undefined，但页面中存在tamplate也能识别挂载目标，因为tamplate可以被看成占位符。如果对其进行定义则显示<div id="app"></div>，所以，beforeMount读取不了真实的el，在mounted才能读取到真实的el，因为el只有渲染完成后才会存在。这里讲的el是真实的el。在真实的el存在前，在beforeMount中的其实是在页面中的#app，是挂载的目标。



beforeMount(){
    console.log('----beforeMount----')
    console.log(this.msg) // msg
    console.log(this.$el) // undefined
}
Mounted(挂载后)
此时模板已经被渲染成真实DOM，用户已经可以看到渲染完成的页面，页面的数据也是通过双向绑定显示data中的数据。这实例创建期间的最后一个生命周期函数，当执行完mounted就表示，实例已经被完全创建好了，此时，如果没有其它操作的话，这个实例，就静静的躺在我们的内存中，一动不动。
mounted(){
    console.log('----mounted----')
    console.log(this.msg) // msg
    console.log(this.$el) //<div id='app'><span model='msg'></span></div>
}
beforeUpdate
更新前状态（view层的数据变化前，不是data中的数据改变前），重新渲染之前触发，然后vue的虚拟dom机制会重新构建虚拟dom与上一次的虚拟dom树利用diff算法进行对比之后重新渲染。只有view上面的数据变化才会触发beforeUpdate和updated，仅属于data中的数据改变是并不能触发。
updated
数据已经更改完成，dom也重新render完成。
添加一个按钮，给按钮绑定点击事件，点击后更新数据。
<template>
    <div id="app">
        <div style="height:50px"
             ref="spanRef">{{msg}}</div>
        <button @click="clickBtn"></button>
    </div>
</template>
<script>
    export default {
        name:'App',
        data(){
            return {
                msg:'msg'            
            }        
        } ,
        methods:{
            clickBtn(){
                this.msg = 'newMsg'            
            }        
        },
        beforeUpdate(){
            console.log('----beforeUpdate----')
            console.log(this.$refs.$el)   
            console.log(this.msg) // msg                   
        },
        updated(){
            console.log('----updated----')  
            console.log(this.$refs.$el)   
            console.log(this.msg) // msg         
        }   
    }
</script>

在这里跟vue图示有出入，vue图示中说明在beforeUpdate阶段，只有data中的数据改变，而视图的还未更新，视图中还是旧的数据，但在示例中，beforeUpdate钩子函数打印出el可看出视图中的数据已更新。查阅资料后发现，视图层的数据更新才会触发beforeUpdate以及updated。当视图所应用的data更新时，触发钩子函数。

beforeDestroy
销毁前执行（$destroy方法杯调用的时候就会执行），一般在这里善后：清除计时器、清除非绑定的事件等。
destroyed
销毁后（DOM元素存在，只是不再受vue控制），卸载watcher，事件监听，子组件等。


enentBus用法
https://zhuanlan.zhihu.com/p/72777951/

v-for与v-if为什么不能同时使用
https://blog.csdn.net/yu_yu_lll/article/details/125352389

http请求放在vue哪个生命周期里
beforeCreated、created、mounted都可。
mounted:在模板渲染成html后调用，通常是初始化页面完成后，再对html的dom节点进行一些需要的操作。在此生命周期发起网络请求容易造成页面闪屏问题。

vue-router路由模式 hash和history的区别
https://juejin.cn/post/6993840419041706014
hash模式
定义：
hash模式是一种把前端路由的路径用井号 # 拼接在真实url后面的模式。当井号 # 后面的路径发生变化时，浏览器并不会重新发起请求，而是会触发 onhashchange 事件。
hash的特点：
hash变化会触发网页跳转，即浏览器的前进和后退。
hash可以改变url，但是不会触发页面重新加载（hash的改变是记录在window.history中），
即不会刷新页面。也就是说，所有页面的跳转都是在客户端进行操作的。因此，这并不算一次http请求，所以这种模式不利于SEO优化。hash只能修改#后面的部分，所以只能跳转到与当前url同文档的url。
hash通过window.onhashchange的方式，来监听hash的改变，借此实现无刷新跳转的功能。
hash永远不会提交到server端（可以理解为只在前端操作）。

History模式
定义：
history API是 H5 提供的新特性，允许开发者直接更改前端路由，即更新浏览器URL地址而不重新发起请求。

history的特点：
新的url 可以是与当前url 同源的任意url ，也可以是与当前url 一样的地址，但是这样会导致的一个问题是：会把重复的这一次操作记录到栈中。
通过history.state，添加任意类型的数据到记录中。
可以额外设置title属性，以便后续使用。
通过pushState、replaceState来实现无刷新跳转的功能。

vue-router路由模式 history刷新404原因
https://blog.csdn.net/weixin_46293668/article/details/124625636
因为我们的应用是单页客户端应用，当使用 history 模式时，URL 就像正常的 url，可以直接访问http://www.xxx.com/user/id，但是因为vue-router设置的路径不是真实存在的路径，所以刷新就会返回404错误。
想要history模式正常访问，还需要后台配置支持。要在服务端增加一个覆盖所有情况的候选资源：如果 URL 匹配不到任何静态资源，则应该返回同一个 index.html 页面，这个页面就是你 app 依赖的页面。
也就是在服务端修改404错误页面的配置路径，让其指向到index.html。


有限期限内免登录原理
https://juejin.cn/post/6953199671430873118

vue 的data为什么是一个函数而不是对象
JS中的对象是引用类型的数据，当多个实例引用同一个对象时，只要一个实例对这个对象进行操作，其他实例中的数据也会发生变化。
在Vue中，我们更多的是想要复用组件，那就需要每个组件都有自己的数据，这样组件之间才不会相互干扰。
所以组件的数据不能写成对象的形式，而是要写成函数的形式。
数据以函数返回值的形式定义，这样当我们每次复用组件的时候，就会返回一个新的data，也就是说每个组件都有自己的私有数据空间，它们各自维护自己的数据，不会干扰其他组件的正常运行。


vuex
https://juejin.cn/post/7073869980411887652

vue3.0了解多少
https://v3.cn.vuejs.org/guide/migration/introduction.html#%E7%94%A8%E4%BA%8E%E8%BF%81%E7%A7%BB%E7%9A%84%E6%9E%84%E5%BB%BA%E7%89%88%E6%9C%AC
https://www.php.cn/vuejs/464077.html
https://blog.csdn.net/m0_62988965/article/details/123054389
优势：更快、更小、更易维护、更易于原生、让开发者更轻松
更快：
virtualDOM完全重写，mounting & patching提速100%
更多编译时（compile-time）提醒以减少runtime开销
基于Proxy观察者机制以满足全语言覆盖以及更好的性能
放弃Object.defineProperty，使用更快的原生Proxy
Proxy是惰性监听（不会在初始化的时候监听，而是在使用数据的时候才回去监听）
主流浏览器使用Proxy来进行监听，在IE中还是使用2.0中的Object.defineProperty
组件实力初始化速度提高100%
提速一倍/内存使用降低一半
更小：
Tree-shaking更友好（通过webpack的Tree-shaking功能，可以将无用模块“剪辑”，仅打包需要的。对开发人员：能够对vue实现更多其他的功能，而不必担忧整体体积过大。对使用者：打包出来的包体积变小了。）
新的core runtime：～10kb gzipped
3.0新加入了TypeScript以及PWA的支持
部分命令发生了变化：
下载安装 npm  install -g vue@cli
删除了vue list
创建项目 vue create
启动项目 npm run serve
默认项目目录结构也发生了变化
移除了配置文件目录，config 和build文件夹
移除了static文件夹，新增了public文件夹，并且index.html移动到public中
在src文件夹中新增了views文件夹，用于分类 视图组件和公共组件

vue2与vue3的区别
速度更快
体积更小（相比于Vue2，Vue3整体体积变小了，除了移出一些不常用的API，再重要的是Tree-shaking 任何一个函数，如ref、reavtived、computed等，仅仅在用刀的时候才打包，没用到的模块都被摇掉，打包的整体体积变小）
更容易维护
更接近原生
更容易使用
vue3重写了虚拟DOM实现
编译模板的优化
更高效的组件初始化
undate性能提高了1.3～2倍
SSR速度提高了2～3倍
Composition API可与现有的Options API一起使用
灵活的逻辑组合与复用
Vue3模块可以和其他框架搭配使用
更好的Typescript支持
Vue3是基于Typescript编写的，可以享受到自动的类型定义提示

vue 模板编译原理
概念：
平时使用模板时，可以在模板中使用变量、表达式或者指令等，这些语法在html中是不存在的，那vue中什么可以实现？这就归于模板编译功能。模板编译的作用是生成渲染函数，通过执行渲染函数生成最新的vnode，最后根据vnode进行渲染。那么，如何将模板编译成渲染函数？

将模板编译成渲染函数：
此过程可以分成两个步骤：先将模板解析成AST（abstract syntax tree，抽象语法树），然后使用AST生成渲染函数。由于静态节点不需要总是重新渲染，所以生成AST之后，生成渲染函数之前这个阶段，需要做一个优化操作：遍历一遍AST，给所有静态节点做一个标记，这样在虚拟DOM中更新节点时，如果发现这个节点有这个标记，就不会重新渲染它。所以，在大体逻辑上，模板编译分三部分内容：
将模板解析成AST
遍历AST标记静态节点
使用AST生成渲染函数
这三部分内容在模板编译中分别抽象出三个模块实现各自的功能：解析器、优化器和代码生成器。




vue 中的router与location.href的区别
    1. router使用pushState进行路由更新，静态跳转，页面不会重新加载；location.href会触发浏览器，页面重新加载一次
    2. router使用diff算法，实现按需加载，减少dom操作
    3. router是路由跳转或同一页面跳转；location.href是不同页面间的跳转
    4.  router是异步加载this.$nextTick(() => { 获取url })；location.href是同步加载
    location.href 可直接获取当前路径
    parent.location.href 跳转至上一层页面
    top.location.href 跳转至最外层页面

vue keep-alive实现原理
keep-alive是Vue.js的一个内置组件。它能够把不活动的组件实例保存在内存中，而不是直接将其销毁，它是一个抽象组件，不会被渲染到真实DOM中，也不会出现在父组件链中。
它提供了include与exclude两个属性，允许组件有条件地进行缓存。
props
include定义缓存白名单，keep-alive会缓存命中的组件
exclude定义缓存黑名单，被命中的组件将不会被缓存
max定义缓存组件上限，超出上限使用LRU的策略置换缓存数据
created
created方法很简单，就初始化了两个变量
cache用来缓存虚拟dom；
keys用来缓存虚拟dom的键集合
mounted
mounted(){
    this.$watch('include',val =>{
        pruneCache(this,name => matches(val,name))
    })
    
    this.$watch('exclude',val =>{
        pruneCache(this,name => !matches(val,name))
    })
}
在mounted这个钩子中用watch来监听include与exclude这两个属性的改变，在改变的时候实时地更新（删除）this.cache对象数据。pruneCache函数的核心也是去调用pruneCacheEntry。
render
获取keep-alive包裹着的第一个子组件对象及其组件名
根据设定的黑白名单（如果有）进行条件匹配，决定是否缓存。不匹配，直接返回组件实例（VNode），否则执行第三步
根据组件ID和tag生成缓存Key，并在缓存对象中查找是否已缓存过该组件实例。如果存在，直接取出缓存值并更新该key在this.keys中的位置（更新key的位置是实现LRU置换策略的关键），否则执行第四步
在this.cache对象中存储该组件实例并保存key值，之后检查缓存的实例数量是否超过max的设置值，超过则根据LRU置换策略删除最近最久未使用的实例（即是下标为0的那个key）
最后将该组件实例的keepAlive属性值设置为true

destroyed
this.cache中缓存的VNode实例
遍历调用pruneCacheEntry函数删除缓存VNode还要对应执行组件实例的destory函数
keep-alive组件的渲染
keep-alive不会生成真正的DOM节点，这是怎么做到的？
vue在初始化生命周期的时候，为组件实例建立父子关系会根据abstract属性决定是否忽略某个组件。在keep-alive中，设置了abstract:true,那么Vue就会跳过该组件实例
最后构建的组件树中就不会包含keep-alive组件，那么由组件树渲染成的DOM树自然也不会有keep-alive相关的节点了

keep-alive包裹的组件是如何使用缓存的
在首次加载被包裹组件时，由keep-alive.js中的render函数可知，vnode.componentInstance的值是undefined，keepAlive的值是true，因为keep-alive组件作为父组件，它的render函数会先于被包裹组件执行；那么就只执行到i(vnode, false /* hydrating */)，后面的逻辑不再执行

再次访问被包裹组件时，vnode.componentInstance的值就是已经缓存的组件实例，那么会执行insert(parentElm, vnode.elm, refElm)逻辑，这样就直接把上一次的DOM插入到了父元素中

vue中的watch为什么监听不到数组的变化
Vue不能监听到数组和对象值的变化其实和双向绑定的原理有关。Vue双向绑定原理是利用js中的Object.defineproperty重定义对象的get和set方法，而同时这种方法存在缺陷。就是只能监听到对象内已有的值。在监听对象中属性变化的方法中，无疑是使用ES6的proxy更为优越。
总结：
如果操作的是数组：改变数组的值用Vue的$set方法，改变数组的长度用数组的splice方法使数组变化变成可监听的。
如果操作的是对象：如果操作的属性是对象内已有的值，使用$watch，加上关键字deep深度监听对象；如果操作的属性是对象内没有的新属性，使用$set使对象变成可监听的。

computed与watch的区别
https://www.jianshu.com/p/d990e2b74aee
computed：如果一个值依赖多个属性（多对一），用computed更加方便。
watch：如果一个值变化后会引起一系列操作，或者一个值变化会引起一系列值的变化（一对多），用watch更加方便。watch支持异步，computed不支持。
计算属性computed
特点：
1）支持缓存，只有依赖数据发生改变，才会重新进行计算。
2）不支持异步，当computed内有异步操作时无效，无法监听数据的变化。
3）computed属性值会默认走缓存，计算属性是基于它们的响应式依赖进行缓存的。也就是基于data中声明过或者伏组件传递的props中的数据通过计算得到的值。
4）如果一个属性是由其他属性计算而来的，这个属性依赖其他属性是一个多对一或者一对一，一般用computed。
5）如果computed属性值是函数，那么默认会走get方法，函数的返回值就是属性的属性值；在computed中，属性都有一个get和一个set方法，当数据发生变化时，调用set方法。
优点：
   1）当改变ref或者reactive响应式变量值时，整个应用会重新渲染，vue会被数据重新渲染到dom中。这时，如果我们模板中使用了methods中的fullNameFun函数，或者使用了组合式return的函数。随着渲染，方法也会被调用。但是如果computed中所依赖的变量没有发生改变，则不会进行重新的计算，从而性能开销比较小。当新的值需要大量计算才能得到，缓存的意义就非常大。
2）如果computed所依赖的数据发生改变时，计算属性才会重新计算，并进行缓存；当改变其他数据时，computed属性并不会重新计算，从而提升性能。
3）当拿到的值需要进行一定处理使用时，就可以使用computed。

侦听属性watch（vue3中还有watchEffect详细讲解）
特点：
  1）完全等同于vue2中的watch
  2）不支持缓存，数据变化，直接会触发相应的操作
  3）watch支持异步操作
  4）监听的函数接收两个参数，第一个参数是最新的值；第二个参数是输入之前的值；当一个属性发生变化时，需要执行对应的操作，一对多。
  5）监听数据必须是data中声明过过着组合式api中声明的响应式值或者父组件传递过来的props中的数据。当数据变化时触发其他操作，函数有两个参数：
immediate：组件加载立即触发回调函数执行
deep：深度监听；为了发现对象内部值的变化，复杂类型的数据时使用，例如：数组中的对象内容的改变，注意：监听数组的变动不需要这么多。注意：deep无法监听到数组的变动和对象的新增，参考vue数组变异，只有以响应式的方式触发才会被监听到。
注：当需要在数据变化时执行异步或开销较大的操作时，这个方式是最有用的，这时和computed最大的区别。

一般用法，监听单个变量或多个数据源或者一个函数返回值
注：监听一个函数的返回值，当函数里面中所用到的变量发生变化都会触发回调
// 侦听一个 getter
const state = reactive({ count: 0 })
watch(
  () => state.count,
  (count, prevCount) => {
    /* ... */
  }
)
// 直接侦听一个 reactive
const count = ref(0)
watch(state , (newValue, oldValue) => {
  /* ... */
})

// 直接侦听一个 ref
const count = ref(0)
watch(count, (count, prevCount) => {
  /* ... */
})
// 监听多个数据源
watch([fooRef, barRef], ([foo, bar], [prevFoo, prevBar]) => {
  /* ... */
})

// watch 可以监听一个函数的返回值
watch(() => {
   return otherName.firstName + otherName.lastName
},
   value => {
   // 当otherName中的 firstName或者lastName发生变化时，都会进入这个函数
   console.log(`我叫${value}`)
  }
)
监听复杂数据（深度监听deep）
不使用deep时，当我们改变obj.a的值时，watch不能监听到数据变化，默认情况下，watch只监听属性引用的变化，也就是只监听了一层，但改对象内部的属性是监听不到的。
immediate属性：通过声明immediate选项为true，可以立即执行一次watch里面的函数。
import { watch,ref,reactive } from 'vue'
export default {
    setup() {
        let obj = reactive({
            text:'hello'        
        })   
        watch(obj,(newValue,oldValue) => {
            // 回调函数
        },{
            immediate:true,
            deep:true        
        }) 
        return {
            obj        
        }
     }
}
通过使用deep:true进行深入观察，我们监听obj，会把obj下面的属性层层遍历，都加上监听事件，这样做性能开销也会变大，只要修改obj中任意属性值，都会触发回调，那么如何优化性能呢？
可以直接用对象.属性的方法拿到属性，也就是上面说到的侦听一个getter
import { watch, ref, reactive } from 'vue-router'
export default {
  setup() {
   let obj= reactive({
        text:'hello'
    })
    watch(()=>obj.text, (newValue, oldValue) => {
      // 回调函数
    }, {
      immediate: true,
      deep: true
    })
    return {
      obj
    }
  }
}
注意事项：
watch中的函数名称必须是所依赖data中的属性名称。（vue2）
watch中的函数是不需要调用的，只要函数所依赖的属性发生了改变，那么相对应的函数就会执行。
watch中的函数会有2个参数：一个是新值，一个是旧值。
watch默认情况下无法监听对象的改变，如果需要进行监听则需要进行深度监听，深度监听需要配置handler（vue2中才需要）函数以及deep为true。（因为它只会监听对象的地址是否发生了改变，而值是不会监听的）（vue2）在vue3中有些许区别。
watch默认情况下第一次的时候不会去做监听，如果需要在第一次加载的时候也需要去做监听的话需要设置immediate:true。
vue2中数组响应式原理：
重新定义原生数组方法：push 、unshift、pop、splice、sort、reverse因为这些方法可以修改原数组。
拿到原生数组方法Object.create(Array.prototype)。
AOP拦截，再执行重写数组方法前，先执行原生数组方法。
watch在特殊情况下是无法监听到数据的变化
vue2中对数组的解决方案：
通过下标来更改数组中的数据
通过length来改变数组的长度
通过Vue实例方法set进行设置$set(target,propertyName/index,value)
参数：target{Object | Array},propertyName/index{string | number},vaule {any}
this.$delete(this.arr,0)
vue2中深度监听对应的函数名必须为handler，否则无效过，因为watcher里面对应的是对handler的调用。
划重点：在vue3中利用的是ES6的proxy，对数据响应式进行一个数据的代理，可以监控到数组的变化。vue3中如果想要让一个对象变为响应式数据，可以使用reactive或ref。因此$set在vue3中废弃。

3. 方法methods
methods跟前面的都不一样，我们通常在这里写入方法，只要调用就会重新执行一次，相应的有一些触发条件，在某些时候methods 和 computed 看不出来具体的差别，但是一旦在运算量比较复杂的页面中，就会体现出不一样。
注意：computed是具有缓存的，这就意味着只要计算属性的依赖没有进行相应的数据更新，那么computed会直接从缓存中获取值，多次访问都会返回之前的计算结果。
总结
在computed 和 watch 方面，一个是计算，一个是观察，在语义上是有区别的。
计算是通过变量计算来得出数据，而观察是观察一个特定的值，根据被观察者的变动进行相应的变化，在特定的场景下不能相互混用，所以还是需要注意api运用的合理性和语义性。

vue 双向数据绑定原理（介绍发布订阅模式、Dep和Watcher类的实现，Object.defineProperty方法的实现等）
vue接收一个模板和data参数。
1. 首先将data中的数据进行递归遍历，对每个属性执行Object.defineProperty，定义get和set函数。
并为每个属性添加一个dep数组。
当get执行时，会为调用的dom节点创建一个watcher存放在该数组中。
当set执行时，重新赋值，并调用dep数组的notify方法，通知所有使用了该属性watcher，并更新对应dom的内容。
2. 将模板加载到内存中，递归模板中的元素，检测到元素有v-开头的命令或者双大括号的指令，就会从data中取对应的值去修改模板内容，这个时候就将该dom元素添加到了该属性的dep数组中。这就实现了数据驱动视图。
在处理v-model指令的时候，为该dom添加input事件（或change），输入时就去修改对应的属性的值，实现了页面驱动数据。
3.将模板与数据进行绑定后，将模板添加到真实dom树中。
如何将watcher放在dep数组中？
在解析模板的时候，会根据v-指令获取对应data属性值，这个时候就会调用属性的get方法，
我们先创建Watcher实例，并在其内部获取该属性值，作为旧值存放在watcher内部，我们在获取该值之前，在Watcher原型对象上添加属性Watcher.target = this;然后取值，将讲Watcher.target = null；这样get在被调用的时候就可以根据Watcher.target获取到watcher实例对象。

介绍发布订阅模式
如果一家餐厅自主进行外派配送，顾客A、B下单，餐厅记录下来所有定外卖的顾客，那么顾客就是一个watcher类，记录的名单就是一个Dep。
Dep类
负责依赖收集
首先，有个数组，专门用来存放所有的订阅信息
其次，还要提供一个向数组中追加订阅信息的方法
然后，还要提供一个循环，循环触发数组中的每个订阅信息
Watcher类
负责订阅一些事件

创建最简单的Dep类和Watcher类
Dep类的简单创建
class Dep {
    constructor() {
        // 设置存放订阅者信息的数组
        this.subs = [] // 也可以使用Set    
    }
    // 向subs数组中添加订阅者的信息
    addSubs(watcher) {
        this.subs.push(watcher)    
    }
    // 发布通知的方法
    notify(){}
}
Watcher类的简单创建
// 订阅者的类
class Watcher {
    constructor(cb) {
        // 实例的回调函数
        this.cb = cb    
    }
    // 触发回调函数的方法
    update(){
        this.cb()    
    }
}

new 两个watcher实例，此时值传入了回调函数，并未触发回调函数，执行没有输出。
const w1 = new Watcher( () => {
    console.log('我是第一个订阅者');
})
const w2 = new Watcher( () => {
    console.log('我是第二个订阅者');
})
// 执行回调
w1.update() // 我是第一个订阅者

实现基本的发布订阅
new一个Dep实例，将w1、w2添加进去
const dep = new Dep()
dep.addSubs(w1)
dep.addSubs(w2)

想要触发每个订阅者的回调函数，调用notify方法
dep.notify()
------Dep------
// 发布通知的方法
notify() {
    this.subs.forEach(watcher => watcher.update())
}
触发成功
我是第一个订阅者
我是第二个订阅者
在vue中，只有我们将data数值重赋值了，这个赋值的动作会被vue监听到，然后vue要把数据的变化通知到每个订阅者  ，数据驱动的变化不是理所当然发生的，而是需要程序员手动实现。
订阅者（DOM元素）根据最新的数据，更新自己的内容。
什么时候调用notify方法呢？数据变化的时候
什么时候把订阅者收集呢？数据刚创建的时候
new watcher 的回调函数应该传递什么内容呢？根据新数据重新渲染视图的方法
那么vue如何监听到数据的变化然后调用notify方法呢？

介绍Object.defineproperty方法
首先创建一个对象
const obj = {
    name:'za',
    age:20
}
// 赋值操作，此时vue监听
obj.name = 'zz'
利用Object.defineProperty()监听数据的变化
Object.defineProperty(obj,'name',{
    enumerable:true, // 当前属性，允许被循环
    configurable:true, // 当前属性，允许被配置delete
    get() { // getter
        return 'obj name属性值被读取'    
    }
    set(newValue) { // setter
    console.log('obj name属性值被重新赋值为' + newValue);            
    }
})
测试
console.log(obj.name); // obj name 属性值被读取
obj.name = 'zz'； // 触发set 输出：obj.name属性值被重新赋值为zz
所以只要触发了set()那么就要调用notify方法
set(newValue) {
    console.log('obj.name属性值被重新赋值为' + newValue);
    dep.notify()
}

实现Vue中的getter和setter
创建一个vue.js文件，以及index.html，引入JS文件，new出vue实例
在index.html文件下
<div id="app">
    <h3>姓名是：{{name}}</h3>
    <h3>姓名是：{{age}}</h3>
</div>
<script src="./vue.js"></script>
<script>
    const vm = new Vue({
        el:'#app',
        data:{
            name:'aa',
            age:20,
            info:{
                a:'1',
                c:'2'            
            }        
        }    
    })
</script>
此时我们并没有真正引入vue，页面是无法正常渲染的，接下来我们手动实现：
将实例对象中的data属性值挂在到$data
class Vue {
    constructor(options){
        this.$data = options.data    
    }
}
console.log(vm);
此时实例对象中不存在get、set方法

调用数据劫持的方法
constructor(options) {
    this$data = options.data
    // 调用数据劫持的方法
    Observe(this.$data)
}
定义该方法，目的是给每个属性添加get和set方法
function Observe(obj) {
    Object.keys(obj).forEach(key => {
        // 获取属性值
        let value = obj[key]
        Object.defineProperty(obj,key,{
            enumerable:true,
            configurable:true,
            get(){},
            set(){}        
        })            
    });
}
此时每一个属性都具有get和set方法

对get和set方法进行处理
get(){
    console.log('有人获取了${key}的值');
    return value;
}
set(newValue){
    value = newValue;
}
注意到此时info内部的属性是不存在get和set方法的，因为我们只进行了一层循环
采用递归避免这种内部属性没有劫持到的对象
首先考虑递归终止条件，进行递归。
function Observe(obj){
    // 递归终止条件
    if(!obj || typeof obj !== 'object') return;
    // 通过Object.keys(obj)获取到当前obj上的每个属性
    Object.keys(obj).forEach(key => {
        // 获取属性值
        let value = obj[key]
        // 把value子节点进行递归
        Observe(value);
        Object.defineProperty(obj,key,{
            enumerable:true,
            configurable:true,
            get(){
                console.log(`有人获取了${key}的值`);
                return value                            
            },
            set(newValue){
                value = newValue            
            }                         
        })
    });
}
此时所有属性都存在get和set方法

问题：如果直接对info属性进行赋值操作，重新赋值的属性是不存在get和set方法
原因：相当于重新对info属性指向一个新的对象值，所以不在具有

解决：所以要在赋值之后再set中递归一次
set(newValue){
    value = newValue;
    Observe(value)
}


属性代理
每次在浏览器中查看值都很麻烦都要书写
vm.$data
通过
属性代理，直接输入
vm就能输出
vm.$data的内容
即把this.$data上的属性代理到vm实例上
实现像vue一样通过this可以直接访问实例中的属性
// 属性代理
Object.keys(this.$data).forEach(key => {
    enumerable:true,
    configurable:true,
    get(){
        return this.$data[key];                          
    },
    set(newValue){
        this.$data[key] = newValue;           
    }           
})

观察者模式和发布订阅模式的区别
观察者模式和发布订阅模式最大的区别就是发布订阅模式有个事件调度中心



观察者模式
观察者模式：当对象之间存在一对多的依赖关系时，其中一个对象的状态发生改变，所有以来它的对象都会收到通知，这就是观察者模式。

在观察者模式中，只有两种主体：目标对象（Object）和观察者（Observer）。
目标对象 Subject
维护观察者列表 observerList ---------- 维护拥有订阅权限的弟子列表
定义添加观察者的方法 -------- 提供弟子购买订阅权限的功能
当自身发生改变后，通过调用自己的 notify 方法依次通知每个观察者执行  update 方法 ----- 发布对应任务后通知有权限的弟子
观察者 Observer  需要实现 update 方法，供目标对象调用。  update 方法中可以执行自定义的业务逻辑 ---- 弟子们需要定义接收任务通知后的方法，例如去抢任务或任务不合适，继续等待下一个任务。
我们把上面的文字形象化一下：


class Observer {
    constructor(name) {
        this.name = name;
    }
    update({taskType, taskInfo}) {
        // 假设任务分为日常route和战斗war
        if (taskType === "route") {
            console.log(`${this.name}不需要日常任务`);
            return;
        }
        this.goToTaskHome(taskInfo);
        
    }
    goToTaskHome(info) {
        console.log(`${this.name}去任务大殿抢${info}任务`);
    }
}

class Subject {
    constructor() {
        this.observerList = []
    }
    addObserver(observer) {
        this.observerList.push(observer);
    }
    notify(task) {
        console.log("发布五星任务");
        this.observerList.forEach(observer => observer.update(task))
    }
}

const subject = new Subject();
const stu1 = new Observer("弟子1");
const stu2 = new Observer("弟子2");

// stu1 stu2 购买五星任务通知权限
subject.addObserver(stu1);
subject.addObserver(stu2);

// 任务殿发布五星战斗任务
const warTask = {
    taskType: 'war',
    taskInfo: "猎杀时刻"
}

// 任务大殿通知购买权限弟子
subject.notify(warTask);

// 任务殿发布五星日常任务
const routeTask = {
    taskType: 'route',
    taskInfo: "种树浇水"
}

subject.notify(routeTask);
输出结果:
// 战斗任务
发布五星任务
弟子1去任务大殿抢猎杀时刻任务
弟子2去任务大殿抢猎杀时刻任务

// 日常任务
发布五星任务
弟子1不需要日常任务
弟子2不需要日常任务
通过上面代码我们可以看到，当宗门发布任务后，订阅的弟子(观察者们)都会收到任务最新通知。
再给举个栗子: 比如你要应聘阿里巴巴的前端工程师，结果阿里巴巴 HR 告诉你没坑位了，留下你的电话，等有坑位联系你。于是，你美滋滋的留下了联系方式。殊不知，HR 已经留下了好多联系方式。好在 2022 年 2 月 30 号那天，阿里巴巴有了前端工程师的坑位，HR 挨着给留下的联系方式联系了一通。
案例中阿里巴巴就是目标对象 Subject ，联系方式列表就是用来维护观察者的 observerList ，根据前端职位的有无来调用 notify 方法。

发布订阅模式
发布订阅模式：基于一个事件（主题）通道，希望接收通知的对象  Subscriber  通过自定义事件订阅主题，被激活事件的对象  Publisher  通过发布主题事件的方式通知各个订阅该主题的  Subscriber 对象。
因此发布订阅模式与观察者模式相比，发布订阅模式中有三个角色：发布者 Publisher，事件调度中心 Event Channel，订阅者Subscriber。

宗门任务大殿: 任务发布者 —— Publisher
中介功能 —— Event Channel
维护任务类型，以及每种任务下的订阅情况
给订阅者提供订阅功能 —— subscribe 功能
当宗门发布任务后，中介会给所有的订阅者发布任务 —— publish 功能
弟子: 任务接受者 —— Subscriber

再给大家举个例子: 以目前的热播剧开端为例，临近过年，摸鱼的心思越来越重，每天就迫不及待的等开端更新，想在开端更新的第一刻就开始看剧，那你会怎么做那？总不能时时刻刻刷新页面吧。
平台提供了消息订阅功能，如果你选择订阅，平台更新开端后，会第一时间发消息通知你，
订阅后，你就可以愉快的追剧了。
上面案例中：开端就是发布者 Publisher，追剧人就是订阅者 Subscribe，平台则承担了事件通道 
Event Channel 功能。
class PubSub {
    constructor() {
        // 事件中心
        // 存储格式: warTask: [], routeTask: []
        // 每种事件(任务)下存放其订阅者的回调函数
        this.events = {}
    }
    // 订阅方法
    subscribe(type, cb) {
        if (!this.events[type]) {
            this.events[type] = [];
        }
        this.events[type].push(cb);
    }
    // 发布方法
    publish(type, ...args) {
        if (this.events[type]) {
            this.events[type].forEach(cb => cb(...args))
        }
    }
    // 取消订阅方法
    unsubscribe(type, cb) {
        if (this.events[type]) {
            const cbIndex = this.events[type].findIndex(e=> e === cb)
            if (cbIndex != -1) {
                this.events[type].splice(cbIndex, 1);
            }
        }
        if (this.events[type].length === 0) {
            delete this.events[type];
        }
    }
    unsubscribeAll(type) {
        if (this.events[type]) {
            delete this.events[type];
        }
    }
}

// 创建一个中介公司
let pubsub = new PubSub();

// 弟子一订阅战斗任务
pubsub.subscribe('warTask', function (taskInfo){
    console.log("宗门殿发布战斗任务，任务信息:" + taskInfo);
})
// 弟子一订阅战斗任务
pubsub.subscribe('routeTask', function (taskInfo) {
    console.log("宗门殿发布日常任务，任务信息:" + taskInfo);
});
// 弟子三订阅全类型任务
pubsub.subscribe('allTask', function (taskInfo) {
    console.log("宗门殿发布五星任务，任务信息:" + taskInfo);
});

// 发布战斗任务
pubsub.publish('warTask', "猎杀时刻");
pubsub.publish('allTask', "猎杀时刻");

// 发布日常任务
pubsub.publish('routeTask', "种树浇水");
pubsub.publish('allTask', "种树浇水");
输出结果:
// 战斗任务
宗门殿发布战斗任务，任务信息:猎杀时刻
宗门殿发布五星任务，任务信息:猎杀时刻
// 日常任务
宗门殿发布日常任务，任务信息:种树浇水
宗门殿发布五星任务，任务信息:种树浇水
通过输出结果，我们可以发现发布者和订阅者不知道对方的存在。需要第三方中介，将订阅者和发布者串联起来，利用中介过滤和分配所有输入的消息。也就是说，「发布-订阅模式用来处理不同系统组件的信息交流，即使这些组件不知道对方的存在」。

 总结
上文中提到了观察者模式和发布订阅模式，我们来总结一下两者差异:



vue diff算法（虚拟dom、真实dom）
https://blog.csdn.net/weixin_43638968/article/details/112686317
https://blog.csdn.net/weixin_52998620/article/details/122804146

diff算法就是进行虚拟节点对比，并返回一个patch对象，用来存储两个节点不同的地方，最后用patch记录的消息去局部更新DOM。

其有两个特点：
比较只会在同层级进行，不会跨层级比较
在diff比较的过程中，循环从两边向中间比较
diff算法在很多场景下都有应用，在vue中，作用于虚拟DOM渲染成真实DOM的新旧VNode


Diff算法的步骤：
用JS对象结构表示DOM树的结构，然后用这个树构建一个真正的DOM树，插到文档当中
当状态变更的时候，重新构造一颗新的对象树。然后用新的树和旧的树进行比较（diff），记录两棵树差异
把第二棵树所记录的差异应用到第一棵树所构建的真正的DOM树上（patch），视图就更新了

比较方式：diff整体策略为：深度优先，同层比较
比较只会在同层级进行，不会跨层级比较


比较的过程中，循环从两边向中间收拢


原理分析
当数据发生改变时，set方法会调用Dep.notify通知所有订阅者Watcher，订阅者就会调用patch给真实的DOM打补丁，更新相应的视图。

patch函数前两个参数位为oldVnode和Vnode，分别代表新的节点和之前的旧节点，主要做了四个判断：
没有新节点，直接触发旧节点的destory钩子
没有旧节点，说明是页面刚开始初始化的时候，此时，根本不需要比较了，直接全是新建，所以只调用createElm
旧节点和新节点自身一样，通过sameVnode判断节点是否一样，一样时，直接调用patchVnode去处理这两个节点
旧节点和新节点自身不一样，当两个节点不一样的时候，直接创建新节点，删除旧节点。

patchVnode主要做了几个判断：
新节点是否是文本节点，如果是，则直接更新DOM的文本内容为新节点的文本内容
新节点和旧节点如果都有子节点，则处理比较更新子节点
只有新节点有子节点，旧节点没有，那么不用比较了，所有节点都是全新的，所以直接全部新建就好了，新建是指创建出所有新DOM，并且添加进父节点
只有旧节点有子节点而新节点没有，说明更新后的页面旧节点全部都不见了，那么要做的就是把所有的旧节点删除，也就是直接把DOM删除，子节点不完全一致，则调用updateChildren

while循环主要处理了以下五种情景：
当新老VNode节点的start相同时，直接patchVnode，同时新老VNode节点的开始索引都加1
当新老VNode节点的end相同时，同样直接patchVnode，同时新老VNode节点的结束索引都减1
当老VNode节点的start和新VNode节点的end相同时，这时候在patchVnode后，还需要将当前真是dom节点移动到oldEndVnode的后面，同时老VNode节点开始索引加1，新VNode节点的结束索引减1
当老VNode节点的end和新VNode节点的start相同时，这时候在patchVnode后，还需要将当前真实dom节点移动到oldStartVnode的前面，同时老VNode节点结束索引减1，新VNode节点的开始索引加1
如果都不满足以上四种情形，那说明没有相同的节点可以复用，则会分为以下两种情况：
从旧的VNode为key值，对应index序列为value值的哈希表中找到与newStartVnode一致key的旧的VNode节点，再进行patchVnode，同时将这个真实dom移动到oldStartVnode对应的真实dom的前面
调用createElm创建一个新的dom节点放到当前newStartIndex的位置

小结：
当数据发生改变时，订阅者watcher就会调用patch给真实的DOM打补丁
通过isSameVnode进行判断，相同则调用patchVnode方法
patchVnode做了以下操作：
找到对应的真实dom，称为el
如果都有文本节点且不相等，将el文本节点设置为Vnode的文本节点
如果oldVnode有子节点而VNode没有，则删除el子节点
如果oldVnode没有子节点而VNode有，则将VNode的子节点真实化后添加到el
如果两者都有子节点，则执行updateChildren函数比较子节点
updateChildren主要做了以下操作：
设置新旧VNode的头尾指针
新旧头尾指针进行比较，循环向中间靠拢，根据情况调用patchVnode进行patch重复流程、调用createElem创建一个新节点，从哈希表寻找key一致的VNode节点再分情况操作

vue v-for中key的作用
https://juejin.cn/post/7058929425156407327
https://blog.csdn.net/qq_32766999/article/details/123421076
key的特殊attribute主要用在Vue的虚拟DOM算法，在新旧nodes对比时辨识VNodes。如果不使用key，Vue会使用一种最大限度减少动态元素并且尽可能的尝试就地修改/复用相同类型元素的算法。而使用key时，它会基于key的变化重新排列元素顺序，并且会移除key不存在的元素。有相同父元素的子元素必须有独特的key。重复的key会造成渲染错误。

vue3.0的vuex与pinia
pinia：
pinia合并了mutation和action，包括异步
无需通过mutation修改state，store.count++可以直接修改状态
特点：
完整的typescript支持
足够轻量，压缩后的体积只有1.6kb
去除mutations，只保留state，getters，actions
actions同时支持同步和异步
没有modules模块的概念，只有store，store之间可以相互引用，更好的代码分割
vuex：
mutations中必须时同步函数
Action类似mutation，区别是action提交mutation，且action可以异步

Echarts修改默认样式

configureWebpack、chainWebpack
https://cli.vuejs.org/zh/config/#configurewebpack
https://www.cnblogs.com/chuanmin/p/15838988.html
configureWebpack与chainWebpack的作用相同，唯一区别就是它们修改webpack配置方式不同：
configureWebpack
Type：object | Function
如果这个值是一个对象，则会通过webpack-merge合并到最终的配置中。
如果这个值是一个函数，则会接收被解析的配置作为参数。该函数既可以修改配置并不返回任何东西，也可以返回一个被克隆或合并过的配置版本。
chainWebpack
Type：Function
是一个函数，会接收一个基于webpack-chain的 ChainableConfig实例。允许对内部的webpack配置进行更细粒度的修改。

configureWebpack通过操作对象的形式来修改默认的webpack配置，该对象将会把webpack-merge合并入最终的webpack配置
chainWebpack通过链式编程的形式来修改默认的webpack配置

MVVM框架的原理
http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html
https://www.cnblogs.com/iovec/p/7840228.html
一. 什么是MVVM框架？
MVVM是Model-View-ViewModel的简写，双向数据绑定，即视图影响模型，模型影响数据。它本质上就是MVC的改进版。
Model（数据模型） 泛指后端进行的各种业务逻辑处理和数据操控，主要围绕数据库系统展开。例如后台接口传递的数据
View（视图层） 也就是用户界面。前端主要由HTML和CSS来构建，为了更方便地展现ViewModel 或者 Model层的数据，已经产生了各种各样的前后端模板语言（FreeMarker、Marko、Pug、Jinja2等），各大MVVM框架（KnockoutJS、Vue、Angular等）都有自己用来构建用户界面的内置模板语言。
ViewModel （视图数据层）是由前端开发人员组织生成和维护的视图数据层。在这一层，前端开发者对从后端获取的Model数据进行转换处理，做二次封装，以生成符合View层使用预期的视图数据模型。
需要注意的是：
ViewModel所封装出来的数据模型包括图的状态和行为两部分，而Model层的数据模型是只包含状态。
视图状态和行为都封装在ViewModel里，这样的封装使得ViewModel可以完整的去描述View层。
由于实现了双向绑定，ViewModel的内容会实时展现在View层，前端开发者再也不必低效又麻烦地通过操作DOM去更新视图，MVVM框架已经把最脏最累的一块做好了，我们开发者只需要处理和维护ViewModel，更新数据视图就会自动得到相应更新，真正实现数据驱动开发。
View层展现的是ViewModel，由ViewModel负责与Model层交互，这就完全解耦了View层和Model层，这个解耦至关重要，它是前后端分离方案实施的重要一环。
MVVM其核心是数据驱动视图，即实现View和ViewModel的双向数据绑定，使得ViewModel的状态改变可以自动传递给View，即数据双向绑定。
二. Vue中MVVM


MVVM的核心是ViewModel层，它就像是一个中转站，负责转换Model中的数据对象来让数据变得更容易管理和使用，该层向上与视图层进行双向数据绑定，向下与Model层通过接口请求进行数据交互，起承上启下作用。
MVVM框架有Vue，Angular等。
组成部分：
简单画了一张图来说明MVVM的各个组成部分：

分层设计一直是软件架构的主流设计思想之一，MVVM也不例外。

Vue 通过数据劫持 + 发布-订阅模式的方式实现双向数据绑定，通过ES5提供的 Object.defineProperty() 方法来劫持各属性 getter、setter，并在数据（对象）发生变动时通知订阅者，触发相应的监听回调函数。
可以更加高效的操作DOM更新视图。
三. MVVM优点
MVVM和MVC模式一样，主要目的是分离视图和模型，其优点包括：
低耦合
可重用
独立开发
可测试

vue中如何获取dom元素
原生js操作dom元素
1. 给相应的dom元素加id，使用“document.getElementById("id")”语句获取该元素
vue：ref
2. 给相应的dom元素加“ref="name"”，使用“this.$refs.name”获取该元素

$nextTick
https://zhuanlan.zhihu.com/p/396831673
nextTick是什么？
nextTick本质就是执行延迟回调的钩子，接受一个回调函数作为参数，在下次DOM更新循环结束之后执行延迟回调。在修改数据之后立即使用这个方法，获取更新后的DOM。Vue2.1.0开始，如果没有提供回调函数，且在支持Promise的环境中，则返回一个Promise。注意Vue本身不是自带polyfill的，如果环境不支持Promise，则需要自己提供polyfill。

nextTick的作用
说起 nextTick ，也不得不说说 Vue 的异步更新，Vue 在更新 DOM 时是异步执行的。只要侦听到数据变化，Vue 将开启一个队列，并缓冲在同一事件循环中发生的所有数据变更。如果同一个 watcher 被多次触发，只会被推入到队列中一次。这种在缓冲时去除重复数据对于避免不必要的计算和 DOM 操作是非常重要的。然后，在下一个的事件循环“tick”中，Vue 刷新队列并执行实际 (已去重的) 工作。Vue（2.6.x） 在内部对异步队列尝试使用原生的 
Promise.then、
MutationObserver 和 
setImmediate，如果执行环境不支持，则会采用 
setTimeout(fn, 0) 代替。
例如：当你设置vm.someData = 'new value'，该组件不会立即重新渲染。当刷新队列时，组件会在下一个事件循环“tick”中更新。多数情况我们不需要关心这个过程，但是如果你想基于更新后的DOM状态来做点什么，这就可能会有些棘手。虽然Vue.js通常鼓励开发人员使用“数据驱动”的方式思考，避免直接接触DOM，但是有时我们必须要这么做。为了在数据变化之后等待Vue完成更新DOM，可以在数据变化之后立即使用Vue.nextTick(callback)。这样回调函数将在DOM更新完成后被调用。
nextTick除了让我们可以在DOM更新之后执行延迟回调，还有一个作用就是Vue内部使用nextTick，把渲染DOM操作这个操作放入callbacks中。

Event Loop
console.log('同步代码1');
setTimeout(() => {
    console.log('setTimeout')
}, 0)
new Promise((resolve) => {
  console.log('同步代码2')
  resolve()
}).then(() => {
    console.log('promise.then')
})
console.log('同步代码3');
// 最终输出"同步代码1"、"同步代码2"、"同步代码3"、"promise.then"、"setTimeout"

nextTick 是下次 DOM 更新循环结束后执行延迟回调。

nextTick原理
nexttick的原理：利用Event loop事件线程去异步操作。本质上就是注册异步任务来对任务进行处理。

Event loop（事件循环机制）
https://www.iteye.com/news/32777
单线程的JavaScript
JS是单线程的，单线程是指：在JS引擎中负责解释和执行JS代码的线程只有一个。JS运行在浏览器中，是单线程的，每个window一个JS线程。
为什么是单线程？
减轻cpu的压力

其他类线程（任务队列）：ajax请求、监控用户事件、定时器、读写文件的线程（例如在NodeJS中）等等。这些我们称之为异步事件，当异步事件发生时，将它们放入执行队列，等待当前代码执行完成。就不会长时间阻塞主线程。等主线程的代码执行完毕，然后再读取任务队列，返回主线程继续处理。如此循环这就是事件循环机制。
总结一下：
我们可以认为某个同域浏览器上下文中JavaScript只有一个主线程、函数调用栈以及多个任务队列。
主线程会依次执行代码，当遇到函数时，会先将函数入栈，函数运行完毕后再将该函数出栈，直到所有代码执行完毕。
当函数调用栈为空时，即会根据事件循环（Event Loop）机制来从任务队列中提取出待执行的回调并执行，执行的过程同样会利用函数栈。
所有同属一个的窗体都共享一个事件循环，所以它们可以同步交流。不同窗体之间相互独立，互不干扰。

事件循环
JavaScript代码的执行过程中，除了依靠函数调用栈来搞定函数的执行顺序外，还依靠任务队列（task queue）来搞定另外一些代码的执行。
根据上面的分析，任务队列的特点是先进先出。

一个js文件里事件循环只有一个，但是任务队列可以有多个。任务队列又可以分为macro-task(task) 与micro-task(job)。

macro-task(task) 包括：
setTimeout / setInterval
setImmediate
I/O操作
UI rendering
micro-task(job)包括：
process.nextTick
Promise
Object.observe(已废弃)
MutationObserve(html5新特性)
浏览器中新标准中的事件循环机制与nodejs类似，其中会介绍到几个nodejs有，但是浏览器中没有的API，大家只需要了解就好。比如process.nextTick，setImmediate
我们称他们为事件源，事件源作为任务分发器，他们的回调函数才是被分发到任务队列，而本身会立即执行。
例如，setTimeout第一个参数被分发到任务队列，Promise的then方法的回调函数被分发到任务队列（catch方法同理）。
不同源的事件被分发到不同的任务队列，其中setTimeout和setInterval属于同源
整体代码开始第一次循环。全局上下文进入函数调用栈。直到调用栈清空（只剩全局），然后执行所有的job。当所有可执行的job执行完毕之后。循环再次从task开始，找到其中一个任务队列执行完毕，然后再执行所有的job，这样一直循环下去。
无论是task还是job，都是通过函数调用栈来完成。
这个时候我们是不是有一个大发现，除了首次整体代码的执行，其他的都有规律，先执行task任务队列，再执行所有的job并清空job队列。再执行task--job--task--job .......，往复循环直到没有可执行代码。
那我们可不可以这么理解，第一次script代码的执行也算是一个task任务呢，如果这么理解那整个事件循环就很容易理解了。



JS中setTimeout、promise、async、await的执行顺序
https://blog.csdn.net/tiven_/article/details/126135848
Javascript是单线程语言，也就是说，同一个时间只能做一件事。这就意味着，所有任务需要排队，前一个任务结束，才会执行后一个任务。如果前一个任务耗时很长，后一个任务就不得不一直等着。
因为任务有同步与异步之分，所以不同任务的执行顺序必定有一定的顺序。

Event Loop（事件循环）
所有任务可以分成两种：
同步任务（synchronous）:  在主线程上排队执行的任务，只有前一个任务执行完毕，才能执行后一个任务。
异步任务（asyncchronous）:  不进入主线程、而进入任务队列（task queue）的任务，只有任务队列通知主线程，某个异步任务可以执行了该任务才会进入主线程执行。
异步执行的运行机制：（同步执行也是如此，因为它可以被视为没有异步任务的异步执行。）
所有同步任务都在主线程上执行，形成一个执行栈（execution context stack）。
主线程外，还存在一个任务队列（task queue）。只要异步任务有了运行结果，就在任务队列之中放置一个事件。
一旦“执行栈”中的所有同步任务执行完毕，系统就会读取任务队列，看看里面有哪些事件。哪些对应的异步任务，于是结束等待状态，进入执行栈，开始执行。
主线程不断重复上面的第三步。
定义：主线程循环不断的从任务队列中读取事件（任务），这整个过程就称为Event Loop（事件循环）。

JavaScript事件
概述：任务队列是一个事件的队列（也可以理解成消息的队列），IO设备完成一项任务，就在任务队列中添加一个事件，表示相关的异步任务可以进入执行栈了。主线程读取任务队列，就是读取里面有哪些事件。
JavaScript的事件分两种：宏任务和微任务
宏任务 ： 从上到下、从左到右、顺序执行的script代码，setTimeout，setInterval，setImmediate（node环境）
微任务 ： Promise.then(非new Promise)，async/await整体，process.nextTick(node环境)
其他异步任务：
requestAnimationFrame(callback)-RAF仅仅存在于浏览器环境，执行时机在setTimeout 之前执行
queueMicrotask: 执行时机在第一轮同步任务执行完成之后，微任务执行之前。
setTimeOut
setTimeOut执行需要满足两个条件：
主进程必须是空闲的状态，如果到时间了，主进程不空闲也不会执行你的回调函数
这个回调函数需要等到插入异步队列时前面的异步函数都执行完了，才会执行。
注意：setTimeOut并不是直接的把回调回那火速放进异步队列中，而是在定时器的时间到了之后，把回调函数放到异步队列中去。如果此时这个队列已经有很多任务了，那就排在他们的后面。这也就解释了为什么setTimeOut为什么不能精准的执行的问题了。

promise、 async / await
new Promise 是同步的任务，会被放到主线程中去立即执行。
.then() 函数是异步任务会房贷异步队列中去，具体就是当promise状态结束（fulfilled）的时候，会立即放进异步队列中去。
带async 关键字的函数会返回一个promise对象，如果里面没有await，执行起来等同于普通函数
await 关键字要在async关键字函数的内部，await写在外面会报错。await如同它的语意，就是在等待，等待右侧的表达式完成。
await会让出线程，阻塞async内后续的代码，先去执行async外的代码。等外面的同步代码执行完毕，才会执行里面的后续代码。就算await的不是promise对象，是一个同步函数，也会同样执行。

执行顺序（总结）：
宏任务（从上到下、从左到右的整体）
微任务的Event Queue(Promise.then，async / await整体，process.nextTick【node环境】)
宏任务的Event Queue(setTimeout / setInterval / setImmediate【node环境】)
同一轮微任务队列中，依次顺序执行 process.nextTick、queueMicrotask、Promise.then 和 async / await
同一轮宏任务队列中， setTmmediate 在 setTimeout之后执行
在浏览器环境同一轮任务队列中，requestAnimationFrame 在 setTimeout 之前执行

总结：
script
process.nextTick(node环境)
queueMicrotask
promise.then / async / await
requestAnimationFrame(浏览器环境)
setTimeout
setImmediate(node环境)


宏任务与微任务
https://juejin.cn/post/6958661915149074463
一. 为什么js是单线程的？
JavaScript的单线程，与它的用途有关。
作为浏览器脚本语言，JavaScript的主要用途是与用户互动，以及操作DOM。
如果js不是单线程，会带来很复杂的同步问题（比如：假定JS同时有两个线程，一个线程在某个DOM节点上添加内容，另一个线程删除了这个节点，这时浏览器应该以哪个线程为准？为了避免复杂性，从一诞生，JS就是单线程）
二. 任务队列
单线程就意味着，所有任务需要排队，按序执行。
但是作为脚本语言，在运行的时候，语言设计人员需要考虑的两件重要的事情，就是执行的实时性和效率。
实时性：指在代码执行过程中，代码执行的实效性，当前执行语句任务是否在当前实效下发挥作用。
效率：指的是代码执行过程中，每个语句执行的造成后续执行的延迟率。
任务分两种：一种是同步任务，另一种是异步任务。

同步任务
在主线程上排队执行的任务，只有当前一个任务执行完毕，才能执行后一个任务。
在一个函数返回的时候，调用者就能够得到预期结果（即拿到了预期的返回值或者看到了预期的效果），那么这个函数就是同步的。
异步任务
不进入主线程而进入任务队列的任务。
只有任务队列通知主线程，某个异步任务可以执行了，该任务才会进入主线程执行。
在函数返回的时候，调用者还不能够得到预期结果，而是需要在将来通过一定的手段得到，那么这个函数就是异步的。

 三. 宏任务和微任务
宏任务是什么？
任何按标准机制调度进行执行的JavaScript代码都是任务。
执行一段程序、执行一个事件回调或interval/timerout触发，这些都在任务队列上被调度。
常见宏任务（包括整体代码script，setTimeout，setInterval，setImmediate）
微任务是什么？
当一个任务存在，事件循环都会检查该任务是否正把控制权交给其他JavaScript代码。
如果不交予执行，事件循环就会运行微任务队列中的所有微任务。
接下来微任务循环会在事件循环的每次迭代中被处理多次，包括处理完事件和其他回调之后。
其次，如果一个微任务通过调用queueMicrotask()，向队列中加入了更多的微任务，则那些新加入的微任务会早于下一个任务运行。
微任务必须是一个异步的执行的任务，这个执行的时间需要在主函数执行之后，也就是微任务建立的函数执行后，而又需要在当前宏任务结束之前。
常见微任务（Promise，Object.observe，MutationObserver，Node.js环境下的process.nextTick，async/await）。

执行流程
整段脚本script作为宏任务开始执行
遇到微任务将其推入微任务队列，宏任务推入宏任务队列
宏任务执行完毕，检查有没有可执行的微任务
发现有可执行的微任务，将所有微任务执行完毕
当前宏任务执行完毕，开始检查渲染，然后GUI线程接管渲染
渲染完毕后，JS线程继续接管，开始新的宏任务，反复如此直到所有任务执行完毕

四. 实战
console.log('global')

for (var i = 1;i <= 5;i ++) {
  setTimeout(function() {
    console.log(i)
  },i*1000)
  console.log(i)
}

new Promise(function (resolve) {
  console.log('promise1')
  resolve()
 }).then(function () {
  console.log('then1')
})

setTimeout(function () {
  console.log('timeout2')
  new Promise(function (resolve) {
    console.log('timeout2_promise')
    resolve()
  }).then(function () {
    console.log('timeout2_then')
  })
}, 1000)

// 第一步，将全局上下文，即整段script代码压入调用栈，作为宏任务开始执行

// 遇到同步任务console,直接执行，打印'global'
// for循环遍历五次，每一次触发一个timeout宏任务和一个同步任务console,
// 将每次遍历触发的宏任务推入宏任务队列，同步任务console,直接执行，打印i
// 这时宏任务队列有5个timeout宏任务
// 控制台按序打印'global'，1，2，3，4，5

// 遇到promise,注意Promise.then里的才是微任务
// 遇到同步任务 console.log('promise1')，直接执行，打印'promise1'
// 将微任务Promise.then推入微任务队列
// 控制台按序打印'global'，1，2，3，4，5，'promise1'

// 遇到Timeout，触发宏任务，将其推入宏任务队列

// 这时第一个宏任务，即整段script代码快要执行完了，需要检查微任务队列
// 微任务队列里有Promise.then，将其执行，打印'then1'
// 第一个宏任务执行完后的控制台：'global'，1，2，3，4，5，'promise1'，'then1'

// 第二步，执行第二个宏任务
// 将for循环产生的第一个宏任务Timeout执行，打印'6'，这时微任务队列为空，直接执行下一个宏任务
// 注意，由于这时宏任务队列中接下来的4个宏任务都是6秒后才触发
// 而第五个宏任务1秒后便触发了，这时浏览器会先执行第五个宏任务

// 先执行第五个宏任务，触发同步任务console.log('timeout2')和  console.log('timeout2_promise')
// 按序打印'timeout2'，'timeout2_promise'
// 触发微任务Promise.then，将其推入微任务队列。
// 这时该宏任务快执行完了，便检查微任务队列，将Promise.then执行，打印'timeout2_then'
// 控制台按序打印'global'，1，2，3，4，5，'promise1'，'then1'，'timeout2'，'timeout2_promise'

// 这时按序执行剩余四个宏任务Timeout
// 最终控制台打印'global'，1，2，3，4，5，'promise1'，'then1'，'timeout2'，'timeout2_promise'，6，6，6，6

function taskOne() {
    console.log('task one ...')
    setTimeout(() => {
        Promise.resolve().then(() => {
            console.log('task one micro in macro ...')
        })
        setTimeout(() => {
            console.log('task one macro ...')
        }, 0)
    }, 0)
    taskTwo()
}

function taskTwo() {
    console.log('task two ...')
    Promise.resolve().then(() => {
        setTimeout(() => {
            console.log('task two macro in micro...')
        }, 0)
    })

    setTimeout(() => {
        console.log('task two macro ...')
    }, 0)
}

setTimeout(() => {
    console.log('running macro ...')
}, 0)

taskOne()

Promise.resolve().then(() => {
    console.log('running micro ...')
})

// 这里注意要先将全局上下文压入调用栈
// 遇到函数调用也要压入调用栈
// 从调用栈开始取出执行
// 或者也可以理解为遇到调用就立即执行

// task one ...
// task two ...
// running micro ...
// running macro ...
// task one micro in macro ...
// task two macro ...
// task two macro in micro...
// task one macro ...

https://www.jianshu.com/p/ada97f33b86e
async function async1(){
    cosole.log("async start");
    await async2();
    console.log("async1 end");
}
async function async2(){
    console.log("async2")
}
console.log("script start")

setTimeout(function(){
    console.log("setTimeout")
},0)

async1();

new Promise(function(resolve){
    console.log("promise1")
    resolve()
}).then(function(){
    console.log("promise2")
})

console.log("script end2")
// 1. script start
// 2. async start
// 3. async2
// 4. promise1
// 5. script end2
// 6. async1 end
// 7. promise2
// 8. setTimeout


堆和栈的区别
内存操作场景 
（1）内存操作场景下，堆与栈表示两种内存的管理方式。
（2）数据结构场景下，堆与栈表示两种常用的数据结构。
栈由操作系统自动分配和释放，用于存放简单的数据段，占据固定大小的空间，比如基本数据类型（Number、String、Boolean，Null，Undefined）和函数的参数值等。
堆是由开发人员自主分配和释放，若不主动释放，程序结束时由浏览器回收，用于存储引用类型（引用类型的变量实际上保存的不是变量本身，而是指向内存空间的指针）。
JavaScript中的数据类型
数据结构场景
JavaScript存在栈和队列概念，通过数组的方式，模仿实现堆栈。
栈：栈是一种运算受限的线性表，其限制是指只仅允许在表的一端进行插入和删除操作，这一端被称为栈顶，相对的，把另一端称为栈底。把新元素放到栈顶元素的上面，使之成为新的栈顶元素称作进栈、入栈或压栈；把栈顶元素删除，使其相邻的元素成为新的栈顶元素称作出栈或退栈。通过数组的push()、pop()方法实现栈。
堆：堆其实是一种优先队列，也就是说队列中存在优先级，比如队列中有很多待执行任务，执行时会根据优先级找优先级度最高的先执行。JavaScript堆的实现方式

js中的数据类型分为基本数据类型和引用数据类型。基本数据类型存在栈内存中，引用数据类型存在堆内存中。但是引用类型的引用还是存在栈内存中的。
栈：先进后出
栈（stack）会自动分配内存空间，会自动释放。栈内存是内存中用于存放临时变量的一片内存块。当声明一个基本变量时，它就会被存储到栈内存中。
特点：存取速度快，但不灵活，同时由于结构简单，在变量使用完成后就可以将其释放，内存回收容易实现。
堆：
堆（heap）动态分配的内存，值大小不一定，也不会自动释放。
特点：使用灵活，可以动态增加或删除空间，但是存取比较慢。

浏览器渲染过程
浏览器的渲染过程共分为几个过程：
JavaScript ---->Style ---->Layout ---->Paint ---->Composite


Layout阶段
计算DOM节点的最终样式，生成Layout tree，这棵树类似DOM树，树中记录了参与页面的布局以及样式，节点的最终布局尺寸以及位置。

浏览器计算样式的步骤：
首先浏览器会遍历一遍DOM，然后在CSSOM（CSS Object Model）中查找对应元素匹配的样式，找到对应的元素的样式定义的时候，接着进行CSS选择器优先排序，得到对应元素最终计算后的样式，以类ComputedStyle体现出来。
DOM遍历完之后，就会得到一个新的树，就是Layout阶段的Layout tree，这棵树虽然是从DOM树中构建而来，但并不是建立在DOM树上，也就是Layout tree 有自己的根节点和孩子节点。
在W3C标准中，CSSOM包含两部分：
Model：描述样式表和规则的模型部分
View：和元素视图相关的API部分

Paint阶段
该阶段会遍历Layout tree中的每个节点，根据节点布局方式和内容，调用节点的业务逻辑（比如：绘制Rect、Border、Text等），这些绘制结果以draw commands的形式保存下来。
使用devtool查看渲染

蓝色的虚线之前表示触发了浏览器的DomContentLoaded事件，表示浏览器已经完成了对页面的解析工作，它对应的Main（JS线程）在这之前完成了对HTML的解析工作，该过程也就是ParseHTML阶段。
render树
html的dom树 + css style生成了render树

V8引擎解析js代码
在解析js代码的过程中，主要经历三个过程，1. 通过parser解析器生成AST抽象语法树  2. 通过interpreter将AST抽象语法树解析成机器能够识别的字节码  3. 通过compiler编译器编译代码

Vue的优势与缺点
vue两大特点：响应式编程、组件化。
vue的优势：轻量级框架、简单易学、双向数据绑定、组件化、数据和结构分离、虚拟DOM、运行速度快、插件化。
vue是单页面应用，使页面局部刷新，不用每次跳转页面都请求所有数据和dom，这样大大加快了访问速度和提升用户体验。而且它的第三方UI库节省了很多开发时间。
缺点：
不支持IE8以下
单页面应用，不利于seo优化
初次加载耗时多

常见Jquery面试问题
http://www.muzhuangnet.com/show/54096.html




