## Day04：

### 1、HTML和CSS结合的方式

 （1）每个HTML标签里都有一个属性 style属性，在该属性中设置样式

 （2）在<head>头声明中添加；

 （3）在<head>头声明中引入外部CSS文件；<u>注意：在某些浏览器中，该引入方式不起作用</u>

 （4）通过头标签<link>引入外部文件；



**优先级（一般情况）：**

-- 由上到下，由外到内，优先级由低到高。

-- ~~后加载的优先级高~~；范围越小的优先级越高；



#### 1 CSS的基本选择器

 （1）标签选择器：使用标签名作为选择器的名称；

 （2）class选择器：：为HTML标签定义一个class名称，并使用这个名称作为选择器；

	-- <div class="aaa">aaaaaa</div>
	
	在<style>标签中写上：div.aaa { ***}

 （3）id选择器：为HTML标签定义一个id名称，并使用这个名称作为选择器

	-- <div id="aaa">aaa</div>
	
	在<style>标签中写上div#id {***}



#### 2 CSS的扩展选择器

（1）关联选择器：设置嵌套标签的样式

		-- <div><p>sdkfhskd</p></div>
	
		-- 只设置里面的p标签的样式；
	
		-- div p {****}

 















（2）组合选择器

（3）伪元素选择器



#### 3 CSS中的盒子模型

	在进行布局前需要把数据封装到一块一块的区域（div）里，称作盒子；

（1）边框

（2）内边距

（3）外边距



#### 4 CSS的布局的漂浮（了解即可）



#### 5 CSS布局的定位（了解即可）

	属性值position





### 2、javascript

#### 1.  javascript的组成

（1）ECMAScript

	-- 由ECMA组织制定javascript的语法

（2）BOM

	-- 浏览器对象模型（browser object model）

（3）DOM

	-- 文档对象模型（document object model）



#### 2. js和HTML的结合方式（两种）

1. 使用一个标签,<script type="text/javascript">这里写js代码</script>；
   注意：上面的标签可以写在<body>标签里
2. 引入外部js文件：
   -- 引入语法：<script type="text/javascript"  src="写上路径"></script>
   注意：第二种（引入外部js文件）方法的标签体里面，js代码不会执行，因此，不要在标签体中写代码



#### 3. js的原始类型（五种）

	js的原始数据类型有五种：string（注意不要大写）、number、boolean、null、undefined；通过函数`typeof()`可以查看对应变量的数据类型；



#### 4. js的运算符

1. js中字符串的相加和相减的运算逻辑不一样："456" + 1 = "4561";   "456"-1 = 455；
   如果字符串中的内容不是一个数字，那么会提示"NaN";
2. js中的 true和false分别对应整数1和0
3. ==  和 === 的区别：
   == 比较值； === 比较值和类型；



#### 5. js的函数定义及调用

格式： function 函数名(参数列表) {***}

注意：参数列表中的参数不用加上`var`关键字；



#### 6. js的全局变量好局部变量

**全局变量**：在script标签里定义的一个变量，这些变量可以在页面中js部分都可以使用（包括其他部分的script标签都能使用）；

局部变量：在方法内部定义的变量





#### 7. script标签的位置

	由于HTML的解析是从上到下解析，因此，如果js文件中需要用到body标签中某个id，那么需要先解析id，再解析js代码；即：js代码放在id定义之后。
	
	建议：把<script>标签放在<body>标签的后面



**js是否存在重载？？？**





# Day 03

### 9、dom 对象

dom：文档对象模型

	-- 文档：指的是超文本标记文档
	
	-- 对象：提供了属性和方法操作
	
	-- 模型：使用属性和方法操作超文本标记型文档

即：使用dom中提供的对象里面的属性和方法，对标记型文档进行操作。

**解析过程**：

	根据html的层级结构，在内存中分配一个树形结构，需要把html中的每部分封装成对象，
	
	-- document对象： 整个文档
	
	-- element对象：标签对象；
	
	-- 文本对象：
	
	-- Node节点对象： 是上面所有对象的父对象，定义了很多方法；







# Day05

## 使用dom4j查询xml

步骤：

1. 创建解析器；
2. 得到document对象；
3. 得到根节点；（上面三步都是相对固定的）
4. 得到所有的p1标签；
5. 得到name；
6. 得到name的值；



## 使用dom4j实现添加操作

需求：在第一个p1标签末尾添加一个元素<sex></sex>

# Day 03

## 一、javascript的对象

### 1. Array 对象的push函数

	A.push(B)：往A中加入元素B，并返回加入元素A后的长度。

注意：B是一个整体，每次push之后，A的长度+1（即使B是一个数组）。



### 2、Date对象

1. getTime() 函数用于获取1970年1月1日至今的毫秒数；
   应用场景：使用毫秒数避免缓存



### 3、Math对象

	Math对象里面的函数都是静态函数，因此，不需要新建一个Math对象（实际上，也不能新建Math对象），就可以使用里面的方法；



### 4、全局函数

1. 使用encodeURL() 和 decodeURL() 分别对中文字符进行编码和解码（因为直接输出中文时会出现乱码）



### 6、js 函数的重载

js 中不存在函数的重载；相同名称的函数，前面的函数会被最后一个函数所覆盖；

传递给函数的所有参数，都会被保存到一个数组对象 arguments 中；



问：js中是否存在重载？

答：（1） js 中不存在重载；

	（2）但是可以通过其他方式实现和重载相类似的功能；（通过arguments 数组可以模拟重载的效果）



### 7、BOM对象

	BOM中有哪些对象：
	
	① navigator：获取客户机（浏览器）的名称；
	
	② screen：获取屏幕的信息（宽、高等）
	
	③ location：请求的URL地址
	
			-- href  属性（获取请求的URL旗帜、设置URL地址）
	
	④ history：请求的URL历史记录
	
	⑤ window（重要）：窗口对象、顶层对象，所有bom对象都是在window对象里操作；



### window对象中的函数

-- setInterval()

	以指定的周期执行js代码；

-- setTimerout()

	指定的时间过后执行js代码，但是只会执行一次；

-- clearInterval()

	清除setInterval设置的定时器

-- clearTimeout()

	清除setTimerout设置的定时器



### **document 对象**

	表示整个的文档

常用方法：

-- getElementById()：得到对应id的标签

```javascript
var A = document.getElementById(id名称);
通过 A.属性名称 即可访问、设置A对应的属性名称的值
```



-- getElementsByName()：通过标签的那么属性值得到标签，返回的是一个集合（数组）



-- getElementsByTagName("标签的名称")：



### **window案例**

要点：B页面需要得到A页面的id（即：需要实现跨页面操作）；可以通过当前window的opener属性得到父窗口；

	此外，如果A页面和B页面都是编写在本地的话，通过谷歌浏览器不能从A页面跳转到B页面（因为javascript的安全性问题，并且谷歌浏览器安全级别很高）；但是实际开发中不存在这种问题，因为都是页面都是部署到服务器上运行的。



**步骤**

1. 编写一个html页面，上面放置两个输入框和一个按钮；按钮上注册一个点击事件，当点击发生时，打开一个新的窗口；
2. 编写另外一个html页面，这个页面上编写一个表格，在这个表格中填入数据：4*3,一列按钮，一列编号，一列姓名；
3. 在B页面中将数据设置到A页面中。





### **element对象**

1. removeAttribute 方法不能删除 value 属性；
2. 利用 元素标签.childNodes 得到的子标签数组，在各个浏览器中存在着兼容性问题，要想获取准确的子标签对象，只能通过 元素标签.getElementsByTagName 方法来获取；





### **Node对象**

**属性**：

- nodeName：对应标签
- nodeType：对应属性
- nodeValue：对应文本
  
- 父节点：parentNode
- 子节点：childNodes可以得到所有子节点，但是兼容性很差



### 操作dom树

**appendChild方法**

	如果把元素A中的子元素A0通过该方法添加到另外一个元素B中去，那么原来的元素A将失去子元素A0（可能由于dom中各个元素只能有一个父节点）；该功能类似于剪切粘贴的操作。



**insertBefore方法**

	用法： `父节点.insertBefore(新节点，旧节点)`，可以实现在旧节点之前添加新节点，并且使得新节点同样位于父节点之下；





### innerHTMl属性

	这个属性不是dom的组成部分，同时，多数浏览器也支持这个属性；
	
	作用：① 获取文本内容； ② 往div中设置内容（可以是HTML代码）





注：javascript编写习惯：每写一行javascript代码，就观察一下该代码的效果（因为Javascript不是编译型语言）



注意：Day07中的jdk5.0新特性没有看；





## Day 08

### 一、Tomcat

- Tomcat的启动需要在环境变量中设置`JAVA_HOME`;
- WEN-INF目录下的文件不允许浏览器直接访问！



### 二、HTTP协议

	HTTP协议包括请求协议和响应协议，其中，请求协议由客户端的浏览器发送，而响应协议则由服务器发送；



请求协议的格式如下：

```
请求行
头信息：由头名称+头值组成
空行
请求体
```

注意：GET请求没有请求体！但是必须有空行；



响应协议的格式如下：

```
响应行（协议/版本 状态吗 状态吗解析） **注意：状态吗首个数字定义了各种状态
响应头（key/value格式）
空行
响应正文（响应体）
```



表单中的url编码：

	如果是中文，那么先把中文的每个汉字对应转换成三个字节（在utf-8的编码格式下），得到三个数值a~1~、a~2~、a~3~；接着分别将各个数值+128，得到新的三个数值，最后转换成16进制



Refer头

作用：① 统计访问量； ② 防止盗链

原理：根据当前的请求头来判断



状态码：

- 200：请求成功；
- 404：请求的资源没有找到；
- 500：请求的资源找到了，但是服务器内部出现了错误；
- 302重定向，需要浏览器再一次发送一个请求给服务器；服务器发送302响应码会带有一个响应头Location，它指定了请求的URL地址；
- 304：假如浏览器两次请求index.html，如果两次的修改时间是一致的，那么服务器会给浏览器发送304响应码，此时，浏览器会直接从本地缓存中读取index.html；（注意：这个响应码只对html有效）



Tomcat会把jsp（动态资源）转换成静态资源（HTML），这时，浏览器才能解析；

JSP中的meta标签可以模拟响应头



# Day09

### 一、Servlet

#### 1 学习 Servlet 接口

	创建一个类A，实现Servlet接口；



注意：

① 类A中实现的接口方法，多数不由我们来调用；并且Servlet对象也不由我们来创建，他们都是由服务器来调用或创建；（准确来说，生命周期方法由服务器来调用）



如何让浏览器访问Servlet：

1. 给Servlet指定一个Servlet路径（即“绑定”）；而给Servlet绑定路径，需要在`web.xml`中进行配置；
2. 浏览器访问Servlet路径；



	当浏览器第一次发送请求时，Servlet会被创建（执行`init`方法），并被响应（执行`servlce`方法），服务器关闭时会销毁Servlet（执行`destroy`方法）；
	
	一个Servlet类只会被创建一次，如果多个客户端要访问同一个Servlet，那么就会出现线程安全问题（因为Servlet不是线程安全的接口）

总结如下：

1. 生命周期方法：
   - `void init(ServletConfig)`创建之后立即执行
   - `void service(ServletRequest request, ServletResponse)`每次客户端访问时被调用；
   - `void destroy()` 对象被销毁之前执行，用于释放资源等；
2. 特性：
   - 单例，一个类只有一个对象；
   - 线程不安全，但是运行效率高；



#### 2 ServletConfig 对象

	`web.xml`中的配置最终会通过xml解析器加载到内存中去，而一个ServletConfig对象对应一个<servlet>标签中的配置；



技巧：`day09->8.GenericServlet介绍`中11:00~14:00 介绍了多回调的技巧



#### 3 HttpServlet类

从请求到响应方法的流程：

```
① 客户端发出请求（GET或POST请求）；
② Tomcat调用Servlet的生命周期方法(service(ServletRequest, ServletResponse))，然后再该方法中，将参数强制转换为HttpServletRequest和HttpServletResponse，然后调用方法service(HttpServletRequest, HttpServletResponse)；
③ 在第二个service方法中，根据客户端发出的请求时GET还是POST，调用方法doGet()或doPost();	注意：如果客户端中有请求，但是Servlet的实现类中没有覆盖doGet或doPost方法，会出现405错误
```



#### 4 Servlet细节

在服务器启动时创建Servlet：

	利用标签<load-on-startup>来指定在服务器启动时创建Servlet的顺序（值越小，越先被创建）；



路径匹配：

	可以利用通配符`*`进行多个路径的匹配，但是`*`只能出现在路径的两端（最开始和最后），不能出现在中间；





#### 5 ServletContext 对象

	一个项目中只有一个ServletContext对象，因此，可以在任意个Servlet中获取相同的ServletContext对象，同时，使用它也可以在不同的Servlet之间传递信息；



	利用ServletContext对象可以得到初始化参数，但是这个初始化和Servlet初始化参数不一样，它是全局的初始化参数；



#### 6 获取类路径下的资源

	使用`Class`和 `ClassLoader`可以获取类路径资源，其中`ClassLoader`较为常用；
	
	类路径对一个JavaWeb项目而言，就是`/WEB-INF/classes`和（`/WEB-INF/lib`每个jar包）；



##### 用法

利用`ClassLoader`类得到资源文件，参数值是相对于资源目录下的文件，即`WEB-INF/classes`目录；注意，参数前面不用带`/`；

利用`Class`类得到资源文件：

1. 如果参数不带`/`，那么是相对于当前class所在的目录;
2. 如果参数带`/`，那么是相对于类路径下的目录；

注意：一般获取项目根目录，利用ServletContext的对象来获取；



# Day10

## 一、HttpServletResponse

状态码：

200表示成功、302表示重定向（需要添加Location头）、404表示资源没找到、500表示服务区错误；



状态码方法：

`sendError(int sc)`：发送错误码；

`sendError(int sc, String msg)`	：发送错误码的同时捎带一个错误信息；

`setStatus(int sc)`：发送成功的状态码，**可以用来发送302**；



响应头方法：

`setHeader(String name, String value)`：设置单值的响应头；



Servlet的两个流：

`ServletOutputStream`：用来向客户端发送字节流； 用法：`ServletOutputStream out = response.getOutputStream();`

`PrintWriter`：用来向客户端发送字符流，需要设置编码； 用法：`PrintWriter writer = response.getWriter();`

上面提到的两种流不能同时使用；



## 二、HttpServletRequest

获取常用信息：

① 获取客户端IP：`request.getRemoteAddr();`； 用途：封IP;

注意：在Windows7系统中，获取IP地址，可能会出现`0:0:0:0:0:0:0:1`，因为获取的是ipv6地址；

② 获取哦请求方式：`request.getMethod()`，可能是POST或GET；



获取HTTP请求头：

`String getHeader(String name)`：用于单值头；



获取请求参数：

`String getParameter(String name)`：获取请求参数的值（单个值）；

`String getParameterValues(String name)`：获取请求参数的值（多个值）；

`Map<String, String[]> getParameterMap()`：获取所有请求参数，其中，key为参数名，value为参数值；



请求转发和请求包含（注意**“14.请求转发和请求包含、延时请求转发.avi”**这个视频）：

	有时候一个请求需要多个Servlet协作才能完成，所以需要在一个Servlet跳转到另外一个Servlet；

- 一个请求跨多个Servlet，需要使用转发和包含；
- 请求转发：由下一个Servlet完成响应体，当前的Servlet可以设置响应头（留头不留体）；
- 请求包含：两个Servlet共同完成响应体（留头又留体）；

		~~客户端发送一个请求到AServlet，AServlet收到请求后，需要BServlet“协助”（即：一个请求需要2个到多个Servlet才能完成），这时候就需要使用请求转发和请求包含；注意：客户端由始至终只创建了一个请求，而服务器也只发送一个响应给客户端；~~

`RequestDispatcher rd = request.getRequestDispatcher();`：获取转发器；

`rd.forward(request, response)`：请求转发（重点）；

`rd.include(request, response)`：请求包含



request域：

	request中的属性是Servlet和Servlet之间在转发或包含时用来传值的；注意：① 不能跨请求传、取值，只能在一个请求范围中传和取；② 请求参数是客户端发送给服务器的，和request中的属性不同；
	
	Servlet中的三大域对象：request、session、application，它们都有三个方法：

- `void setAttribute(String name, Object object)`：向request中设置
- `Object getAttribute(String name)`
- `void removeAttribute(String name)`



请求转发和重定向的区别：

1. 请求转发所示一个请求一次响应，而重定向是两个请求两次响应；
2. 请求转发中的地址栏没有变化，而重定向中会显示最后一个请求的地址；
3. 请求转发只能转发到本项目其他的Servlet，而重定向不仅能重定向到本项目的其他Servlet，还能重定向到其他项目；
4. 请求转发是服务器行为，只需要给出Servlet路径，而重定向需要给出requestURI（即：包含项目名称）；
5. 请求转发的效率比重定向要高；



## 三、编码与解码

响应编码与解码：

1. 服务器给客户端发送数据时，默认使用的是ISO编码；而浏览器一般使用GBk进行解码；

![](./images/响应编码.jpg)



请求编码与解码：

客户端传递给服务器的数据是如何编码的？

- 如果在地址栏中直接给出参数，那么请求编码使用GBK进行编码的；
- 如果实在页面中点击表单或链接：如果页面的编码是UTF-8的话，那么参数是用UTF-8进行编码；

![](./images/请求编码.jpg)

注意：GET请求设置编码需要到tomcat目录下的`/config/server.xml`中进行设置（但是最好不要用）；而POST直接调用`setCharacterEncoding("utf-8")`即可；

![修改Tomcat的server.xml文件](./images/GET请求编码.bmp)

URL编码：

	表单的类型：`ContentType: application/x-www-form-urlencoded`：把中文转成`% + 两位的16进制编码`，它不是编码格式，而是在字符编码（GBk等）基础上再进行转换；
	
	在客户端发给服务器的	GET请求时，如果请求参数包含中文，该请求不会使用URL编码，此时，有可能出现丢失字节的现象；
	
	**今后，我们需要把超链接中的中文，使用URL进行编码；**



## 四、路径

- web.xml中<url-pattern>路径，要么以`*`开头，要么以`/`开头，相对于当前项目；
- 转发和包含路径：
  - 以`/`开头，那么是相对于当前项目路径；（尽量使用这种方式）
  - 不以`/`开头，相对于当前Servlet路径；
- 重定向路径（客户端路径）：
  - 以`/`开头，相对于当前主机（即：`http://localhost`）
- 页面中的超链接和表单路径：
  - 与重定向相同，都是客户端路径，如果以`/`开头，需要添加项目名称；（建议使用这种方式）
  - 如果不以`/`开头，那么相对于当前页面的路径；
- ServletContext获取资源路径：
  - 相对于当前项目目录；
- ClassLoader获取资源路径：
  相对于类路径下获取资源；（注意：参数不能以`/`开头）
- Class获取资源路径：
  - 以`/`开头，相对于`WEB-INF/classes`目录;
  - 不以`/`开头，相对于当前类字节码`.class`所在的目录（即，需要带上当前类的包名）；



# Day11

## 一、JSP

JSP的作用：

- Servlet优缺点：

  - 缺点：不适合设置HTML响应体，如`response.getWriter().print("<html>")`；
  - 优点：动态资源，可以变成；

- HTML优缺点：

  - 缺点：html是静态资源页面，不能包含动态信息；
  - 优点：不用输出html标签；

- JSP（java server page）

  - 优点：在原有html的基础上添加java脚本

  它是服务端页面，不能被客户端所识别；



JSP和Servlet的分工：

- JSP作为请求发起页面，例如：显示表单、超链接；同时，也作为请求结束页面，例如显示数据；
- Servlet作为请求中处理数据的环节；



JSP组成

JSP = html + java脚本 + jsp标签；

JSP中无需创建即可使用的对象有9个，称为9大内置对象；

3中java脚本：

- `<%...%>`：java代码片段，用于定义0~N条java语句（注意，不能定义方法）；
- `<%=...%>`：java表达式，常用于输出一条表达式的结果；
- `<%!...%>`：生命，用来创建类的成员变量和成员方法（基本不用）；



注意：

1. JSP页面中，如果有`<base href="...">`，那么在这个页面上的所有`<a href="a0">`，如果a0不以`/`开头，那么a标签的超链接都是相对于`base`的；（视频：“**3.jsp中java脚本的使用**”）



JSP原理：

​	JSP其实是一种特殊的Servlet；① 当jsp页面被第一次访问时，服务器会把jsp文件编译成Java文件（继承了Servlet类），然后再把java文件编译成.class文件，最后创建该类对象，最后调用service方法；② 第一次请求后，如果再有请求，那么直接调用service方法即可；

​	`tomcat/work`目录下可以找到某个jsp对应的java源码；

 

## 二、Cookie

​	Cookie是HTTP协议制定的！先由服务器保存Cookie到浏览器，等下次浏览器请求服务器时把上一次的请求得到的Cookie归还给服务器；Cookie是一个键值对（只有一个键一个值）

特点：

- 每一个由服务端发送到客户端的Cookie的大小是有限制的；
- 客户端保存在本地的Cookie的总大小也是有限制的；
- Cookie是不能跨浏览器的！



Cookie用途：

- 服务器用Cookie来跟踪客户端的状态；
- 保存历史浏览记录（例如购物网站）；
- 显示登录名；



JavaWeb中使用Cookie：

便捷方式：`response.addCookie()`和`request.getCookies()`；



Cookie详解：

Cookie的maxAge：指的是Cookie的最大生命时长，以秒为单位；

- `maxAge>0`：浏览器会把Cookie保存到客户机的硬盘上，有效时长为maxAge；
- `maxAge<0`：Cookie只在内存中存在，当用户关闭浏览器时，Cookie也被释放了；
- `maxAge==0`：浏览器会马上删掉这个Cookie（如果客户机上存在同名Cookie，那么也会把客户端的Cookie删掉）；

Cookie的path：Cookie的path是由服务器创建Cookie时设置的，当浏览器访问服务器某个路径时，需要归还的Cookie，是由path所决定的：当浏览访服务器的路径$p_0$包含Cookie的path时，就会把该Cookie带上并发给服务器；（注意：path不是值Cookie保存在客户机硬盘上的路径！）



## 三、HttpSession

概述：

- HttpSession是由JavaWeb提供的（不是由Http协议本身所定义的），用来绘画跟踪的类。`session`是服务端对象，保存在服务端。（而Cookie和Http协议相关的，而且保存在客户机上）



HttpSession的作用：

- 会话范围：会话范围是某个用户从首次访问服务器开始，到该用户关闭浏览器结束；会话是指一个用户对服务器多次连贯性请求，而连贯性指的是该用户多次请求中间没有关闭浏览器（关闭浏览器后重新打开，并访问服务器，这时是第二次会话了）；
- session是基于会话而建立的，存活于会话的范围内；一个用户只能有一个session（如果打开两个浏览器并访问同一个网站，这时建立了两个session）；



HttpSession原理：

​	当客户端第一次访问服务器时，服务器会创建一个Session，保存在服务器端，而这个Session的标志ID，则会通过Cookie返回给客户端；当下一次客户端再次访问服务器时，在Cookie中捎带的ID会识别出是服务器的哪一个Session，即找到了原先的Session；

​	当用户关闭客户端时，保存在客户端的ID就会被清空，因此，即使在服务器存在着Session，也因为没有ID而找不到对应的Session；此外，如果客户端长时间没有访问服务器，服务器也会把这个Session删除，此时需要重新创建新的Session。



​	但是，服务器并不是在客户端第一次访问时就创建Session，而是第一次调用`request.getSession()`方法时才会创建；关于`getSession()`方法，见下：

- 如果没有`sessionId`或`sessionId`对应的`session`不存在，那么服务器会创建一个`Session`；
- 如果既有`sessionId`又有`sessionId`对应的`Session`，那么直接返回这个`Session`对象；

注意：如果浏览器直接访问`servlet`那么需要调用方法`request.getSession()`如果浏览器访问了`jsp`页面，那么默认就调用了`request.getSession()`;





# Day12

## 一、JSP的三大指令

格式：

`<%@page 属性名称="属性值" 属性名="属性值"%>`

- 属性`pageEncoding`：指定当前JSP页面的编码，在服务器把jsp编译成.java文件时需要使用`pageEncoding`；
- `contentType`：表示添加一个响应头`Content-Type`，设置页面的编码；
- 如果上面提及的两个属性只提供一个，那么另一个的默认值也跟随着被设置的属性的值；如果两个属性都没有设置，那么默认为iso编码；
- `errorPage`属性：指定当前页面出错时，将会被转发到哪一个页面；
  注意：当前页面出现错误时，如果指定了`errorPage`，那么就相当于设置了`try...catch...`，其中`errorPage`所指定的值在catch部分执行；最后的状态码是200；
- `isErrorPage`：指定当前页面是否为处理错误的页面，如果值为`true`，那么当从别的页面跳转到当前页面（即错误页面）时，状态码为500；
  注意：这个页面会设置状态码为500，并且还可以使用9大内置对象中的`exception`；



## 二、九大内置对象

- out：JSP输出流对象；
- page：当前JSP的对象，它的类型是Object类型（即：在JSP转化为java代码时，代码中有`Object page = this;`
- config：对应“真身”中的ServletConfig对象；
- pageContext；
- request；
- response
- exception
- session
- application



pageContext：

​	Servlet中拥有三大域，而JSP除了可以访问这三大域以外，还拥有pageContext域对象；

  用途：

① 域对象，域范围是当前JSP页面，利用它可以在当前JSP以及当前JSP页面中使用的标签之间共享数据；

② 代理其他域，例如：`pageContext.setAttribute("xxx", "xxx",PageContext.SESSION_SCOPE) `；

③ 获取其他八个内置对象；

④ 全域查找：`pageContext.findAttribute("xxx");`，根据域范围，从小到大，依次查找；

注意：page指的是当前JSP页面的对象，pageContext指的是page的域，是一个域对象；





## 三、JSP指令

**include指令（静态包含）：**

​	该指令的功能与RequestDispatcher的include方法相似，但是，该指令`<%include%>`是在JSP被编译成java文件时完成的，他们共同生成一个Servlet；而RequestDispatcher的include则是一个方法，包含和被包含的是两个Servlet，他们没有被合并为一个文件，只是想“协作”关系；

​	注意：被包含的页面不能使变量！例子如下：

① 在a.jsp页面中有如下代码：

```jsp
........
<%
	String pagePath = "指向b.jsp的路径";
%>
<%@include file="<%=pagePath %>"%>
........
```

② 因为`<%include%>`指令是在合并成java文件时执行的（Java文件级别进行合并），而`<%=pagePath %>`只有在运行时才能确定，因此，不能找到对应的文件进行合并；



​	这个指令的作用是：可以把页面分解为几个部分，把每个页面的不变的部分提取出来，变化的部分被不变的页面include进去；





**taglib标签指令**

​	这个指令可以用来导入标签库，有两个属性`prefix`和`uri`。



## 四、JSP动作标签

​	JSP动作标签是由服务器来解释执行的，而html标签则是由浏览器来解释执行，两者有着本质的区别。

标签如下：

- `<jsp:forward>`：转发，与RequestDispatcher的forward方法相同；
- `<jsp:include>`：包含；
  注意：厘清`<%@include%>`和`<jsp:include>`有什么不同；
- `<jsp:param>`：用来作为forward或include标签的子标签，用来传递参数



JSP中和JavaBean相关的bean：

- `<jsp:useBean>`：创建或查询bean，如果查询不到，即创建；
- `<jsp:setProperty>`：设置bean的属性值；
- `<jsp:getProperty>`：获取bean的属性值；



## 五、JavaBean

​	JavaBean实际上是一个Java文件，需要为该类提供get/set方法（只选其一也是可以的），同时必须要有一个默认构造器（无参构造器）；具体见下面代码：

```java
package cn.itcast.domain;

public class Person {

    private String username;
    private String password;
    private int age;

    // 实际上并不需要类中拥有一个成员，只需要有一个方法即可，方法会被转换为“去掉get/set后的、首字母小写的名称  所对应的属性”
    public String getName() {
        return "你想要返回的字符串";
    }

	/**
	* 为每个属性提供get/set方法
	*/
    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}

```



**JavaBean规范：**

1. 必须提供一个默认构造器；
2. 为属性提供get/set方法，如果只有get方法，那么这个属性是只读的；
3. 属性：可以对应get/set方法的成员，也可以不用对应；此外，属性的名称由`get/set方法来指定`



**内省：**

流程：内省类-->Bean信息-->属性描述符数组-->单个属性描述符的get/set方法-->接着可以利用反射机制来执行方法。



**BeanUtils的使用：**

**见“BeanUtils的使用”20:30~最后**



## 六、EL表达式

​	EL表达式是JSP内置的表达式语言（由于是表达式，因此后面不需要加分号）。JSP2.0开始，要求不能使用java脚本，而EL表达式是用来取代`<%=%>`语句的，因此EL表达式只能用作输出。



EL表达式用来读取四大域：

- `${xxx}`：全域查找名为xxx的属性，如果没找到，那么输出空字符串（而不是null）；
- 用指定域中查找属性：`${pageScope.xxx}`；（注意：后面的“Scope”不能丢）
- 



JavaBean导航：

​	假设有一个bean为`Employee`，而`Employee`中含有属性`Address`，`Address`中含有属性`street`，那么，当把`Employee`对象设置到某个域中（例如request域中），此时，可以利用EL表达式来获取`street`的值；语法如下：

`requestScope.emp.address.street`。



EL内置对象：

- 前面四个为`pageScope、requestScope、sessionScope、applicationScope`；
- `param`：对应参数，是一个`Map<String, String>`，适用于单值属性；
- `paramValues`：对应参数，是一个`Map<String, String[]>`，适用于多值属性；
- `header`和`headerValues`：对应请求头，内容和`param`、`paramValues`相似；
- `initParam`：获取`<context-param>`定义的参数；
- `cookie`：是`Map<String, Cookie>`类型，根据键得到的值是`Cookie`类型，因此，还需要调用相关方法`getName()`、`getValue()`才能得到对应的名称或值；
- `pageContext`：对应`PageContext`对象；



自定义函数库<u>（见视频“15.EL自定义函数库.avi”）</u>：

- 写一个java类，类中可以定义0~N个方法，每个方法必须是`static` 并且有返回值；
- 在`WEB-INF`m目录下创建一个tld文件，并参考`jstl.jar`中的模板，编写tld文件；
- 最后，在JSP页面中导入标签，并使用标签；





# Day 13

## 一、JSTL的概述

​	JSTL是apache对EL表达式的扩展，使用JSTL标签需要导入`jstl.jar`；



**四大库：**

- core：核心库；
- fmt：格式化库，常用的格式化需求有数字、日期；
- sql：
- xml：



**导入标签库：**

- 导入jar包；
- 在JSP页面中，使用指令`<%@ taglib prefix="前缀" uri="路径"%>`



**core：**

1. out和set:
   - `<c:out>`：输出
     - `value`：可以是字符串常量，也可以是EL表达式
     - `default`：当要输出的被容为`null`时，会输出default所对应的值；
     - `escapeXml`：默认值为true，表示将内容转义；

   - `<c:set>`：设置（创建）域的属性

     `var`-->变量名， `value`-->变量值， `scope`-->域，默认为page；

2. remove：
   删除域变量，其中`var`表示变量名，`scope`表示待删除的域，如果没有指定`scope`对象，那么默认删除所有域中的变量名；

3. url
   url标签可以指定路径，同时，也可以为路径追加请求参数，用法如下：

   - `<c:url value="/index.jsp" />`：生成的最终路径为`/项目名称/index.jsp`;

   - ```jsp
     <c:url>
         <c:param name="username" value="张三" />
         ...
     </c:url>
     最终生成的路径为：/项目名称/index.jsp?username=%XX%XX...(即自动进行url编码)
     ```

   `var`：指定变量名，当设置了这个属性时，url标签就不会输出到页面上，而是把url保存到域中，其中`scope`指定域。

4. `if`标签和`choose`标签：
   `if`对应java中的if语句，`choose`对应java中的if...else if ... else if ... ... else...语句。

5. ==forEach标签：==
   该标签可以用来遍历数组、集合，同时，还可以用来进行计数方式的循环；

   - `var` ：循环变量，对应java中for语句的`int i`；
   - `begin`：设置循环变量的起始值；
   - `end`：设置循环变量的终止值（包含终止值）；
   - `step`：设置步长；

   上面的是计数方式的循环；下面介绍遍历数组和集合：

   - `items`：指定要循环的数组或集合；**注意：EL表达式后、双引号前不能有空格！（`items="${requestScope.xxx }"`）**
   - `var`：把数组或集合中的每个元素赋值给该变量；

   此外，还可以使用`varStatus`来创建循环状态变量，用法如下：

   - `count`：循环元素的个数；
   - `index`：循环元素的下标；
   - `first`：是否为第一个元素；
   - `last`：是否为最后一个元素；
   - `current`：当前元素；

注意：填写uri路径时，不要导入错误的uri，正确的uri为：`http:..java.sun.com/jsp/jstl/core`



**fmt库：**

​	fmt库是一个格式化库。

1. `<fmt:formatDate value="" pattern="" />`：用来输出一个由`value`指定的Date类型、`pattern`指定的格式的字符串；
2. `<fmt:formatNumber value="" pattern="0.00"/>`：根据`pattern`输出保留指定位数的数字字符串（例子中是保留小数点后两位，如果小数点后面不足两位，那么补位，会四舍五入）；
3. `<fmt:formatNumber value="" pattern="#.##"/>`：根据`pattern`输出保留指定位数的数字字符串（例子中是保留小数点后两位，如果小数点后面不足两位，那么不补位，会四舍五入）；



## 二、自定义标签



### 步骤：

1. 编写自定义标签类；
2. 编写tld文件，将自定义标签类中的方法定义在tld文件中；
3. 在JSP页面中引入tld文件：`<%@ taglib%>`；



### 标签处理类（没有在idea中运行起来）

`SimpleTag`接口：

- `void doTag()`：每次执行标签时都会调用这个方法；
- `JspTag getParent()`：获取父标签；（非生命周期方法）
- `void setParent(JspTag)`：设置父标签；
- `void setJspBody(JspFragment)`：设置标签体；
- `void setJspContext(JspContext)`：设置JSP上下文；

其中，`doTag()`方法在后三个方法执行后再被tomcat调用；



`SimpleTagSupport`类：

​	该类继承了`SimpleTag`接口，同时封装了若干个成员，以及成员的get/set方法；



### 标签体内容

- `empty`：无标签体；
- `JSP`：表示标签体的内容可以是Java脚本、标签、也可以是EL表达式，但是在JSP2.0以后已经不再支持这个类型了；
- `scriptless`：只能是EL表达式，也可以是其他标签（这时就出现了“父标签”的概念）；

用法如下：

```java
package cn.itcast.tag;

import javax.servlet.jsp.JspException;
import javax.servlet.jsp.tagext.SimpleTagSupport;
import java.io.IOException;
import java.io.Writer;

public class MyTag3 extends SimpleTagSupport {
    @Override
    public void doTag() throws JspException, IOException {
        // ① 执行某一些动作
        
        // ② 再输出标签体
        // 先获取流对象
        Writer out = getJspContext().getOut();
        getJspBody().invoke(out);
        
        // ③ 再执行某些动作
        
    }
}

```



另：可以实现一种标签，这种标签后面的内容将完全忽略，实现方法如下：① 实现`SimpleTagSupport`类，并重载`doTag()`方法； ② 在`doTag()`方法中，抛出异常`throw new SkipPageException()`；	这个`SkipPageException`会忽略该标签后的所有内容，但是Tomcat会捕捉到它，并处理掉异常，因此，不会影响其他页面。

​	<u>具体分析见“**11.自定义标签之SkipPageException，不再执行标签下面的内容.avi**”</u>。可以参考其方法来分析源码。





### 标签属性

​	可以为标签添加属性，例如`<c:if test=""/>`中的`test..`就是属性；

步骤：

1. 给标签处理类添加属性
   注意：属性至少需要一个`set`方法，`set`方法会在`doTag`方法之前被Tomcat调用，因此可以直接使用属性；

2. 在tld文件中对属性进行配置：

   ```xml
   在<tag>中写上：
       <attribute>
       	<name></name>  指定属性名称
           <required></required>	指定是否为必需的
           <rtexprvalue></rtexprvalue>	指定是否能使用EL表达式
       </attribute>
   ```


## 三、MVC设计模式和JavaWeb三层架构

​	MVC设计模式是独立于语言的，不是Java所独有的；而JavaWeb三层架构则是JavaWeb所独有的。



### JavaWeb三层架构：

- Web层；与Web相关的内容（Servlet， JSP， Servlet相关的API）；有时候，B/S架构和C/S架构可以重用业务层和数据层，而Web层则是B/S所独有的；
- 业务层；（可以理解为将数据的零散操作聚集为一个功能集合
- 数据层；（可以理解为数据的一些零散操作）；所有对数据库的操作，不能跳出到DAO之外；





# Day 14

dao层直接copy其代码即可；