# Hello World

[ECMA-262 - Ecma International](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)、[Web 开发技术 | MDN](https://developer.mozilla.org/zh-CN/docs/Web)、[现代 JavaScript 教程](https://zh.javascript.info/)

## JavaScript 实现

1995 年，网景公司工程师Brendan Eich，为即将发布的 Netscape Navigator 2 开发 Mocha（后改名为 LiveScript）的脚本语言。当时计划在客户端和服务器端都使用它，在服务器端叫 LiveWire。网景与 Sun 公司结为开发联盟，共同开发 LiveScript。在 Netscape Navigator 2 正式发布前，网景把 LiveScript 改名为 JavaScript（以便搭上 Java 的顺风车）。

JavaScript 1.0 很成功，在 Netscape Navigator 3 中发布了 1.1 版本。网景稳居市场领导者的位置。这时，微软向 IE 投入了更多资源。就在 Netscape Navigator 3 发布后不久，微软发布了 IE3，其中包含名为 JScript（叫这个名字是为了避免与网景发生许可纠纷）的 JavaScript 实现。1996 年 8 月，微软进入 Web 浏览器领域，微软的 JavaScript 实现意味着出现了两个版本的 JavaScript：Netscape Navigator 中的 JavaScript，以及 IE 中的 JScript。此时 JavaScript 还没有规范其语法或特性的标准，两个版本并存让这个问题更加突出了。

1997 年，JavaScript 1.1 作为提案被提交给欧洲计算机制造商协会（Ecma）。第 39 技术委员会（TC39）承担了“标准化一门通用、跨平台、厂商中立的脚本语言的语法和语义”的任务。TC39 委员会由来自网景、Sun、微软、Borland、Nombas 和其他对这门脚本语言有兴趣的工程师组成。他们花了数月时间打造出 ECMA-262，也就是 ECMAScript（发音“ek-ma-script”）这个新的脚本语言标准。1998 年，国际标准化组织（ISO）和国际电工委员会（IEC）也将 ECMAScript 采纳为标准（ISO/ IEC-16262）。此后，各家浏览器均以 ECMAScript 作为自己 JavaScript 实现的依据，虽然具体实现各有不同。

![img](E:\HelloWorld\学习资料\md\assets\1680530475780-bba031ae-c0f1-4101-aa27-387c85815a7a.png)

### ECMAScript

ECMAScript，即 ECMA-262 定义的语言，并不局限于 Web 浏览器。ECMAScript没有输入和输出之类的方法。ECMA-262 将这门语言作为一个基准来定义，以便在它之上再构建更稳健的脚本语言。Web 浏览器只是 ECMAScript 实现可能存在的一种宿主环境（host environment）。宿主环境提供ECMAScript 的基准实现和与环境自身交互必需的扩展。扩展（比如 DOM）使用 ECMAScript 核心类型和语法，提供特定于环境的额外功能。其他宿主环境还有服务器端 JavaScript 平台 Node.js 和即将被淘汰的 Adobe Flash。

如果不涉及浏览器的话，ECMA-262 在基本的层面，描述这门语言的如下部分： 语法、类型、语句、关键字、保留字、操作符、全局对象 。

ECMAScript 只是对实现这个规范描述的所有方面的一门语言的称呼。JavaScript 实现了 ECMAScript，而 Adobe ActionScript 同样也实现了 ECMAScript。



**ECMA-262 第 1 版**本质上跟网景的 JavaScript 1.1 相同， 只不过删除了所有浏览器特定的代码，外加少量的修改。ECMA-262 要求支持 Unicode 标准（以支持多语言），而且对象要与平台无关（Netscape JavaScript 1.1 的对象不是这样，如它的 Date 对象就依 赖平台）。

**ECMA-262 第 2 版**只是做了一些编校工作，主要是为了更新之后严格符合 ISO/IEC-16262 的要求。这也是 JavaScript 1.1 和 JavaScript 1.2 不符合 ECMA-262 第 1 版要求的原因。 

**ECMA-262 第 3 版**第一次真正对这个标准进行更新，更新了字符串处理、错误定义和数值输出。增加了对正则表达式、新的控制语句、try/catch 异常处理的支持，以及为了更好地让标准国际化所做的少量修改。

**ECMA-262 第 4 版**是对这门语言的一次彻底修订。以满足全球 Web 开发日益增长的需求。几乎在第 3 版基础上完全定义了一门新语言。括强类型变量、新语句和数据结构、真正的类和继承，及操作数据的新手段。与此同时，TC39 委员会的一个子委员会也提出了另外一份提案，叫作“ECMAScript 3.1”，只对这门语言进行了较少的改进。这个子委员会的人认为第 4 版对这门语言来说跳跃太大了。因此，他们提出 了一个改动较小的提案，只要在现有 JavaScript 引擎基础上做一些增改就可以实现。最终，ES3.1 子委员 会赢得了 TC39 委员会的支持，ECMA-262 第 4 版在正式发布之前被放弃。 

ECMAScript 3.1 变成了 **ECMA-262 第 5 版**，于 2009 年 12 月 3 日正式发布（ES5）。第 5 版致力于厘清第 3 版存在的歧义，也增加了包括原生的解析和序列化 JSON 数据的 JSON 对象、方便继承和高级属性定义的方法，以及新的增强 ECMAScript 引擎解释和执行代码能力的严格模式。第 5 版 在 2011 年 6 月发布了一个维护性修订版，这个修订版只更正了规范中的错误，并未增加任何新的语言或库特性。 

**ECMA-262 第 6 版**，俗称 ES6、ES2015 或 ES Harmony（和谐版），于 2015 年 6 月发布。包含了大概这个规范有史以来最重要的一批增强特性。ES6 正式支持了类、模块、迭代器、生成器、箭头函数、期约、反射、代理和众多新的数据类型。 

...

## DOM

文档对象模型（DOM，**Document Object Model**）是一个应用编程接口（API），用于在 HTML 中使用扩展的 XML。DOM 将整个页面抽象为一组分层节点。HTML 或 XML 页面的每个组成部分都是一种节点，包含不同的数据。

## BOM

IE3 和 Netscape Navigator 3 提供了浏览器对象模型（BOM） API，用于支持访问和操作浏览器的窗口。使用 BOM可以操控浏览器显示页面之外的部分。它是唯一一个没有相关标准的 JavaScript 实现。HTML5 改变了这个局面，这个版本的 HTML 以正式规范的形式涵盖了尽可能多的 BOM 特性。

BOM 主要针对浏览器窗口和子窗口（frame），不过人们通常会把任何特定于浏览器的扩展都归在 BOM 的范畴内。比如，这样一些扩展：

- 弹出新浏览器窗口的能力；
- 移动、缩放和关闭浏览器窗口的能力；
- navigator 对象，提供关于浏览器的详尽信息；
- location 对象，提供浏览器加载页面的详尽信息；
- screen 对象，提供关于用户屏幕分辨率的详尽信息； 
- performance 对象，提供浏览器内存占用、导航行为和时间统计的详尽信息； 
- 对 cookie 的支持； 
- 其他自定义对象，如 XMLHttpRequest 和 IE 的 ActiveXObject。

## <script>元素

```html
<body>
  <!-- 方法1：script标签 -->
  <script type="text/javascript">
    alert("hello");
  </script>

  <!-- 方法2：外部引入(推荐)：1. 可维护性；2. 缓存：浏览器会根据特定的设置缓存所有外部链接的 JS 文件，如果两个页面用到同一个文件，只需下载一次。页面加载更快。 -->
  <script type="text/javascript" src="js/script.js"></script>
  
  <!-- 方法3：写在标签体 -->
  <input onclick="alert('hello');" type="button" value="点击按钮" />
  <a href="javascript:alert('hello');">点击a标签</a>
</body>
```

<script>元素有下列 8 个属性：

- **async**：表示应该立即开始下载脚本，但不能阻止其他页面动作，只对外部脚本文件有效。 

- - async 脚本不保证按照它们出现的次序执行。
  - 目的是告诉浏览器，不必等脚本下载和执行完后再加载页面，同样也不必等到该异步脚本下载和执行后再加载其他脚本。因此，异步脚本不应该在加载期间修改 DOM。
  - 异步脚本保证会在页面的 load 事件前执行，但可能会在 DOMContentLoaded之前或之后。

- charset：使用 src 属性指定的代码字符集。很少使用，大多数浏览器不在乎它的值。 
- crossorigin：配置相关请求的CORS（跨源资源共享）设置。默认不使用CORS。crossorigin= "anonymous"配置文件请求不必设置凭据标志。crossorigin="use-credentials"设置凭据标志，意味着出站请求会包含凭据。
- **defer**：告诉浏览器立即下载，但延迟到整个页面都解析完毕后再运行。只对外部脚本文件有效。在 IE7 及更早的版本中，对行内脚本也可以指定这个属性。 

- - 推迟执行的脚本不一定总会按顺序执行或者在 DOMContentLoaded事件之前执行，因此最好只包含一个这样的脚本。

- integrity：允许比对接收到的资源和指定的加密签名以验证子资源完整性（SRI， Subresource Integrity）。如果接收到的资源的签名与这个属性指定的签名不匹配，则页面会报错，脚本不会执行。可以用于确保内容分发网络（CDN，Content Delivery Network）不会提供恶意内容。 
- language：废弃。最初用于表示代码块中的脚本语言（如"JavaScript"、"JavaScript 1.2"或"VBScript"）。大多数浏览器都会忽略这个属性，不应该再使用它。 
- src：表示包含要执行的代码的外部文件。
- type：代替 language，表示代码块中脚本语言的内容类型（也称 MIME 类型）。按照惯例，这个值始终都是"text/javascript"，尽管"text/javascript"和"text/ecmascript"都已废弃。JavaScript 文件的 MIME 类型通常是"application/x-javascript"，不过给 type 属性这个值有可能导致脚本被忽略。在非 IE 的浏览器中有效的其他值还有"application/javascript"和"application/ecmascript"。如果这个值是 module，则被当成 ES6 模块，这时候代码中才能出现 import 和 export 关键字。

### 动态加载脚本

```javascript
let script = document.createElement('script'); 
script.src = 'gibberish.js'; 
// script.async = false;
document.head.appendChild(script);
```

默认情况下，这种方式创建的<script>元素是以异步的，相当于加了 async。但不是所有浏览器都支持 async。如果要统一动态脚本的加载行为，可将其设置为同步加载：`script.async = false;`

以这种方式获取的资源对浏览器预加载器是不可见的。这会严重影响它们在资源获取队列中的优先级。可能会严重影响性能。要想让预加载器知道动态请求文件的存在，在文档头部声明：`<link rel="preload" href="gibberish.js">`

## 严格模式

ECMAScript 5 增加了严格模式（strict mode）的概念。严格模式是一种不同的 JavaScript 解析和执行模型，对于不安全的活动将抛出错误。

在脚本开头加上这一行：`"use strict"; `

单独指定一个函数在严格模式下执行：`function doSomething() {  "use strict";  // 函数体 }`

## var,let,const

- 使用`var`来声明变量。

- - 只有`**函数作用域**`和`**全局作用域**`，没有块级作用域。
  - 全局作用域中声明的变量会成为 window 对象的属性。
  - 变量提升
  - 允许重新声明

- `let`是有块级作用域。
- `const`。与 let 基本相同，唯一一个重要的区别是用它声明变量时必须同时初始化变量，且尝试修改 const 声明的变量会导致运行时错误。

### 变量作用域

函数之外声明的变量--**全局变量**，可被当前文档中的任何其他代码所访问。

- 在浏览器中，除非使用 modules，否则使用 var 声明的全局函数和变量会成为全局对象的属性。

函数内部声明的变量--**局部变量**，只能在当前函数的内部访问。

```javascript
if (true) {
  // 全局变量（全局作用域）
  var x = 5;
}
console.log(x); // 5


// 使用 ECMAScript 6 中的 let 声明
if (true) {
  let y = 5;
}
console.log(y); // ReferenceError: y 没有被声明



function sayHi() {
  if (true) {
    // 局部变量（函数作用域）
    var phrase = "Hello";

    // 全局变量（全局作用域）
    phrase2 = "Hello2";
  }

  alert(phrase); // 能正常工作
  alert(phrase2); // 能正常工作
}

sayHi();
alert(phrase); // ReferenceError: phrase is not defined
alert(phrase2); // ok
```

### IIFE

- “立即调用函数表达式”（immediately-invoked function expressions，IIFE）一种模仿块级作用域的方法。

```javascript
(function() {
  var message = "Hello";
  alert(message); // Hello
})();
```

### var允许重新声明

```javascript
let user = "Pete";
let user = "John"; // SyntaxError: Identifier 'user' has already been declared

var user = "Pete";
var user = "John"; // 这个 "var" 无效（变量已经声明过了）
alert(user); // John
```

### 变量提升

- **变量提升：先使用变量稍后再声明变量而不会引发异常。**
- JS 变量被“提升”到函数作用域的顶部。但是，提升后的变量将返回 undefined

```javascript
/**
 * 例子 1 效果等同于 例子 2
 */
console.log(x === undefined); // true
var x = 3;


/**
 * 例子 2
 */
var y;
console.log(y === undefined); // true
y = 3;
```

ES 6 中，let和const也会被提升变量到代码块的顶部但不会被赋予初始值。

在解析代码时，JavaScript 引擎也会注意出现在块后面的 let 声明，只不过在此之前不能以任何方式来引用未声明的变量。在 let 声明之前的执行瞬间被称为“暂时性死区”（temporal dead zone），在此阶段引用任何后面才声明的变量都会抛出 ReferenceError。

```javascript
console.log(x); // ReferenceError
let x = 3;
```

### 函数提升

```javascript
/* 函数声明 */
foo(); // bar

function foo() {
  console.log("bar");
}


/* 函数表达式 */
// baz(); // 类型错误：baz 不是一个函数

var baz = function() {
  console.log("bar2");
};

baz(); // bar2
```

## 数据类型

- 最新的 ECMAScript 标准定义了 8 种数据类型
- 有 7 种简单数据类型（也称为原始类型）：Undefined、Null、Boolean、Number、Bigint、String 和 Symbol（ECMAScript 6 新增）
- 有一种复杂数据类型叫 Object（对象）。Object 是一种无序名值对的集合
- `**typeof 变量**`检查变量类型

- - "undefined" 值未定义；
  - "boolean" 布尔值；
  - "string" 字符串；
  - "number" 数值；
  - "object" 对象或 null；
  - "function" 函数； ECMA-262 规定，任何实现内部[[Call]]方法的对象在typeof 检测时返回"function"。
  - "symbol" 符号;
  - "bigint" bigint

### string

- `var str = "hello";` 表示零或多个 16 位 Unicode 字符序列

- - `""`  `''`  ````  

### number

- 使用 IEEE 754 格式表示整数和浮点值
- 范围： `±(253-1)` 【`±9007199254740991`】，超过会不精确

```javascript
var num1 = 11;
var num2 = 11.22; 
var num3 = Number.MAX_VALUE; // 最大值
var num4 = Number.MIN_VALUE; // 0以上的最小值
var num5 = 1/0; // Infinity 无穷大 
var num6 = "not a number" / 2; // NaN, not a number 不是数的数
```

存储浮点值使用的内存空间是存储整数值的两倍，ECMAScript 总是想方设法把值转换为整数。

```
let floatNum1 = 1.; // 小数点后面没有数字，当成整数 1 处理
let floatNum2 = 10.0; // 小数点后面是零，当成整数 10 处理
```



浮点值的精确度最高可达 17 位小数，但在算术计算中远不如整数精确。例如，0.1 加 0.2 得到的不是 0.3，而是 0.300 000 000 000 000 04。由于这种微小的舍入错误，导致很难测试特定的浮点值。

```
if (a + b == 0.3) { console.log("You got 0.3");   // 别这么干！ }
```



**值的范围：**ECMAScript 可以表示的最小数值保存在 Number.MIN_VALUE（多数浏览器中是 5e-324）。最大数值保存在Number.MAX_VALUE（多数浏览器中是 1.797 693 134 862 315 7e+308）。如果某个计算结果超出了范围，那么这个数值会被自动转换为一个特殊的 Infinity（无穷）值。任何无法表示的负数以-Infinity（负无穷）。



**NaN：**

- 任何涉及 NaN 的操作始终返回 NaN（如 NaN/10），
- NaN 不等于包括 NaN 在内的任何值

### bigint 

一种特殊的数字类型，它提供了对任意长度整数的支持。

创建 bigint 的方式有两种：在整数字面量后加 n 或调用 BigInt 函数，该函数从字符串、数字等中生成 bigint。

- `const bigint = 1234567890123456789012345678901234567890n;`
- `const sameBigint = BigInt("1234567890123456789012345678901234567890");`



对 bigint 的所有操作，返回的结果也是 bigint。

不可以把 bigint 和常规数字类型混合使用，应该显式地转换：使用 BigInt() 或者 Number()

- `alert(bigint + BigInt(number));`
- `alert(Number(bigint) + number); // 如果 bigint 太大而数字类型无法容纳，会截断多余的位`

#### 比较运算符

比较运算符，如 < 和 >，对 bigint 和 number 类型的数字进行比较没有问题：

- `alert( 2n > 1n ); // true alert( 2n > 1 ); // true`

进行 ===（严格相等）比较时不相等：

- `alert( 1 === 1n ); // false`



在布尔运算中时，bigint 的行为类似于 number。

### boolean

- `true, false`

### null	

- null 值表示一个空对象指针，这也是给typeof 传一个 null 会返回"object"的原因。
-  null 在数值类型环境中被当作 `0`
- 在定义将来要保存对象值的变量时，建议使用 null 来初始化，不要使用其他值。
- `typeof null` 为 "object"。这是错误的，这个问题来自于 JavaScript 语言的早期阶段，为了兼容性而保留。
- 类似的：

- - `typeof alert` 为 "function"，alert 在 JavaScript 语言中是一个函数。函数隶属于 object 类型。但是 typeof 会对函数区分对待。

### undefined

-  未定义`用 var 或 let 语句声明的变量，如果没有赋初始值，则其值为 undefined。`建议在声明变量的同时进行初始化。
- 数值类型环境中 undefined 值会被转换为 `NaN`
- 增加这个特殊值的目的就是为了明确空对象指针（null）和未初始化变量的区别。

```javascript
let message; // 这个变量被声明了，只是值为 undefined 
// 确保没有声明过这个变量
// let age 
console.log(typeof message); // "undefined" 
console.log(typeof age); // "undefined"
```

undefined 值是由 null 值派生而来的，因此 ECMA-262 将它们定义为表面上相等。`console.log(null == undefined); // true`

### Symbol 

- ECMAScript 6 中新添加的类型。一种实例是唯一且不可改变的数据类型。

### object

-  引用数据类型
- `let o = new Object();`
- Object 的实例并不是很有用，但与它相关的概念非常重要。类似 Java 中的 java.lang.Object，ECMAScript 中的 Object 也是派生其他对象的基类。Object 类型的所有属性和方法在派生的对象上同样存在。

- - `constructor`：用于创建当前对象的函数。在`let o = new Object();`中，这个属性的值就是 Object() 函数。
  - `hasOwnProperty(propName)`：用于判断当前对象实例（不是原型）上是否存在给定的属性。（如 o.hasOwnProperty("name" 或 Symbol)）。
  - `isPrototypeOf(object)`：用于判断当前对象是否为另一个对象的原型。
  - `propertyIsEnumerable(propertyName)`：用于判断给定的属性是否可以使用 for-in 语句枚举。
  - `toLocaleString()`：返回对象的字符串表示，该字符串反映对象所在的本地化执行环境。
  - `toString()`：返回对象的字符串表示。
  - `valueOf()`：返回对象对应的字符串、数值或布尔值表示。通常与 toString()的返回值相同。

## 数据类型转换

### 转为string

```javascript
<script type="text/javascript">
  var num1 = 111;
  var bool = false;
  var a = null;
  var b = undefined;
  
  // 方法1：toString()方法, null, undefined 没有此方法。
  num1 = num1.toString();
  bool = bool.toString();
  alert(typeof num1); // string
  
  // 方法2：String()函数：如果值有 toString()方法，则调用该方法（不传参数）并返回结果。如果值是 null，返回"null"。如果值是 undefined，返回"undefined"。
  a = String(a); // "null"
  b = String(b); // "undefined"
  
	// 多数情况下，toString()不接收参数。在对数值调用这个方法时，toString()可以接收一个底数参数
	// 通过传入参数，可以得到数值的二进制、八进制、十六进制，或者其他任何有效基数的字符串表示
  let num = 10; 
  console.log(num.toString()); // "10" 
  console.log(num.toString(2)); // "1010"

</script>
```

### 转为number

有 3 个函数可以将非数值转换为数值：`Number()`、`parseInt()`和 `parseFloat()`。Number()是转型函数，可用于任何数据类型。后两个函数主要用于将字符串转换为数值。

```javascript
<script type="text/javascript">
  const str1 = Number(""); 				// 0
  const str2 = Number("123");			// 123
	const str3 = Number("1.23");		// 1.23
  const str4 = Number("123abc");	// NaN
	const str5 = Number("0xf");			// 15 （该十六进制值对应的十进制整数值）
  const bool = Number(true);			// 1
  const a = Number(null);					// 0
  const b = Number(undefined);		// NaN
  
  // 方法2：parseInt()和parseFloat()函数：分别取出字符串中的整数和浮点数（数字或.(对于parseFloat())必需在开头）
  const str4 = parseInt("123px", 10); 		// 123 	第二个参数是数字的进制
  const str5 = parseInt("123.456cm"); // 123.456	parseFloat()只解析十进制值
  const str6 = parseInt(".233cm"); 		// 0.233
	const str7 = parseInt("-1.233cm"); 		// -1.233
  const str8 = parseInt("qq233cm"); 	// NaN
	const str9 = parseInt(""); 	// NaN 【对于空串的处理 这是parseInt和parseFloat跟Number 不同的地方 】
  
  // 方法3：var num = +"123";
</script>
```

| undefined     | NaN                                                          |
| ------------- | ------------------------------------------------------------ |
| null          | 0                                                            |
| true 和 false | 1 and 0                                                      |
| string        | 去掉首尾空白字符（空格、换行符 \n、制表符 \t 等）后。如果剩余字符串为空，则转换为 0。否则，将会从剩余字符串中“读取”数字。当类型转换出现 error 时返回 NaN。 |

### 转为boolean

- 使用`Boolean()`函数

| 0, null, undefined, NaN, "" | false |
| --------------------------- | ----- |
| 其他值                      | true  |

## 非boolean的 `&&` `||` `!` 运算

```javascript
<script type="text/javascript">
  // 遇见 false【转为boolean后的】 返回为false的值，没有遇见返回最后一个值
  var a = 0 && 1; // 返回 0
  var b = 1 && 0 && 1; // 返回 0

  // 遇见true【转为boolean后】 返回为true的值，没有遇见返回最后一个值
  var c = 1 || 0; // 返回 1
  var d = 0 || 1 || 0; // 返回 1

  // !运算
  alert(!1); // false
  alert(!!1); // true，将任意值转为boolean值
</script>

// 优先级：! > && > ||
```

### ?? 运算

- `??`空值合并运算符
- 一个值不是 null、undefined 时，将其称为“已定义的（defined）”。

- - `a ?? b` 的结果是：
  - 如果 a 是已定义的，结果为 a，
  - 如果 a 不是已定义的，结果为 b。
  - 即：`result =(a !==null&& a !==undefined)? a : b;`

### 与 || 比较

- `??` 返回第一个**已定义的值**。
- `||` 返回第一个**真值**。

- - `||` 无法区分 `false、0、"" 和 null/undefined`。它们都一样 —— 假值（falsy values）。

- `??` 运算符的优先级与 `||` 相同
- JavaScript 禁止将 `??` 运算符与 `&&` 和 `||` 运算符一起使用，除非使用括号指定了优先级。

- - `let x = 1 && 2 ?? 3; // Syntax error`
  - `let x = (1 && 2) ?? 3; // OK!`

## 严格相等

- `==`处于相等判断符号 == 两侧的值会先被转化为数字。空串和 false 也是如此，转化后它们都为数字 0。
- 严格相等运算符 `===` 在进行比较时不会做任何的类型转换。

- - `switch('1'){case '1':}` switch与case的对应就是严格相等

### 与 Object.is 进行比较

- 一个特殊的内建方法 `Object.is`，它类似于 `===` 一样对值进行比较

- - 它适用于 NaN：`Object.is(NaN, NaN) === true`
  - `0` 和 `-0` 是不同的：

- - - `Object.is(0，-0) === false`
    - ` console.log(0 === -0); // true`

- 其他情况，`Object.is(a，b) 与 a === b` 相同

## 关系运算

```javascript
<script type="text/javascript">
  alert(1 > ""); // ture
  alert(1 > "hello"); // false
  alert(1 > "2"); // false
  alert(1 < "2"); // true
  alert(1 > NaN); // false
  alert("11" > "2"); // false
  // 1、number与string、boolean比较，string、boolean转number再比较；
  // 2、number与 NaN 比较为 false；
  // 3、string相互比较，转为ASCII一位一位比较
  
  // 4、NaN 不和任何值相等；null == undefined 为true
  // 5、通过函数 isNaN() 判断是否为NaN；
</script>
```

### 乘法操作符

- 如果 ECMAScript 不能表示乘积，则返回 Infinity 或-Infinity。
- 任一操作数是 NaN，则返回 NaN。
- Infinity 乘以 0，则返回 NaN。
- Infinity 乘以非 0的有限数值，则根据第二个操作数的符号返回 Infinity 或-Infinity。
- Infinity 乘以 Infinity，则返回 Infinity。
- 有不是数值的操作数，则先在后台用 Number()将其转换为数值，然后再应用上述规则。

### 除法操作符

- 有任一操作数是 NaN，则返回 NaN。 
- Infinity 除以 Infinity，则返回 NaN。 
- 0 除以 0，则返回 NaN。 
- 非 0 的有限值除以 0，则根据第一个操作数的符号返回 Infinity 或-Infinity。 
- Infinity 除以任何数值，则根据第二个操作数的符号返回 Infinity 或-Infinity。

## 位操作符

ECMAScript 中的所有数值都以 IEEE 75464 位格式存储，但位操作并不直接应用到 64 位表示，而是先转换为 32 位整数，再操作，之后再把结果转换为 64 位。对开发者而言，就好像只有 32 位整数一样，因为 64 位整数存储格式是不可见的。所以只需要考虑 32 位整数即可。

有符号整数使用 32 位的前 31 位表示整数值。第 32 位表示数值的符号，如 0 表示正，1 表示负。



- 正值以真正的二进制格式存储。如18的二进制格式为00000000000000000000000000010010，或更精简的 10010。
- 负值以一种称为二补数（或**补码**）的二进制编码存储。

- - 补码 = 反码 + 1
  - 反码 = 原码取反
  - ![img](E:\HelloWorld\学习资料\md\assets\1681132339298-622c81b0-5de4-446c-ac2b-0a2d7f92aa7c.png)
  - `let num = -18; console.log(num.toString(2)); // "**-10010**" `



在对 ECMAScript 中的数值应用位操作符时，后台会发生转换：64 位数值会转换为 32 位数值，然后执行位操作，最后再把结果从 32 位转换为 64 位存储起来。整个过程就像处理 32 位数值一样，这也导致了一个副作用，NaN 和Infinity在位操作中都会被当成 0 处理。

如果将位操作符应用到非数值，那么首先会使用 Number()函数将该值转换为数值，然后再应用位操作。最终结果是数值。

**按位非：**

```javascript
let num1 = 25; // 二进制 00000000000000000000000000011001 
let num2 = ~num1; // 二进制 11111111111111111111111111100110 
console.log(num2); // -26  ========> (-num1 - 1)
```



**运算优先级：**

![img](E:\HelloWorld\学习资料\md\assets\1609666735886-b2ee9336-5de5-4223-8d91-81b03ac6c64f.png)

# **函数**

也是一个对象

## 基本操作

函数声明`**function fun(param1,param2,...) {} // 在所有代码执行前被创建**`  

函数表达式`var fun = function() {};` 

```javascript
function fun(a, b) {
  return a + b; // 不写return或写 return; 返回undefined
}

var sum = fun(1, 2, "hello");
alert(sum);
```

## 函数成为对象的属性--方法

```javascript
var obj = {
  name: "婉君",
  display() {
    alert("我叫婉君");
  }
};
obj.display(); // 我叫婉君
```

## 工厂模式

```javascript
function createPerson(name, age, job) { 
 let o = new Object(); 
 o.name = name; 
 o.age = age; 
 o.job = job; 
 o.sayName = function() { 
 	console.log(this.name); 
 }; 
  
 return o; 
} 

let person1 = createPerson("Nicholas", 29, "Software Engineer"); 
let person2 = createPerson("Greg", 27, "Doctor");
```

## 构造函数

构造函数也是函数。并没有把某个函数定义为构造函数的特殊语法。只要使用 new 操作符调用就是构造函数，不使用 new 操作符调用的就是普通函数。

使用构造函数和 "new" 操作符来实现：

- 在内存中创建一个新对象。 
- 新对象内部的[[Prototype]]特性被赋值为构造函数的 prototype 属性。
- this 指向新对象
- 执行构造函数内部的代码（给新对象添加属性）。 
-  如果构造函数返回非空对象，则返回该对象；否则，返回刚创建的新对象。

```javascript
function Person(name, age) { // 首字母大写	
  this.name = name;
  this.age = age;
  this.display = display;
}

var per1 = new Person("婉君");
var per2 = new Person("家明", 18);

alert(per1.name); // 婉君
alert(per1.age); // undefined
alert(per2.age); // 18
per2.display(); // hello!家明

// 检查一个对象属于一个类
alert(per1 instanceof Person); // true
```

## 函数表达式 vs 函数声明

- **函数表达式**在代码执行到达时被创建，并且仅从那一刻起可用。



- **函数声明**在被定义之前，就能被调用。
- 如，一个全局函数声明对整个脚本来说都是可见的，无论它被写在这个脚本的哪个位置。
- 这是内部算法的原故。当 JavaScript 准备运行脚本时，首先会在脚本中寻找全局函数声明，并创建这些函数。可将其视为“初始化阶段”。在处理完所有函数声明后，代码才被执行。所以运行时能够使用这些函数。

```javascript
sayHi("John"); // Hello, John
function sayHi(name) {
  alert( `Hello, ${name}` );
}


//********************************************************
sayHi("John"); // error!
let sayHi = function(name) {
  alert( `Hello, ${name}` );
};
```



函数声明的另外一个特殊的功能是它们的块级作用域。

严格模式下，当一个函数声明在一个代码块内时，它在该代码块内的任何位置都是可见的。但在代码块外不可见。

```javascript
let age = prompt("What is your age?", 18);

// 有条件地声明一个函数
if (age < 18) {

  function welcome() {
    alert("Hello!");
  }

} else {

  function welcome() {
    alert("Greetings!");
  }

}

// ……稍后使用
welcome(); // Error: welcome is not defined
```

**根据经验，声明函数时，首先考虑函数声明语法。**它能够为组织代码提供更多的灵活性。因为可以在声明这些函数之前调用这些函数。

## 函数的两个方法

```javascript
function fun(a, b) {
  alert(this);
  alert(a);
  alert(b);
}

// call()和apply()
// 这两个方法都是函数对象的方法，需要通过函数对象来调用
// 当对函数调用call()和apply()都会调用函数执行
// 在调用call()和apply()可以将一个对象指定为第一个参数
// 此时这个对象将会成为函数执行时的this
fun(111, 222); // [object Window] 111 222
var obj = {};
fun.call(obj, 111, 222); // [object Object] 111  222
fun.apply(obj, [111, 222]); // [object Object] 111  222
```

## 箭头函数

```javascript
function fun(a, b) {
  alert(this);
  alert(a);
  alert(b);
}

// 一个参数()括号可省略，一行代码{}可省略，return 以可省略
(a, b) => {...}

// 箭头函数中的this的指向最近作用域中的this
let obj = {
  m1() {   
    console.log(this) // obj对象
    
    setTimeOut(()=>{
      console.log(this) // obj对象
    }, 10000)
  }
}
obj.m1()
  const f2 = () => {
    console.log('b');
  }
  
  console.log(typeof f2); // function
  let f3 = new f2(); //  TypeError f2 is not a constructor
```

- 箭头函数没有 “arguments”
- 也没有 super

**普通函数的this**

- 非严格模式的情况下，this 将会是 全局对象（浏览器中的 window）
- 严格模式下的 this 值为 undefined

**箭头函数中**，this引用的是定义箭头函数的上下文。

## caller

ECMAScript 5 给函数对象上添加了`caller`属性。是调用当前函数的函数，如果在全局作用域中调用的则为 null。

```javascript
function outer() { 
 	inner(); 
} 
function inner() { 
 	console.log(inner.caller); // outer这个函数
} 
outer();
```

## new.target

ECMAScript 6 新增了检测函数是否使用 new 关键字调用的 new.target 属性。

如果函数是正常调用的，则 new.target 的值是 undefined；如果是使用 new 关键字调用的，则 new.target 将引用被调用的构造函数。

```javascript
function King() { 
 if (!new.target) { 
   throw 'King must be instantiated using "new"' 
 } 
 console.log('King instantiated using "new"'); 
} 
new King(); // King instantiated using "new" 
King(); // Error: King must be instantiated using "new"
```

## 属性与方法

ECMAScript 中的函数是对象，因此有属性和方法。每个函数都有两个属性：length和 prototype。其中，length 属性保存函数定义的命名参数的个数。

```javascript
function sayName(name) { 
 console.log(name); 
} 
function sum(num1, num2) { 
 return num1 + num2; 
} 
function sayHi() { 
 console.log("hi"); 
} 
console.log(sayName.length); // 1 
console.log(sum.length); // 2 
console.log(sayHi.length); // 0
```

## 尾调优化

...

## 闭包

JavaScript 允许函数嵌套，且内部函数可以访问定义在外部函数中的所有变量和函数。由于内部函数可以访问外部函数的作用域，因此当内部函数生存周期大于外部函数时，外部函数中定义的变量和函数的生存周期将比内部函数执行时间长。当内部函数以某一种方式被任何一个外部函数作用域访问时，一个闭包就产生了。

闭包：指一个引用了另一个函数作用域中变量的函数，通常是在嵌套函数中实现的。在 JavaScript 中，所有函数都是天生闭包的（只有一个例外："new Function"）。

```javascript
function makeCounter() {
    let count = 0;

    return function () {
      return count++;
    };
  }

  let counter = makeCounter();

  console.log(counter()); // 0
  console.log(counter()); // 1
  console.log(counter()); // 2
```

## 默认参数

```javascript
// 为参数b设置默认参数
function multiply(a, b = 1) {
  // b = (typeof b !== 'undefined') ?  b : 1;
  return a*b;
}

multiply(5); // 5

function showMessage(from, text = anotherFunction()) {
  // anotherFunction() 仅在没有给定 text 时执行，返回值将成为 text 的值
}
```

## 剩余参数

```javascript
function multiply(multiplier, ...theArgs) {
  //...
}

var arr = multiply(2, 1, 2, 3);
```

## "new Function" 语法

```javascript
// let func = new Function ([arg1, arg2, ...argN], functionBody);

let sum = new Function('a', 'b', 'return a + b');
alert( sum(1, 2) ); // 3
```

# 对象

## 基本操作

创建`let obj = new Object();` 

添加属性`obj.name = "婉君";` 

获取属性`alert(obj.name); // "婉君"` 

删除属性`delete obj.name;` 

判断属性`"key"in object // true or false` 

排序属性： **整数**【有string转为number】属性`{"3":"c", "2":"b"}`会被进行排序【遍历时是有顺序的】，其他属性则按照创建的顺序显示 

```javascript
var obj = new Object();
obj["name1"] = " 婉君";
var str = "name";
alert(obj["name" + "1"]); // 婉君
alert(obj[str]); // 婉君

delete obj[str];
```

### 使用对象字面量来创建对象（推荐）：

`var obj = {};` 对象字面量表示法定义对象时，并不会调用 Object 构造函数。

```javascript
var obj2 = {
  name:"婉君",
  age=18,
  fun() { // 函数
  } 
};

// 同上
name:"婉君"
age=18
var obj2 = {name,age};
```

### 遍历对象 

```javascript
for(var n in obj){
    alert("属性名："+ n); 
    alert("属性值：" + obj[n]);
} 
```

### 克隆与合并，Object.assign

当对象变量被复制 —— 引用被复制，而该对象自身并没有被复制。

- 把源对象所有的本地属性一起复制到目标对象上。有时候这种操作也被称为“混入”（mixin），因为目标对象通过混入源对象的属性得到了增强。

```javascript
let user = {
  name: "John",
  age: 30
};

let clone = {}; // 新的空对象

// 将 user 中所有的属性拷贝到其中
for (let key in user) {
  clone[key] = user[key];
}

// 现在 clone 是带有相同内容的完全独立的对象
clone.name = "Pete"; // 改变了其中的数据
console.log( user.name ); // 原来的对象中的 name 属性依然是 John

// 方式2：Object.assign(dest, [src1, src2, src3...])
// dest 是目标对象。参数 src1, ..., srcN是源对象。将所有源对象的属性拷贝到目标对象 dest 中。返回 dest。

// 方式3：使用 spread 语法 clone = {...user}
```

### 深层克隆

```javascript
let user = {
  name: "John",
  // 属性可以是对其他对象的引用，简单clone： clone 和 user 会共用一个 sizes
  sizes: {
    height: 182,
    width: 50
  }
};
```

可以使用递归来实现它。或者为了不重复造轮子，采用现有的实现，例如 [lodash](https://lodash.com/) 库的 [_.cloneDeep(obj)](https://lodash.com/docs#cloneDeep)。

## Object 属性和方法

- constructor：用于创建当前对象的函数。在前面的例子中，这个属性的值就是 Object() 函数。
- hasOwnProperty(propertyName: string | symbol)：用于判断当前对象实例（不是原型）上是否存在给定的属性。
- isPrototypeOf(object)：用于判断当前对象是否为另一个对象的原型。
- propertyIsEnumerable(propertyName: string | symbol)：用于判断给定的属性是否可以使用for-in 语句枚举。
- toLocaleString()：返回对象的字符串表示，该字符串反映对象所在的本地化执行环境。
- toString()：返回对象的字符串表示。
- valueOf()：返回对象对应的字符串、数值或布尔值表示。通常与 toString()的返回值相同。

## 可选链?.

- 当可选链 `?.` 前面的值为 `undefined` 或者 `null`，会停止运算并返回 undefined
- 使用`?.` 来安全地读取或删除，不能写入。

```javascript
let user = {}; // user 没有 address 属性

// console.log( user.car.name ); // Cannot read properties of undefined (reading 'name')
console.log( user.car?.name ); // undefined

user = null;
user?.name = "John"; // Error，不起作用
// 因为它在计算：undefined = "John"
```

### 变体?.()，?.[]

- `?.()` 用于调用一个可能不存在的函数。
- `?.[]` 它允许从一个可能不存在的对象上安全地读取属性。

```javascript
// user.admin(); // TypeError: user.admin is not a function
const result =  user.admin?.(); // 啥都没发生，result为undefined


let user1 = {
  firstName: "John"
};

console.log(user1?.["firstName"]); // John
// console.log(user1.["lastName"]); // Unexpected token '['
console.log(user1?.["lastName"]); // undefined

user1 = null;
console.log(user1?.["lastName"]); // undefined


// 将 ?. 跟 delete 一起使用：
delete user?.name; // 如果 user 存在，则删除 user.name
```

## symbol 类型

根据规范，只有两种原始类型可以用作对象属性键：

- 字符串类型
- symbol 类型
- 如果使用别的类型，如number、boolean，会被自动转换为字符串。所以 `obj[1]` 与 `obj["1"]` 相同，`obj[true]`与 `obj["true"]` 相同。
- 凡是可以使用字符串或数值作为属性的地方，都可以使用符号



- “symbol” 值表示唯一的标识符。
- 使用 `Symbol()` 来创建这种类型的值：`let id = Symbol("id"); // id 是描述为 "id" 的 symbol`
- **symbol 保证是唯一的**。即使创建了许多具有相同描述的 symbol，它们的值也是不同。

- - `let id1 =Symbol("id"); let id2 =Symbol("id");alert(id1 == id2);// false`

- **symbol 不会被自动转换为字符串**

- - `// console.log(id); // Cannot convert a Symbol value to a string`
  - `***console***.log(***id***.toString()); // Symbol(id)`
  - `alert(id.description);// id`

- symbol 在 for…in 中会被跳过
- Object.assign 会同时复制字符串和 symbol 属性

### “隐藏”属性

如果使用第三方代码的 user 对象，想要给它添加一些标识符。

由于 user 对象属于另一个代码库，所以向它们添加字段是不安全的，可能会影响代码库中的其他预定义行为。但 symbol 属性不会被意外访问到。第三方代码不会知道新定义的 symbol，因此将 symbol 添加到 user 对象是安全的。

```javascript
  let user = { // 属于另一个代码
    name: "John"
  };

  {
    let id = Symbol("id");

    user[id] = 1;
    alert( user[id] ); // 1, 使用 symbol 作为键来访问数据 
  }

  // 从新定义Symbol类的id，不会影响到原来的id
  let id = Symbol("id");

  user[id] = 2;
  console.log( user[id] ); // 2, 使用 symbol 作为键来访问数据

// 标识符和它们的标识符之间不会有冲突，因为 symbol 总是不同的，即使它们有相同的名字。如下图
```

![img](E:\HelloWorld\学习资料\md\assets\1661874700694-e29d545b-e194-4797-afe0-b025c11ae31d.png)

```javascript
let id = Symbol("id");

let user = {
  name: "John",
  [id]: 123 // 而不是 "id"：123
};
```

### 全局 symbol

通常所有的 symbol 都是不同的，即使它们有相同的名字。但有时想要名字相同的 symbol 具有相同的实体。

为了实现这一点，这里有一个 **全局 symbol 注册表**。我们可以在其中创建 symbol 并在稍后访问它们，它可以确保每次访问相同名字的 symbol 时，返回的都是相同的 symbol。



- 从注册表中读取（不存在则创建）symbol：`Symbol.for(key)`
- 该调用会检查全局注册表，如果有一个描述为 key 的 symbol，则返回该 symbol，否则将创建一个新 symbol（Symbol(key)），并通过给定的 key 将其存储在注册表中并返回。
- 通过全局 symbol 返回description：`Symbol.keyFor(sym)`

```javascript
// 从全局注册表中读取
let id = Symbol.for("id"); // 如果该 symbol 不存在，则创建它

// 再次读取（可能是在代码中的另一个位置）
let idAgain = Symbol.for("id");

// 相同的 symbol
alert( id === idAgain ); // true

// 通过 symbol 获取 name
alert( Symbol.keyFor(idAgain) ); // id, 不适用于非全局 symbol, 如果使用返回undefined
```

symbol 不是 100% 隐藏的。有一个内建方法 Object.getOwnPropertySymbols(obj) 允许我们获取所有的 symbol。还有一个名为 Reflect.ownKeys(obj) 的方法可以返回一个对象的 所有 键，包括 symbol。但大多数库、内建方法和语法结构都没有使用这些方法。

## 对象的 toString方法

- 可为对象添加toString 和 valueOf 方法，当对象需要被转换时就会调用这些方法，方法必须返回的时基本类型。

```javascript
let obj = {
  name:'zs',

  toString() {
    return 999;
  }
}

// alert 默认会将对象转换
alert(obj); // 999
```

valueOf() 获取对象的原始值（原始类型），通常返回的是该对象对应的基本类型的值。如，对于字符串对象，valueOf() 返回的是字符串，数字对象，返回的是数字的原始值（数字）。

toString() 方法用于将当前对象转换成字符串。如，对于数字对象，toString() 方法返回的是数字的字符串形式，对于日期对象，toString() 方法返回的是日期的字符串形式。



在 JS 中，当需要使用一个对象的原始值时，会优先调用对象的 valueOf() 方法，如果该方法返回的不是原始值，那么 JavaScript 引擎就会尝试调用 toString() 方法将其转换为原始值。因此，在对象进行运算或比较时，valueOf() 方法具有更高的优先级。

如果一个对象同时实现了 valueOf() 和 toString() 方法，可以通过覆盖这两个方法来自定义该对象的原始值。同时，JavaScript 还提供了一些原始类型的构造函数（比如 Number、String、Boolean 等），这些构造函数也实现了 valueOf() 和 toString() 方法，因此我们可以通过扩展这些构造函数的原型来修改它们的行为。

## 隐藏类和删除操作

V8 在将解释后的 JavaScript代码编译为实际的机器码时会利用“**隐藏类**”。如果代码非常注重性能，这一点可能很重要。

运行期间，V8 会将创建的对象与隐藏类关联起来，以跟踪它们的属性特征。能够共享相同隐藏类的对象性能会更好，V8 会针对这种情况进行优化，但不一定总能够做到。比如：

```javascript
function Article() { 
 this.title = 'Inauguration Ceremony Features Kazoo Band'; 
} 
// V8 会在后台配置，让这两个类实例共享相同的隐藏类，因为这两个实例共享同一个构造函数和原型。
let a1 = new Article(); 
let a2 = new Article();

// 假设之后又添加了这行代码,两个 Article 实例对应两个不同的隐藏类。根据这种操作的频率和隐藏类的大小，可能对性能产生明显影响。
a2.author = 'Jake'; 
 this.title = 'Inauguration Ceremony Features Kazoo Band'; 
 this.author = opt_author; 
} 
let a1 = new Article(); 
let a2 = new Article('Jake');
```

使用 delete 关键字会导致生成相同的隐藏类片段

```javascript
function Article() { 
 this.title = 'Inauguration Ceremony Features Kazoo Band'; 
 this.author = 'Jake'; 
} 
let a1 = new Article(); 
let a2 = new Article(); 
delete a1.author; // a1.author = null;
/*
代码结束后，即使两个实例使用了同一个构造函数，它们也不再共享一个隐藏类。动态删除属性与动态添加属性导致的后果一样。
最佳实践是把不想要的属性设置为 null。这样可以保持隐藏类不变和继续共享，同时也能达到删除引用值供垃圾回收程序回收的效果。
*/
```

## 内存泄漏

```javascript
function setName() { 
 name = 'Jake';  // 解释器会把 name 当作 window 的属性来创建（window.name = 'Jake'）。只要 window 本身不被清理就不会消失。
}


let name = 'Jake'; 
setInterval(() => { 
 console.log(name); // 只要定时器一直运行，回调函数中引用的 name 就会一直占用内存。
}, 100);


// 调用 outer()会导致分配给 name 的内存被泄漏。创建了一个内部闭包，只要返回的函数存在就不能清理 name，因为闭包一直在引用着它。
let outer = function() { 
 let name = 'Jake'; 
 return function() { 
 return name; 
 }; 
};
// 清理
outer = null;
```

## 单例内置对象

ECMA-262 对内置对象的定义“任何由 ECMAScript 实现提供、与宿主环境无关，并在 ECMAScript程序开始执行时就存在的对象”。包括 Object、Array 和 String。和另外两个单例内置对象：Global 和 Math。

ECMA-262 规定 Global对象为一种兜底对象，它所针对的是不属于任何对象的属性和方法。

事实上，不存在全局变量或全局函数这种东西。在全局作用域中定义的变量和函数都会变成 Global 对象的属性 。如 isNaN()、isFinite()、parseInt()和 parseFloat()，都是 Global 对象的方法。

###  URL 编码方法

`encodeURI()` 和 `**encodeURIComponent**()`用于编码统一资源标识符（URI），以便传给浏览器。有效的 URI 不能包含某些字符，比如空格。使用 URI 编码方法来编码 URI 可以让浏览器能够理解它们，同时又以特殊的 UTF-8 编码替换掉所有无效字符。

encodeURI()不会编码属于 URL 组件的特殊字符，比如冒号、斜杠、问号、井号，而 encodeURIComponent()会编码它发现的所有非标准字符。

`decodeURI()` 和 `decodeURIComponent()`。decodeURI()只对使用 encodeURI()编码过的字符解码。

```javascript
let uri = "http://www.wrox.com/illegal value.js#start"; 
console.log(encodeURI(uri));  // "http://www.wrox.com/illegal%20value.js#start" 
console.log(encodeURIComponent(uri)); // "http%3A%2F%2Fwww.wrox.com%2Fillegal%20value.js%23start" 

let uri = "http%3A%2F%2Fwww.wrox.com%2Fillegal%20value.js%23start"; 
console.log(decodeURI(uri)); // http%3A%2F%2Fwww.wrox.com%2Fillegal value.js%23start 
console.log(decodeURIComponent(uri)); // http:// www.wrox.com/illegal value.js#start 
```

取代了`escape()`和 `unescape()`方法（均已废弃）

### eval

一个完整的 ECMAScript 解释器。

`eval("console.log('hi')")` 执行代码。

### Global 对象属性

undefined 		特殊值 undefined 

NaN 			特殊值 NaN 

Infinity 			特殊值 Infinity 

Object 			Object 的构造函数 

Array 			Array 的构造函数 

Function 			Function 的构造函数 

Boolean 			Boolean 的构造函数 

String 			String 的构造函数

Number 			Number 的构造函数 

Date 			Date 的构造函数 

RegExp 			RegExp 的构造函数 

Symbol 			Symbol 的伪构造函数 

Error 			Error 的构造函数 

EvalError 			EvalError 的构造函数 

RangeError 		RangeError 的构造函数 

ReferenceError 	ReferenceError 的构造函数 

SyntaxError 		SyntaxError 的构造函数 

TypeError 		TypeError 的构造函数 

URIError			URIError 的构造函数

###  window 对象

浏览器将 window 对象实现为 Global 对象的代理。因此，所有全局作用域中声明的变量和函数都变成了 window 的属性。

window 对象在 JavaScript 中远不止实现了 ECMAScript 的 Global 对象那么简单。

# 赋值

| 名字             | 简写的操作符 |
| ---------------- | ------------ |
| 加法赋值         | x += y       |
| 减法赋值         | x -= y       |
| 乘法赋值         | x *= y       |
| 除法赋值         | x /= y       |
| 求余赋值         | x %= y       |
| 求幂赋值         | x **= y      |
| 左移位赋值       | x <<= y      |
| 右移位赋值       | x >>= y      |
| 无符号右移位赋值 | x >>>= y     |
| 按位与赋值       | x &= y       |
| 按位异或赋值     | x ^= y       |
| 按位或赋值       | x \|= y      |

## 解构赋值

将**数组或对象【****任何可迭代对象: string, set, ...****】**“拆包”至一系列变量中。

### 数组解构

```javascript
// 不需要第二个元素
let [firstName, , title] = ["Julius", "Caesar", "Consul", "of the Roman Republic"];
alert( title ); // Consul


let [name1, name2, ...rest] = ["Julius", "Caesar", "Consul", "of the Roman Republic"];

// rest 是包含从第三项开始的其余数组项的数组
alert(rest[0]); // Consul
alert(rest[1]); // of the Roman Republic
alert(rest.length); // 2
// 这种情况下解构赋值是通过迭代右侧的值来完成工作的。这是一种用于对在 = 右侧的值上调用 for..of 并进行赋值的操作的语法糖。
let [a, b, c] = "abc"; // ["a", "b", "c"]
let [one, two, three] = new Set([1, 2, 3]);
let user = {};
[user.name, user.surname] = "John Smith".split(' ');
let user = {
  name: "John",
  age: 30,
};

// 使用循环遍历键—值对
for (let [key, value] of Object.entries(user)) {
  alert(`${key}:${value}`); // name:John, then age:30
}


let user = new Map();
user.set("name", "John");
user.set("age", "30");

// Map 是以 [key, value] 对的形式进行迭代的，非常便于解构
for (let [key, value] of user) {
  alert(`${key}:${value}`); // name:John, then age:30
}
let guest = "Jane";
let admin = "Pete";

// 让我们来交换变量的值：使得 guest = Pete，admin = Jane
[guest, admin] = [admin, guest];

alert(`${guest} ${admin}`); // Pete Jane（成功交换！）
// 默认值
let [name = "Guest", surname = "Anonymous"] = ["Julius"];

alert(name);    // Julius（来自数组的值）
alert(surname); // Anonymous（默认值被使用了）
```

### 对象解构

```javascript
const student = {
  name: 'Jack',
  age: 22,
  sex: 'male',
  car: {
    id: 1,
    name: 'bmw',
  }
}

// 解构赋值；顺序不重要；对sex属性进行了重命名; 为pet属性附默认值；重命名和默认值可以同时使用
const {age, name, sex: gender, pet = "cat"} = student;
console.log("student:", `${name}, ${age}, ${gender}, ${pet}`); // student: Jack, 22, male, cat

// 多层解构，数组同样适用
const {car: {name}} = student;
console.log("car name:", name); // car name: bmw
let options = {
  title: "Menu",
  height: 200,
  width: 100
};

// title = 名为 title 的属性
// rest = 存有剩余属性的对象
let {title, ...rest} = options;

// 现在 title="Menu", rest={height: 200, width: 100}
alert(rest.height);  // 200
alert(rest.width);   // 100
let title, width, height;
const obj = {};
// 这一行发生了错误，要加括号
// {title, width, height} = {title: "Menu", width: 200, height: 100};
({title, width, height} = {title: "Menu", width: 200, height: 100})
// 或
({title: obj.t, width: obj.w, height: obj.h} = {title: "Menu", width: 200, height: 100})
//  JavaScript 把主代码流（即不在其他表达式中）的 {...} 当做一个代码块而不是解构赋值语法
```

### 智能函数参数

- 可以用一个对象来传递所有参数，而函数负责把这个对象解构成各个参数

```javascript
// 函数把对象解构成变量
function showMenu({title = "Untitled", width = 200, height = 100, items = []} = {}) {
  // title, items – 提取于 options; width, height – 使用默认值
  alert( `${title} ${width} ${height}` ); // My Menu 200 100
  
  alert( items ); // Item1, Item2
}

// 我们传递一个对象给函数
let options = {
  title: "My menu",
  items: ["Item1", "Item2"]
};

showMenu(options);

showMenu(); // 全部使用默认值，如果在解构赋值的最后加了  = {}，就可以这样写
```