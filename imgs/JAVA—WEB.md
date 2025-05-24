---

---

typora-copy-images-to: javaweb

# HTML

## 参考

https://www.w3cschool.cn/html/html-form.html

## 基本语法

![image-20241105214019480](https://raw.githubusercontent.com/blkheadfish/picGo/main/imgs/image-20241105214019480.png)

### 基本结构

![image-20241105214231412](https://raw.githubusercontent.com/blkheadfish/picGo/main/imgs/image-20241105214231412.png)

不允许交叉嵌套

```html
正确：
<div>
    <a></a>
</div>
错误：
<div>
    <a>
</div>
    </a>
```

![image-20241105214602794](C:\Users\27251\Desktop\笔记\javaweb\image-20241105214602794-1745151037783.png)

```html
<DOCTYPE html>
<!--这个头部是为了告诉浏览器解析HTML的标准
HTML分为HTML,xhtml,HTML5等不同版本
>    
```

```html
<DOCTYPE html>
    <html lang="en">

    <head>
        <meta charset="utf-8">
        <title>
            test
        </title>
    </head>

    <body>

    </body>

    </html>
```

vscode中输入！+tab可以自动补全

简单页面小代码

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>测试</title>
    </head>
    <body>
        <h1>欢迎来到测试页面</h1>
        <a href="https://space.bilibili.com/375081822/favlist?fid=3135803622&ftype=create ">好康的</a>
    </body>
</html>
```

效果![image-20241105220636597](C:\Users\27251\Desktop\笔记\javaweb\image-20241105220636597.png)

![image-20241105220543803](C:\Users\27251\Desktop\笔记\javaweb\image-20241105220543803.png)

### 头部信息

![image-20241105220737041](C:\Users\27251\Desktop\笔记\javaweb\image-20241105220737041.png)

### 常用标签

![image-20241106150120812](C:\Users\27251\Desktop\笔记\javaweb\image-20241106150120812.png)

```html
<b></b>
<strong></strong>
<!--区别在于strong标签可以优先被搜索引擎找到-->
```

![image-20241106150914285](C:\Users\27251\Desktop\笔记\javaweb\image-20241106150914285.png)

列表中也可以放链接

```html
    <ul>
        <li><a href="https://space.bilibili.com/375081822/favlist?fid=3135803622&ftype=create">好康的</a></li>
        <li><a href="https://www.baidu.com">好用的</a></li>
        <li>ccc</li>
    </ul>
```

<img src="C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20241106152130453.png" alt="image-20241106152130453" style="zoom:100%;" />

![image-20241106152446484](C:\Users\27251\Desktop\笔记\javaweb\image-20241106152446484.png)

锚点就像goto和标签,#作用是定位,比如./h1.html#chiikawa1意思就是跳转到h1.html下的chiikawa1锚点

![image-20241106153736437](C:\Users\27251\Desktop\笔记\javaweb\image-20241106153736437.png)

合并单元格：由左向右,由上到下

![image-20241106154356090](C:\Users\27251\Desktop\笔记\javaweb\image-20241106154356090.png)

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="./h1.html" method="GET"><!--用get方法将参数传到./h1.html-->
        <input type="text" name="uname"><br/><br/><!--type表示表单类型,文本框,密码框,提交按钮-->
        <input type="password" name="upass"><br/><br/>
        <input type="submit" value="登录">
    </form>
</body>
</html>
```

![image-20241106160459005](C:\Users\27251\Desktop\笔记\javaweb\image-20241106160459005.png)

![image-20241106160622879](C:\Users\27251\Desktop\笔记\javaweb\image-20241106160622879.png)

# CSS

![image-20241112204644589](C:\Users\27251\Desktop\笔记\javaweb\image-20241112204644589.png)

## 语法

![image-20241112210952820](C:\Users\27251\Desktop\笔记\javaweb\image-20241112210952820.png)

选择器：选的是<body>中的标签名</body>

```html
<!--css样式位于style标签中-->
<!DOCTYPE html>
<html>
<head>
    <meta charset="GBK">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        strong{font-size: 20;color: aquamarine;}
    </style>
</head>
<body>
    <strong>这是CSS测试页面</strong>
    <ul>
        <li>
            <a href="https://www.bilibili.com">学习网站</a>
        </li>
        <li>CSS测试</li>
        <li>油专</li>
    </ul>
</body>
</html>
```

## 使用方法

![image-20241112211552861](C:\Users\27251\Desktop\笔记\javaweb\image-20241112211552861.png)

1.外部样式表：

![image-20241112214706096](C:\Users\27251\Desktop\笔记\javaweb\image-20241112214706096.png)

html中用link单标签引用

```css
/*mycss.css*/
h1{font-size: 30;background-color: aquamarine;color: crimson;}
```

2.内嵌方法

嵌入在style中

3.内联样式

```html
<!-- 直接将style写入标签中-->
<ul>
    <li style="font-size:25;color:red"></li>
</ul>
```

## CSS2常用选择器

![image-20241113143203446](C:\Users\27251\Desktop\笔记\javaweb\image-20241113143203446.png)

### html选择器

把html的标签作为选择器,比如h1,a,也可以用*表示对所有标签生效（可能有兼容性问题）

缺点：过于笼统,html中有很多标签是重复的

### 类选择器

在标签中加入class属性,在创建css样式时用  （标签名）.属性值进行标记

属性名可写可不写,不写属性名,那么只要class属性值等于css样式前的类属性值,css就会对该标签生效

![image-20241113145110647](C:\Users\27251\Desktop\笔记\javaweb\image-20241113145110647.png)

### id选择器

根据标签中的id属性的属性值进行选择

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="GBK">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #hid{font-size: 20;color: aquamarine;}/*#开始*/
    </style>
    
</head>
<body>
    <strong>这是CSS测试页面</strong>
    <ul>
        <li id="hid">
            <a href="https://www.bilibili.com">学习网站</a>
        </li>
        <li>CSS测试</li>
        <li>油专</li>
    </ul>
</body>
</html>
```

![image-20241113151502621](C:\Users\27251\Desktop\笔记\javaweb\image-20241113151502621.png)

### 关联选择器/包含选择器

![image-20241113151832026](C:\Users\27251\Desktop\笔记\javaweb\image-20241113151832026.png)

### 组合选择器

![image-20241113151857100](C:\Users\27251\Desktop\笔记\javaweb\image-20241113151857100.png)

### 伪类选择器![image-20241113152003635](C:\Users\27251\Desktop\笔记\javaweb\image-20241113152003635.png)

## 常用属性

![image-20241116141614334](C:\Users\27251\Desktop\笔记\javaweb\image-20241116141614334.png)

### 尺寸与单位

![image-20241116141922772](C:\Users\27251\Desktop\笔记\javaweb\image-20241116141922772.png)

### 颜色

![image-20241116142012471](C:\Users\27251\Desktop\笔记\javaweb\image-20241116142012471.png)

![image-20241116142144234](C:\Users\27251\Desktop\笔记\javaweb\image-20241116142144234.png)

### 字体属性font

![image-20241116142434890](C:\Users\27251\Desktop\笔记\javaweb\image-20241116142434890.png)

![image-20241116143211419](C:\Users\27251\Desktop\笔记\javaweb\image-20241116143211419.png)

### 文本属性

![image-20241116143406170](C:\Users\27251\Desktop\笔记\javaweb\image-20241116143406170.png)

![image-20241116143422896](C:\Users\27251\Desktop\笔记\javaweb\image-20241116143422896.png)

# JavaScript

![image-20241119164618385](C:\Users\27251\Desktop\笔记\javaweb\image-20241119164618385.png)

## 引入方式

![image-20241119165144002](C:\Users\27251\Desktop\笔记\javaweb\image-20241119165144002.png)

## 书写语法

![image-20241119165641575](C:\Users\27251\Desktop\笔记\javaweb\image-20241119165641575.png)

![image-20241119165911317](C:\Users\27251\Desktop\笔记\javaweb\image-20241119165911317.png)

## 变量

![image-20241119170445990](C:\Users\27251\Desktop\笔记\javaweb\image-20241119170445990.png)

![image-20241119170644091](C:\Users\27251\Desktop\笔记\javaweb\image-20241119170644091.png)

![image-20241119170730015](C:\Users\27251\Desktop\笔记\javaweb\image-20241119170730015.png)

## 数据类型&运算符

![image-20241119170948064](C:\Users\27251\Desktop\笔记\javaweb\image-20241119170948064.png)

![image-20241119171037540](C:\Users\27251\Desktop\笔记\javaweb\image-20241119171037540.png)

![image-20241119171256783](C:\Users\27251\Desktop\笔记\javaweb\image-20241119171256783.png)

![image-20241119171419300](C:\Users\27251\Desktop\笔记\javaweb\image-20241119171419300.png)

![image-20241119171550102](C:\Users\27251\Desktop\笔记\javaweb\image-20241119171550102.png)

![image-20241119171612159](C:\Users\27251\Desktop\笔记\javaweb\image-20241119171612159.png)

<u>***parseInt()会从第一个字符开始匹配,直到遇到第一个非数字停止转换；所以如果转换的内容第一个字符就不是数字,转换结果就是NaN***</u>

![image-20241119172004670](C:\Users\27251\Desktop\笔记\javaweb\image-20241119172004670.png)

## Day02-06. JS-函数

![image-20241119172350774](C:\Users\27251\Desktop\笔记\javaweb\image-20241119172350774.png)

![image-20241119172541604](C:\Users\27251\Desktop\笔记\javaweb\image-20241119172541604.png)

js函数可以接收任意个数参数,有几个形参就接收前几个参数

## Day02-07. JS-对象-Array数组

![image-20241119172827435](C:\Users\27251\Desktop\笔记\javaweb\image-20241119172827435.png)

![image-20241119173017067](C:\Users\27251\Desktop\笔记\javaweb\image-20241119173017067.png)

![image-20241119173224884](C:\Users\27251\Desktop\笔记\javaweb\image-20241119173224884.png)

```js
var arr = [1,2,3,4];
arr[10] = "佐佐木淳平";
arr.forEach(function(e){//相当于匿名内部类
    console.log(e);
})
//箭头函数简化（lambda表达式）
var arr = [1,2,3,4];
arr[10] = "佐佐木淳平";
arr.forEach((e)=>{
    console.log(e);
})

//splice()参数1：起始索引 参数2：删除个数
```

## Day02-08. JS-对象-String字符串

![image-20241119174136829](C:\Users\27251\Desktop\笔记\javaweb\image-20241119174136829.png)

![image-20241119174205541](C:\Users\27251\Desktop\笔记\javaweb\image-20241119174205541.png)

substring参数1：开始索引,参数2：结束索引；左闭右开

## Day02-09. JS-对象-JSON

![image-20241119174436326](C:\Users\27251\Desktop\笔记\javaweb\image-20241119174436326.png)

函数简化写法：

```
函数名(){

}
```

![image-20241119174651818](C:\Users\27251\Desktop\笔记\javaweb\image-20241119174651818.png)

![image-20241119174803855](C:\Users\27251\Desktop\笔记\javaweb\image-20241119174803855.png)

***key-value形式***

***key必须用双引号包围***

![image-20241119175056791](C:\Users\27251\Desktop\笔记\javaweb\image-20241119175056791.png)

![image-20241119175150122](C:\Users\27251\Desktop\笔记\javaweb\image-20241119175150122.png)

```js
var json_str = '{"name":"wwwtty","password":114514}';
var json_obj = JSON.parse(json_str);
var json_str = JSON.stringify(json_obj);
alert(json_obj.name);
alert(json_str);
```



## Day02-10. JS-对象-BOM

![image-20241119185453379](C:\Users\27251\Desktop\笔记\javaweb\image-20241119185453379.png)

![image-20241119193346757](C:\Users\27251\Desktop\笔记\javaweb\image-20241119193346757.png)

```js
var res = window.confirm();//确认为true,取消为false
if(res){
    alert("确定");
}else{
    alert("取消");
}
```

![image-20241119194157829](C:\Users\27251\Desktop\笔记\javaweb\image-20241119194157829.png)

```js
alert(location.href);
location.href="https://www.bilibili.com";//跳转到该网址
```

## Day02-11. JS-对象-DOM

![image-20241119195159129](C:\Users\27251\Desktop\笔记\javaweb\image-20241119195159129.png)

## Day02-12. JS-对象-DOM案例

![image-20241119195435377](C:\Users\27251\Desktop\笔记\javaweb\image-20241119195435377.png)

![image-20241119195552066](C:\Users\27251\Desktop\笔记\javaweb\image-20241119195552066.png)

可以用.innerHTML=修改div标签内文本内容

## Day02-13. JS-事件-事件绑定&常见事件

![image-20241119201210647](C:\Users\27251\Desktop\笔记\javaweb\image-20241119201210647.png)

![image-20241119201342163](C:\Users\27251\Desktop\笔记\javaweb\image-20241119201342163.png)

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>测试</title>
</head>
<body>
    <form action="" method="get">
        <input type="button" value="点我" id="hhh">
    </form>
    <script>
        function on(){
            alert("点我干嘛?");
        }
        document.getElementById("hhh").onclick=function(){
            alert("干嘛点我");
        }


    </script>
</body>
</html>
```

![image-20241119202455816](C:\Users\27251\Desktop\笔记\javaweb\image-20241119202455816.png)

焦点：比如光标在输入框中闪烁

## Day02-14. JS-事件-案例



# Vue

## Day02-15. Vue-概述

![image-20241119203955051](C:\Users\27251\Desktop\笔记\javaweb\image-20241119203955051.png)

![image-20241119204210374](C:\Users\27251\Desktop\笔记\javaweb\image-20241119204210374.png)

## Day02-16. Vue-指令-v-bind&v-model&v-on

## Day02-17. Vue-指令-v-if&v-show&v-for

## Day02-18. Vue-指令-案例

## Day02-19. Vue-生命周期



# Ajax

# nginx打包部署

```bash
#vue项目目录下
npm run build
```

打包好后会有一个dist文件夹

部署：将dist复制到nginx的/html中,启动nginx.exe 占用80端口（默认）

![image-20250416204044806](C:\Users\27251\Desktop\笔记\javaweb\image-20250416204044806.png)

![image-20250416204440011](C:\Users\27251\Desktop\笔记\javaweb\image-20250416204440011.png)

若端口被占用,在nginx.conf里更改

# Maven

![image-20241120164940486](C:\Users\27251\Desktop\笔记\javaweb\image-20241120164940486.png)

![image-20241120165923695](C:\Users\27251\Desktop\笔记\javaweb\image-20241120165923695.png)

![image-20241120173152507](C:\Users\27251\Desktop\笔记\javaweb\image-20241120173152507.png)

![image-20241120174537451](C:\Users\27251\Desktop\笔记\javaweb\image-20241120174537451.png)

![image-20241124202223071](C:\Users\27251\Desktop\笔记\javaweb\image-20241124202223071.png)

![image-20241124202556434](C:\Users\27251\Desktop\笔记\javaweb\image-20241124202556434.png)

## 依赖配置

![image-20241124202749916](C:\Users\27251\Desktop\笔记\javaweb\image-20241124202749916.png)

```xml
        <dependencies>
                <dependency>
                        <groupId>ch.qos.logback</groupId>
                        <artifactId>logback-classic</artifactId> <!--先写这个,其他idea可以代码提示-->
                        <version>1.5.6</version>
                </dependency>
        </dependencies>
```

![image-20241124203647719](C:\Users\27251\Desktop\笔记\javaweb\image-20241124203647719.png)

## 依赖传递

![image-20241124203856449](C:\Users\27251\Desktop\笔记\javaweb\image-20241124203856449.png)

### 排除依赖![image-20241124204124508](C:\Users\27251\Desktop\笔记\javaweb\image-20241124204124508.png)

## 依赖范围

![image-20241124205452618](C:\Users\27251\Desktop\笔记\javaweb\image-20241124205452618.png)

## 生命周期

![image-20241124211735777](C:\Users\27251\Desktop\笔记\javaweb\image-20241124211735777.png)

![image-20241124211752639](C:\Users\27251\Desktop\笔记\javaweb\image-20241124211752639.png)

![image-20241124211957736](C:\Users\27251\Desktop\笔记\javaweb\image-20241124211957736.png)

![image-20241124212032323](C:\Users\27251\Desktop\笔记\javaweb\image-20241124212032323.png)

# SpringBoot

![image-20250417203457434](C:\Users\27251\Desktop\笔记\javaweb\image-20250417203457434.png)

![image-20241124214239548](C:\Users\27251\Desktop\笔记\javaweb\image-20241124214239548.png)





![image-20241124214652524](C:\Users\27251\Desktop\笔记\javaweb\image-20241124214652524.png)

![image-20250416205936107](C:\Users\27251\Desktop\笔记\javaweb\image-20250416205936107.png)

<img src="C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250416210249296.png" alt="image-20250416210249296" style="zoom: 67%;" />

![image-20250416210302032](C:\Users\27251\Desktop\笔记\javaweb\image-20250416210302032.png)

### @RestController

@RestController 通常用于创建 REST API,其中每个方法的返回值都是 HTTP 响应体的一部分。这使得开发人员可以专注于业务逻辑,而不必担心视图解析和模型数据的填充。

### @RequestMapping()注解

```
在 Java 的 Spring 框架中,@RequestMapping注解用于将 HTTP 请求映射到控制器的处理方法上。这个注解可以用于类或方法上,用于定义请求的 URL 模式、HTTP 方法（如 GET、POST）、请求参数、头部信息等。
```

```java
package com.example.demo.controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

//请求处理类
@RestController
public class HelloController {

        //请求路径
        @RequestMapping("/Hello")
        public String Hello(){
                return "Hello SpringBoot";
        }
}

```

# HTTP协议

![image-20241125164413610](C:\Users\27251\Desktop\笔记\javaweb\image-20241125164413610.png)

![image-20241125165152198](C:\Users\27251\Desktop\笔记\javaweb\image-20241125165152198.png)

## 请求数据格式

请求行,请求头,请求体

![image-20241125165931263](C:\Users\27251\Desktop\笔记\javaweb\image-20241125165931263.png)

请求头与请求体之间用空行隔开

![image-20241125170028877](C:\Users\27251\Desktop\笔记\javaweb\image-20241125170028877.png)

### 常见请求头：

![image-20241125165719305](C:\Users\27251\Desktop\笔记\javaweb\image-20241125165719305.png)

User-Agent用于浏览器兼容性处理



## 响应数据格式

相应行,响应头,响应体/响应正文

![image-20241125170308311](C:\Users\27251\Desktop\笔记\javaweb\image-20241125170308311.png)

### 状态码

![image-20241125170408069](C:\Users\27251\Desktop\笔记\javaweb\image-20241125170408069.png)

![image-20241125170527857](C:\Users\27251\Desktop\笔记\javaweb\image-20241125170527857.png)

![image-20241125170725201](C:\Users\27251\Desktop\笔记\javaweb\image-20241125170725201.png)

最常见:![image-20241125170957970](C:\Users\27251\Desktop\笔记\javaweb\image-20241125170957970.png)

### 常见响应头

![image-20241125171113513](C:\Users\27251\Desktop\笔记\javaweb\image-20241125171113513.png)

# Web服务器-Tomcat

![image-20250416211501889](C:\Users\27251\Desktop\笔记\javaweb\image-20250416211501889.png)

## 基本使用

![image-20241125174320885](C:\Users\27251\Desktop\笔记\javaweb\image-20241125174320885.png)

![image-20250416212251052](C:\Users\27251\Desktop\笔记\javaweb\image-20250416212251052.png)

### 端口冲突解决：

![image-20241125173307496](C:\Users\27251\Desktop\笔记\javaweb\image-20241125173307496.png)

## 程序解析

![image-20250416212750472](C:\Users\27251\Desktop\笔记\javaweb\image-20250416212750472.png)

创建springboot项目时要关联start.spring.io,所以创建时需要联网

![image-20250416212848621](C:\Users\27251\Desktop\笔记\javaweb\image-20250416212848621.png)

![image-20250416213051842](C:\Users\27251\Desktop\笔记\javaweb\image-20250416213051842.png)

![image-20250416213101326](C:\Users\27251\Desktop\笔记\javaweb\image-20250416213101326.png)

起步依赖的版本依赖于父工程,版本依赖于父工程版本

![image-20250416213644225](C:\Users\27251\Desktop\笔记\javaweb\image-20250416213644225.png)

Spring Boot-Web的maven依赖中已经内嵌了tomcat

![image-20241125174015658](C:\Users\27251\Desktop\笔记\javaweb\image-20241125174015658.png)

![image-20250416213330507](C:\Users\27251\Desktop\笔记\javaweb\image-20250416213330507.png)

# 请求响应

## 请求

![image-20250416214125055](C:\Users\27251\Desktop\笔记\javaweb\image-20250416214125055.png)

HttpServletRequest称为请求对象

HttpServletResponse称为响应对象

![image-20241204160223484](C:\Users\27251\Desktop\笔记\javaweb\image-20241204160223484.png)

DispatcherServlet称为前端控制器/核心控制器

![image-20241204160805640](C:\Users\27251\Desktop\笔记\javaweb\image-20241204160805640.png)

### postman工具

![image-20241204161524017](C:\Users\27251\Desktop\笔记\javaweb\image-20241204161524017.png)

### 简单参数![image-20241204161631646](C:\Users\27251\Desktop\笔记\javaweb\image-20241204161631646.png)

![image-20241204165153743](C:\Users\27251\Desktop\笔记\javaweb\image-20241204165153743.png) 

```java
package com.example.demo.controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class RequestController {
        @RequestMapping("/Args")
        //请求的参数名与接收参数名必须一致,不然接收到的就是null
        public String RequestController(String name,String passwd){
                String response = name+':'+passwd;
                System.out.println(response);
                return response;
        }
}
```

![image-20250416215444075](C:\Users\27251\Desktop\笔记\javaweb\image-20250416215444075.png)

![image-20241204165500368](C:\Users\27251\Desktop\笔记\javaweb\image-20241204165500368.png)

![image-20241204165558132](C:\Users\27251\Desktop\笔记\javaweb\image-20241204165558132.png)

```java
package com.example.demo.controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class RequestController {
        @RequestMapping("/Args")
        //请求的参数名与接收参数名必须一致,不然接收到的就是null
        public String RequestController(@RequestParam(name = "name",required = true)String name, @RequestParam(name = "passwd") String password){
                String response = name+':'+password;
                System.out.println(response);
                return response;
        }
}
```

![image-20250416215756230](C:\Users\27251\Desktop\笔记\javaweb\image-20250416215756230.png)

![image-20250416215819660](C:\Users\27251\Desktop\笔记\javaweb\image-20250416215819660.png)

![image-20250416215852456](C:\Users\27251\Desktop\笔记\javaweb\image-20250416215852456.png)

### 实体参数

![image-20241204170401173](C:\Users\27251\Desktop\笔记\javaweb\image-20241204170401173.png)

实体都放在pojo下（自己建目录）

![image-20250416220501221](C:\Users\27251\Desktop\笔记\javaweb\image-20250416220501221.png)

![image-20250416220602362](C:\Users\27251\Desktop\笔记\javaweb\image-20250416220602362.png)

至少要有请求参数

![image-20250416220807637](C:\Users\27251\Desktop\笔记\javaweb\image-20250416220807637.png)

```java
@RequestMapping("/simplePojo")
public String simplyPojo(User user){
    System.out.println(user);
    return "OK";
}
```

![image-20250417190259676](C:\Users\27251\Desktop\笔记\javaweb\image-20250417190259676.png)

如果改变参数名字就不能封装进去,参数值为null

![image-20250417190352654](C:\Users\27251\Desktop\笔记\javaweb\image-20250417190352654.png)

![image-20241204171709972](C:\Users\27251\Desktop\笔记\javaweb\image-20241204171709972.png)

请求如下：

**![image-20250417190905367](C:\Users\27251\Desktop\笔记\javaweb\image-20250417190905367.png)**



![image-20250417191007007](C:\Users\27251\Desktop\笔记\javaweb\image-20250417191007007.png)

![image-20250417191130946](C:\Users\27251\Desktop\笔记\javaweb\image-20250417191130946.png)

![image-20250417191330869](C:\Users\27251\Desktop\笔记\javaweb\image-20250417191330869.png)

![image-20250417191437056](C:\Users\27251\Desktop\笔记\javaweb\image-20250417191437056.png)控制台输出

### 数组参数

![image-20250416214712902](C:\Users\27251\Desktop\笔记\javaweb\image-20250416214712902.png)

![image-20250417191956083](C:\Users\27251\Desktop\笔记\javaweb\image-20250417191956083.png)

```java
@RequestMapping("/arrayParam")
public String arrayParam(String[] param){
    System.out.println(Arrays.toString(param));
    return "OK";
}
```

![image-20250417192127800](C:\Users\27251\Desktop\笔记\javaweb\image-20250417192127800.png)

### 集合参数

![image-20250417192219602](C:\Users\27251\Desktop\笔记\javaweb\image-20250417192219602.png)

不用@RequestParam会被解释成数组而非集合

![image-20250417192522019](C:\Users\27251\Desktop\笔记\javaweb\image-20250417192522019.png)

![image-20250417192553966](C:\Users\27251\Desktop\笔记\javaweb\image-20250417192553966.png)

### 日期参数

![image-20250417193302287](C:\Users\27251\Desktop\笔记\javaweb\image-20250417193302287.png)

![image-20250417193712205](C:\Users\27251\Desktop\笔记\javaweb\image-20250417193712205.png)

![image-20250417193742315](C:\Users\27251\Desktop\笔记\javaweb\image-20250417193742315.png)

### json参数

![image-20250417193843243](C:\Users\27251\Desktop\笔记\javaweb\image-20250417193843243.png)

postman请求json参数方法：

![image-20250417194252409](C:\Users\27251\Desktop\笔记\javaweb\image-20250417194252409.png)

url中要加上请求路径,否则报错

![image-20250417194953911](C:\Users\27251\Desktop\笔记\javaweb\image-20250417194953911.png)

键名与形参对象属性名相同

![image-20250417194516998](C:\Users\27251\Desktop\笔记\javaweb\image-20250417194516998.png)

使用@RequestBody标识

```java
 @RequestMapping("/jsonParam")
        public String jsonParam(@RequestBody User user){
                System.out.println(user);
                return "OK";
        }
```

![image-20250417195009225](C:\Users\27251\Desktop\笔记\javaweb\image-20250417195009225.png)

### 路径参数

#### 单个路径

![image-20250417195216812](C:\Users\27251\Desktop\笔记\javaweb\image-20250417195216812.png)

![image-20250417195556231](C:\Users\27251\Desktop\笔记\javaweb\image-20250417195556231.png)

#### 多个路径

![image-20250417195836541](C:\Users\27251\Desktop\笔记\javaweb\image-20250417195836541.png)

## 响应

### @ResponseBody注解

![image-20250417200126906](C:\Users\27251\Desktop\笔记\javaweb\image-20250417200126906.png)

#### 响应字符串

```java
@RequestMapping("/str")
public String stringResponse() {
    return "Hello SpringBoot";
}
```

![image-20250417201221679](C:\Users\27251\Desktop\笔记\javaweb\image-20250417201221679.png)

#### 响应对象

响应格式为json

```java
@RequestMapping("/obj")
public Address objResponse() {
    Address address = new Address();
    address.setProvince("福建");
    address.setCity("泉州");
    return address;
}
```

![image-20250417201254954](C:\Users\27251\Desktop\笔记\javaweb\image-20250417201254954.png)

#### 响应集合

响应格式为json数组

```java
@RequestMapping("/List")
public List<Address> listResponse() {
    Address address = new Address();
    address.setProvince("福建");
    address.setCity("泉州");
    Address address2 = new Address();
    address2.setProvince("福建");
    address2.setCity("厦门");

    List<Address> list = new ArrayList<>();
    list.add(address2);
    list.add(address);

    return list;
}
```

![image-20250417201350422](C:\Users\27251\Desktop\笔记\javaweb\image-20250417201350422.png)

#### 统一响应结果

上面三种响应格式都不同,不便于前后端开发

![image-20250417201534271](C:\Users\27251\Desktop\笔记\javaweb\image-20250417201534271.png)

![image-20250417201653548](C:\Users\27251\Desktop\笔记\javaweb\image-20250417201653548.png)

```java
package com.example.demo.POJO;

public class Result {
        //响应码 success:0 error:-1
        private Integer code;
        //提示信息
        private String msg;
        //返回数据
        private Object data;


        public Result() {
        }

        public Result(Integer code, String msg, Object data) {
                this.code = code;
                this.msg = msg;
                this.data = data;
        }

        public Integer getCode() {
                return code;
        }

        public void setCode(Integer code) {
                this.code = code;
        }

        public String getMsg() {
                return msg;
        }

        public void setMsg(String msg) {
                this.msg = msg;
        }

        public Object getData() {
                return data;
        }

        public void setData(Object data) {
                this.data = data;
        }

        @Override
        public String toString() {
                return "Result{" +
                        "code=" + code +
                        ", msg='" + msg + '\'' +
                        ", data=" + data +
                        '}';
        }
        public static Result success(Object data){
                return new Result(0,"success",data);
        }
        
        public static Result success(){
                return new Result(0,"success",null);
        }
        
        public static Result error(String errMsg){
                return new Result(-1,errMsg,null);
        }
}
```

static方法用于快速构建Result对象

##### 响应字符串

```java
@RequestMapping("/str")
public Result stringResponse() {
    //return new Result(0,"success","Hello SpringBoot");
    return Result.success("Hello SpringBoot");
}
```

![image-20250417202949112](C:\Users\27251\Desktop\笔记\javaweb\image-20250417202949112.png)

##### 响应对象

响应格式为json

```java
@RequestMapping("/obj")
public Result objResponse() {
    Address address = new Address();
    address.setProvince("福建");
    address.setCity("泉州");
    //return new Result(0,"success",address);
    return Result.success(address);
}
```

![image-20250417203015137](C:\Users\27251\Desktop\笔记\javaweb\image-20250417203015137.png)

##### 响应集合

响应格式为json数组

```java
@RequestMapping("/List")
public Result listResponse() {
    Address address = new Address();
    address.setProvince("福建");
    address.setCity("泉州");
    Address address2 = new Address();
    address2.setProvince("福建");
    address2.setCity("厦门");

    List<Address> list = new ArrayList<>();
    list.add(address2);
    list.add(address);

    //return new Result(0,"success",list);
    return Result.success(list);
}
```

![image-20250417203041487](C:\Users\27251\Desktop\笔记\javaweb\image-20250417203041487.png)

## 案例

![image-20250417204553667](C:\Users\27251\Desktop\笔记\javaweb\image-20250417204553667.png)

### pom.xml中添加坐标

```xml
<dependency>
    <groupId>org.dom4j</groupId>
    <artifactId>dom4j</artifactId>
    <version>2.1.3</version>
</dependency>
```

### 工具类XmlParserUtils

![image-20250417204611577](C:\Users\27251\Desktop\笔记\javaweb\image-20250417204611577.png)

```java
package com.example.demo.Utils;

import org.dom4j.Document;
import org.dom4j.DocumentException;
import org.dom4j.Element;
import org.dom4j.io.SAXReader;

import java.io.File;
import java.lang.reflect.Constructor;
import java.util.ArrayList;
import java.util.List;

/**
 * XML解析工具类
 * 提供将XML文件解析为Java对象列表的功能
 */
public class XmlParserUtils {

        /**
         * 将XML文件解析为指定类型的对象列表
         *
         * @param file        XML文件路径
         * @param targetClass 目标对象类型
         * @param <T>         泛型类型
         * @return 解析后的对象列表
         * @throws DocumentException 如果XML解析失败
         */
        public static <T> List<T> parse(String file, Class<T> targetClass) throws DocumentException {
                // 1. 创建SAXReader对象用于读取XML
                SAXReader reader = new SAXReader();

                // 2. 读取XML文件并获取Document对象
                Document document = reader.read(new File(file));

                // 3. 获取XML根元素
                Element rootElement = document.getRootElement();

                // 4. 获取所有emp元素
                List<Element> elements = rootElement.elements("emp");

                // 5. 准备返回的结果列表
                List<T> list = new ArrayList<>();

                try {
                        // 6. 遍历集合,得到每一个emp标签
                        for (Element element : elements) {
                                // 获取name属性
                                String name = element.element("name").getText();
                                // 获取age属性
                                String age = element.element("age").getText();
                                // 获取image属性
                                String image = element.element("image").getText();
                                // 获取gender属性
                                String gender = element.element("gender").getText();
                                // 获取job属性
                                String job = element.element("job").getText();

                                // 7. 获取目标类的构造方法
                                Constructor<T> constructor = targetClass.getDeclaredConstructor(
                                        String.class, Integer.class, String.class, String.class, String.class
                                );

                                // 8. 设置构造方法可访问（即使是私有构造方法）
                                constructor.setAccessible(true);

                                // 9. 使用反射创建对象实例
                                T object = constructor.newInstance(
                                        name,
                                        Integer.parseInt(age),
                                        image,
                                        gender,
                                        job
                                );

                                // 10. 将创建的对象添加到列表
                                list.add(object);
                        }
                } catch (Exception e) {
                        throw new RuntimeException("XML解析为对象失败", e);
                }

                return list;
        }
}
```

### Emp类

```java
public class Emp {
        private String name;
        private Integer age;
        private String image;
        private String gender;
        private String job;

        public Emp() {
        }

        public Emp(String name, Integer age, String image, String gender, String job) {
                this.name = name;
                this.age = age;
                this.image = image;
                this.gender = gender;
                this.job = job;
        }

        public String getName() {
                return name;
        }

        public void setName(String name) {
                this.name = name;
        }

        public Integer getAge() {
                return age;
        }

        public void setAge(Integer age) {
                this.age = age;
        }

        public String getImage() {
                return image;
        }

        public void setImage(String image) {
                this.image = image;
        }

        public String getGender() {
                return gender;
        }

        public void setGender(String gender) {
                this.gender = gender;
        }

        public String getJob() {
                return job;
        }

        public void setJob(String job) {
                this.job = job;
        }
}
```

### 处理请求类EmpController

假设前端请求路径如下：

![image-20250417212515559](C:\Users\27251\Desktop\笔记\javaweb\image-20250417212515559.png)

那么@RequestMapping中的路径就为"/listEmp"

```java
package com.example.demo.controller;

import com.example.demo.POJO.Emp;
import com.example.demo.POJO.Result;
import com.example.demo.Utils.XmlParserUtils;
import org.dom4j.DocumentException;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import java.util.List;

@RestController
public class EmpController {
        @RequestMapping("/listEmp")
        public Result list() throws DocumentException {
                //1.加载并解析emp.xml
                //动态加载xml文件
                String file = this.getClass().getClassLoader().getResource("emp.xml").getFile();
                List<Emp> empList = XmlParserUtils.parse(file, Emp.class);
                //2.对数据进行转换处理
                //流式处理
                empList.stream().forEach(emp -> {
                        String gender = emp.getGender();
                        if ("1".equals(gender)) {
                                emp.setGender("男");
                        } else if ("2".equals(gender)) {
                                emp.setGender("女");
                        }
                        String job = emp.getJob();
                        if ("1".equals(job)) {
                                emp.setJob("老师");
                        } else if ("2".equals(job)) {
                                emp.setJob("主任");
                        }else if("3".equals(job)){
                                emp.setJob("就业指导");
                        }
                });
                //3.响应数据
                return Result.success(empList);
        }
}

```

响应结果：

![image-20250417213927717](C:\Users\27251\Desktop\笔记\javaweb\image-20250417213927717.png)

# 分层解耦

## 三层架构

![image-20250417210400405](C:\Users\27251\Desktop\笔记\javaweb\image-20250417210400405.png)

![image-20250417210427254](C:\Users\27251\Desktop\笔记\javaweb\image-20250417210427254.png)

![image-20250417210517928](C:\Users\27251\Desktop\笔记\javaweb\image-20250417210517928.png)

### Dao层-数据访问

Dao对数据的访问方式很多（文件,数据库等）,想要灵活处理需要使用接口

![image-20250417214158607](C:\Users\27251\Desktop\笔记\javaweb\image-20250417214158607.png)

```java
package com.example.demo.Dao;

import com.example.demo.POJO.Emp;

import java.util.List;

public interface EmpDao {
        //获取员工列表
        public List<Emp> getListEmp();
}
```

它的实现类A：

![image-20250417214439110](C:\Users\27251\Desktop\笔记\javaweb\image-20250417214439110.png)

```java
package com.example.demo.Dao.impl;

import com.example.demo.Dao.EmpDao;
import com.example.demo.POJO.Emp;
import com.example.demo.Utils.XmlParserUtils;
import org.dom4j.DocumentException;

import java.util.List;

public class EmpDaoA implements EmpDao {
        @Override
        public List<Emp> getListEmp() throws DocumentException {
                //1.加载并解析emp.xml
                //动态加载xml文件
                String file = this.getClass().getClassLoader().getResource("emp.xml").getFile();
                return XmlParserUtils.parse(file, Emp.class);
        }
}
```

### Service层-业务逻辑处理

与Dao层类似,想要灵活处理,使用接口

![image-20250417214923497](C:\Users\27251\Desktop\笔记\javaweb\image-20250417214923497.png)

```java
package com.example.demo.service;

import com.example.demo.POJO.Emp;

import java.util.List;

public interface EmpService {
        //返回处理后的emp列表
        public List<Emp> ListEmp();
}
```

它的实现类：

要处理数据,需要从Dao层获取,那么需要定义Dao对象

```java
package com.example.demo.service.impl;

import com.example.demo.Dao.EmpDao;
import com.example.demo.Dao.impl.EmpDaoA;
import com.example.demo.POJO.Emp;
import com.example.demo.service.EmpService;
import org.dom4j.DocumentException;

import java.util.List;

public class EmpServiceA implements EmpService {
        //面向接口编程
        private EmpDao empDao = new EmpDaoA();

        @Override
        public List<Emp> ListEmp() throws DocumentException {
                List<Emp> empList = empDao.getListEmp();
                empList.stream().forEach(emp -> {
                        String gender = emp.getGender();
                        if ("1".equals(gender)) {
                                emp.setGender("男");
                        } else if ("2".equals(gender)) {
                                emp.setGender("女");
                        }
                        String job = emp.getJob();
                        if ("1".equals(job)) {
                                emp.setJob("老师");
                        } else if ("2".equals(job)) {
                                emp.setJob("主任");
                        } else if ("3".equals(job)) {
                                emp.setJob("就业指导");
                        }
                });
                
                return empList;
        }
}
```

### Controller层-接收请求,响应数据

需要调底下1层的接口

```java
package com.example.demo.controller;

import com.example.demo.Dao.EmpDao;
import com.example.demo.POJO.Emp;
import com.example.demo.POJO.Result;
import com.example.demo.Utils.XmlParserUtils;
import com.example.demo.service.EmpService;
import com.example.demo.service.impl.EmpServiceA;
import org.dom4j.DocumentException;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import java.util.List;

@RestController
public class EmpController {
        private EmpService empService = new EmpServiceA();
        @RequestMapping("/listEmp")
        public Result list() throws DocumentException {
                //1.加载并解析emp.xml
                //2.对数据进行转换处理
                List<Emp> empList = empService.ListEmp();
                //3.响应数据
                return Result.success(empList);
        }
}
```

![image-20250417215752235](C:\Users\27251\Desktop\笔记\javaweb\image-20250417215752235.png)

## 分层解耦

![image-20250417220049558](C:\Users\27251\Desktop\笔记\javaweb\image-20250417220049558.png)

EmpController中的empService是Service层实现类的实例,说明这两层耦合

解决方法：容器

![image-20250417220320616](C:\Users\27251\Desktop\笔记\javaweb\image-20250417220320616.png) 

![image-20250417220343493](C:\Users\27251\Desktop\笔记\javaweb\image-20250417220343493.png)

  ![image-20250417220457909](C:\Users\27251\Desktop\笔记\javaweb\image-20250417220457909.png)

### 步骤

![image-20250418201847743](C:\Users\27251\Desktop\笔记\javaweb\image-20250418201847743.png)

### @Component注解

在Dao层、Service实现类前加上该注解,表示将该类交给IOC容器管理,成为IOC容器中的bean

这样一来Controller层想要切换底层,直接更改@Component作用的类就行

```java
@Component
public class EmpDaoA implements EmpDao {
        @Override
        public List<Emp> getListEmp() throws DocumentException {
                //1.加载并解析emp.xml
                //动态加载xml文件
                String file = this.getClass().getClassLoader().getResource("emp.xml").getFile();
                return XmlParserUtils.parse(file, Emp.class);
        }
}
```



### @Autowired注解

运行时,IOC容器会提供该类型的bean对象,并赋值给该变量 - 依赖注入

```java
@RestController
public class EmpController {
        @Autowired
        private EmpService empService;
        @RequestMapping("/listEmp")
        public Result list() throws DocumentException {
                //1.加载并解析emp.xml
                //2.对数据进行转换处理
                List<Emp> empList = empService.ListEmp();
                //3.响应数据
                return Result.success(empList);
        }
}
```

## IOC详解

### Bean的声明

![image-20250418203528345](C:\Users\27251\Desktop\笔记\javaweb\image-20250418203528345.png)

Controller层不用再加@Controller,因为@RestController=@Repository+@Controller

![image-20250418203737224](C:\Users\27251\Desktop\笔记\javaweb\image-20250418203737224.png)

为什么称之为@Component的衍生类？



![image-20250418204430796](C:\Users\27251\Desktop\笔记\javaweb\image-20250418204430796.png)

![image-20250418204407308](C:\Users\27251\Desktop\笔记\javaweb\image-20250418204407308.png)

```java
//可以以这样的形式为Bean对象起名字
@Service("Name")
```

### 注意事项

![image-20250418204546486](C:\Users\27251\Desktop\笔记\javaweb\image-20250418204546486.png)

### Bean组件扫描

![image-20250418204842261](C:\Users\27251\Desktop\笔记\javaweb\image-20250418204842261.png)

规范：将Dao放在启动类所在包

不规范：找不到包

![image-20250418205159062](C:\Users\27251\Desktop\笔记\javaweb\image-20250418205159062.png)

就需要在启动类上使用@ComponentScan

![image-20250418205005662](C:\Users\27251\Desktop\笔记\javaweb\image-20250418205005662.png)

源码显示,@ComponentScan需要接受String数组作为所在包

```java
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.context.annotation.ComponentScan;

@ComponentScan({"Dao","com.example.demo"})
@SpringBootApplication
public class DemoApplication {

        public static void main(String[] args) {
                SpringApplication.run(DemoApplication.class, args);
        }

}
```

我们为什么数组中传入两个包呢？

@SpringBootApplication中集成的@ComponentScan扫描的是启动类所在的包；

在@ComponentScan中声明其他的包会覆盖掉启动类所在的包,所以需要重新声明启动类所在的包

## DI详解

如果有多个相同类型的Bean：

![image-20250418211728937](C:\Users\27251\Desktop\笔记\javaweb\image-20250418211728937.png)

![image-20250418211743623](C:\Users\27251\Desktop\笔记\javaweb\image-20250418211743623.png)

![image-20250418211703044](C:\Users\27251\Desktop\笔记\javaweb\image-20250418211703044.png)

![image-20250418211232732](C:\Users\27251\Desktop\笔记\javaweb\image-20250418211232732.png)

### @Primary

多个相同类型的Bean,加上@Primary的那个生效

![image-20250418211916896](C:\Users\27251\Desktop\笔记\javaweb\image-20250418211916896.png)

![image-20250418211907939](C:\Users\27251\Desktop\笔记\javaweb\image-20250418211907939.png)

![image-20250418212004613](C:\Users\27251\Desktop\笔记\javaweb\image-20250418212004613.png)

![image-20250418211955691](C:\Users\27251\Desktop\笔记\javaweb\image-20250418211955691.png)

### @Qualifier

在@AutoWired前加上@Qualifier("Bean名字")

```java
package com.example.demo.controller;

import com.example.demo.POJO.Emp;
import com.example.demo.POJO.Result;
import com.example.demo.service.EmpService;
import org.dom4j.DocumentException;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import java.util.List;

@RestController
public class EmpController {
    	//EmpServiceA默认的bean名字
        @Qualifier("empServiceA")
        @Autowired
        private EmpService empService;
        @RequestMapping("/listEmp")
        public Result list() throws DocumentException {
                //1.加载并解析emp.xml
                //2.对数据进行转换处理
                List<Emp> empList = empService.ListEmp();
                //3.响应数据
                return Result.success(empList);
        }
}
```

### @Resource

与@Qualifier的区别：

- @Qualifier按照类型注入

- @Resource按照名称注入;使用@Resource后就不用@Autowired了

    ```java
    package com.example.demo.controller;
    
    import com.example.demo.POJO.Emp;
    import com.example.demo.POJO.Result;
    import com.example.demo.service.EmpService;
    import jakarta.annotation.Resource;
    import org.dom4j.DocumentException;
    import org.springframework.beans.factory.annotation.Autowired;
    import org.springframework.beans.factory.annotation.Qualifier;
    import org.springframework.web.bind.annotation.RequestMapping;
    import org.springframework.web.bind.annotation.RestController;
    
    import java.util.List;
    
    @RestController
    public class EmpController {
    //        @Qualifier("empServiceA")
    //        @Autowired
            @Resource(name = "empServiceB")
            private EmpService empService;
            @RequestMapping("/listEmp")
            public Result list() throws DocumentException {
                    //1.加载并解析emp.xml
                    //2.对数据进行转换处理
                    List<Emp> empList = empService.ListEmp();
                    //3.响应数据
                    return Result.success(empList);
            }
    }
    ```

    

<img src="C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250418212814266.png" alt="image-20250418212814266" style="zoom:40%;" />

# Mybatis

![image-20250418213624926](C:\Users\27251\Desktop\笔记\javaweb\image-20250418213624926.png)

## 准备工作

![image-20250418213948765](C:\Users\27251\Desktop\笔记\javaweb\image-20250418213948765.png)

![image-20250420162905928](C:\Users\27251\Desktop\笔记\javaweb\image-20250420162905928.png)

![image-20250420163058104](C:\Users\27251\Desktop\笔记\javaweb\image-20250420163058104.png)

![image-20250420163042923](C:\Users\27251\Desktop\笔记\javaweb\image-20250420163042923.png)

### springboot工程

![image-20250418214309975](C:\Users\27251\Desktop\笔记\javaweb\image-20250418214309975.png)

![image-20250418214350129](C:\Users\27251\Desktop\笔记\javaweb\image-20250418214350129.png)

### 配置文件

```properties
spring.application.name=Mybatis-demo
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
#数据库名
spring.datasource.url=jdbc:mysql://localhost:3306/mybatis
#用户名
spring.datasource.username=root
#密码
spring.datasource.password=114514
```

### @Mapper注解

Mybatis中Mapper层其实就和Dao层差不多

在运行时，会自动生成该接口的实现类对象（代理对象），并且将该对象交给IOC容器管理

```java
package com.wwwtty.mybatisdemo.mapper;

import com.wwwtty.mybatisdemo.pojo.User;
import org.apache.ibatis.annotations.Mapper;
import org.apache.ibatis.annotations.Select;

import java.util.List;

@Mapper
public interface UserMapper {
        @Select("select* from user")
        public List<User> list();
}
```

### 进行单元测试

![image-20250420163551135](C:\Users\27251\Desktop\笔记\javaweb\image-20250420163551135.png)

```java
package com.wwwtty.mybatisdemo;

import com.wwwtty.mybatisdemo.mapper.UserMapper;
import com.wwwtty.mybatisdemo.pojo.User;
import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;

import java.util.List;

@SpringBootTest
class MybatisDemoApplicationTests {

        @Autowired
        UserMapper userMapper;

        @Test
        public void UserListTest(){
                List<User> list = userMapper.list();
                list.stream().forEach(user ->{
                        System.out.println(user);
                });
        }
}
```

@SpringBootTest进行单元测试时，也会加载整个springboot环境

![image-20250420170435640](C:\Users\27251\Desktop\笔记\javaweb\image-20250420170435640.png)

### 配置sql提示

![image-20250420201158998](C:\Users\27251\Desktop\笔记\javaweb\image-20250420201158998.png)

![image-20250420201430768](C:\Users\27251\Desktop\笔记\javaweb\image-20250420201430768.png)

![image-20250420201500926](C:\Users\27251\Desktop\笔记\javaweb\image-20250420201500926.png)

![image-20250420201524960](C:\Users\27251\Desktop\笔记\javaweb\image-20250420201524960.png)

![image-20250420201822363](C:\Users\27251\Desktop\笔记\javaweb\image-20250420201822363.png)

![image-20250420202059036](C:\Users\27251\Desktop\笔记\javaweb\image-20250420202059036.png)

功能强大qaq：

![image-20250420202159898](C:\Users\27251\Desktop\笔记\javaweb\image-20250420202159898.png)

## JDBC

（面向接口编程）

JDBC只提供接口，由数据库厂商实现具体方法

 ![image-20250420202340362](C:\Users\27251\Desktop\笔记\javaweb\image-20250420202340362.png)

缺点：

![image-20250420202552672](C:\Users\27251\Desktop\笔记\javaweb\image-20250420202552672.png)

![image-20250420202708569](C:\Users\27251\Desktop\笔记\javaweb\image-20250420202708569.png)

## 数据库连接池

![image-20250420202838234](C:\Users\27251\Desktop\笔记\javaweb\image-20250420202838234.png)

 ![image-20250420202924564](C:\Users\27251\Desktop\笔记\javaweb\image-20250420202924564.png)

![image-20250420203009321](C:\Users\27251\Desktop\笔记\javaweb\image-20250420203009321.png)

![image-20250420203204017](C:\Users\27251\Desktop\笔记\javaweb\image-20250420203204017.png)

![image-20250420203059719](C:\Users\27251\Desktop\笔记\javaweb\image-20250420203059719.png)

实现了DataSource接口

![image-20250420203123699](C:\Users\27251\Desktop\笔记\javaweb\image-20250420203123699.png)

### 切换连接池

只需要引入maven依赖

![image-20250420203258391](C:\Users\27251\Desktop\笔记\javaweb\image-20250420203258391.png)

```XML
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid-spring-boot-starter</artifactId>
    <version>1.2.8</version>
</dependency>
```

本地测试还得在properties文件加上：

```properties
spring.datasource.type=com.alibaba.druid.pool.DruidDataSource
```

才能：

![image-20250420204600465](C:\Users\27251\Desktop\笔记\javaweb\image-20250420204600465.png)

或者：

由于我的springboot版本为：

![image-20250420205002180](C:\Users\27251\Desktop\笔记\javaweb\image-20250420205002180.png)

因此坐标中的druid-spring-boot-starter应该改成druid-spring-boot-3-starter

```xml
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>druid-spring-boot-3-starter</artifactId>
    <version>1.2.22</version>
</dependency>
```

![image-20250420204922741](C:\Users\27251\Desktop\笔记\javaweb\image-20250420204922741.png)

另一种配置方式

![image-20250420205145225](C:\Users\27251\Desktop\笔记\javaweb\image-20250420205145225.png)

## lombok

pojo类算上getter/setter等方法之后，太过于臃肿

![image-20250420205336460](C:\Users\27251\Desktop\笔记\javaweb\image-20250420205336460.png)

![image-20250420205419808](C:\Users\27251\Desktop\笔记\javaweb\image-20250420205419808.png)

### 引入依赖

```xml
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
</dependency>
```

### @Data

包含了@Getter，@Setter，@ToString，@EqualsAndHashCode

不包含构造器

```java
package com.wwwtty.mybatisdemo.pojo;

import lombok.AllArgsConstructor;
import lombok.Data;
import lombok.Getter;
import lombok.NoArgsConstructor;

@Data
@NoArgsConstructor
@AllArgsConstructor
public class User {
        private Integer id;
        private String username;
        private String password;
        private String email;
}
```

![image-20250420210030897](C:\Users\27251\Desktop\笔记\javaweb\image-20250420210030897.png)

上述注解的作用在于根据注解生成一系列方法

User的字节码文件反编译：

![image-20250420210155253](C:\Users\27251\Desktop\笔记\javaweb\image-20250420210155253.png)

![image-20250420210230204](C:\Users\27251\Desktop\笔记\javaweb\image-20250420210230204.png)

## Mybatis基础操作

## 删除操作

### @Delete

```java
package com.wwwtty.basic_op.Mapper;

import org.apache.ibatis.annotations.Delete;
import org.apache.ibatis.annotations.Mapper;

@Mapper
public interface EmpMapper {
        @Delete("delete from emp where id = 1")
        void delete();
}
```

这么做的局限性是，id是静态的，但是前端传进来的id参数肯定是动态的

### 传递参数

在@Delete中将参数用`#{}`包围

![image-20250426152414630](C:\Users\27251\Desktop\笔记\javaweb\image-20250426152414630.png)

```java
package com.wwwtty.basic_op.Mapper;

import org.apache.ibatis.annotations.Delete;
import org.apache.ibatis.annotations.Mapper;

@Mapper
public interface EmpMapper {
        @Delete("delete from emp where id = #{id}")
        void delete(Integer id);
}
```

如何拿到影响的记录数呢，改一下返回值就可以

```java
package com.wwwtty.basic_op.Mapper;

import org.apache.ibatis.annotations.Delete;
import org.apache.ibatis.annotations.Mapper;

@Mapper
public interface EmpMapper {
        @Delete("delete from emp where id = 1")
        Integer delete();
}
```

```java
@Test
void contextLoads() {
    System.out.println(empMapper.delete(5));
}
```

![image-20250426152241559](C:\Users\27251\Desktop\笔记\javaweb\image-20250426152241559.png)

### 测试

表内容如下：

![image-20250426151816452](C:\Users\27251\Desktop\笔记\javaweb\image-20250426151816452.png)

用@Autowired注入

```java
package com.wwwtty.basic_op;

import com.wwwtty.basic_op.Mapper.EmpMapper;
import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;

@SpringBootTest
class BasicOpApplicationTests {
        @Autowired
        private EmpMapper empMapper;
        @Test
        void contextLoads() {
                empMapper.delete(5);
        }
}
```

![image-20250426151830288](C:\Users\27251\Desktop\笔记\javaweb\image-20250426151830288.png)

### Mybatis日志输出

```properties
#mybatis日志输出,输出到控制台
mybatis.configuration.log-impl=org.apache.ibatis.logging.stdout.StdOutImpl
```

运行结果：![image-20250426152754662](C:\Users\27251\Desktop\笔记\javaweb\image-20250426152754662.png)

使用了参数化查询技术（预编译查询）

### 预编译SQL优势

![image-20250426153102976](C:\Users\27251\Desktop\笔记\javaweb\image-20250426153102976.png)

### 参数占位符

![image-20250426153355879](C:\Users\27251\Desktop\笔记\javaweb\image-20250426153355879.png)

## 新增操作

### @Insert

insert中的字段太多，可以直接封装成一个对象

用lombok封装getter/setter等方法

![image-20250426154316266](C:\Users\27251\Desktop\笔记\javaweb\image-20250426154316266.png)

```java
package com.wwwtty.mybatis_insert.Mapper;

import com.wwwtty.mybatis_insert.pojo.Emp;
import org.apache.ibatis.annotations.Insert;
import org.apache.ibatis.annotations.Mapper;

@Mapper
public interface EmpMapper {
        @Insert("insert into emp (id,name,email) values (#{id},#{name},#{email})")
        void Insert(Emp emp);
}
```

```java
package com.wwwtty.mybatis_insert;

import com.wwwtty.mybatis_insert.Mapper.EmpMapper;
import com.wwwtty.mybatis_insert.pojo.Emp;
import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;

@SpringBootTest
class MybatisInsertApplicationTests {
        @Autowired
        EmpMapper empMapper;
        @Test
        void contextLoads() {
                Emp emp = new Emp();
                emp.setId(5);
                emp.setEmail("114514@acceed.com");
                emp.setName("淳平");

                empMapper.Insert(emp);
        }
}
```

日志输出：

![image-20250426155110184](C:\Users\27251\Desktop\笔记\javaweb\image-20250426155110184.png)

### 主键返回

![image-20250426155301757](C:\Users\27251\Desktop\笔记\javaweb\image-20250426155301757.png)

#### @Options

```java
package com.wwwtty.mybatis_insert.Mapper;

import com.wwwtty.mybatis_insert.pojo.Emp;
import org.apache.ibatis.annotations.Insert;
import org.apache.ibatis.annotations.Mapper;
import org.apache.ibatis.annotations.Options;

@Mapper
public interface EmpMapper {

        /*
        * keyProperty:主键值赋值给实体类哪个对象
        * useGeneratedKeys:获取主键值
        * */
        @Options(keyProperty = "id", useGeneratedKeys = true)
        @Insert("insert into emp (name,email) values (#{name},#{email})")
        void Insert(Emp emp);
}
```

这样一来getId()就不会返回null

```java
package com.wwwtty.mybatis_insert;

import com.wwwtty.mybatis_insert.Mapper.EmpMapper;
import com.wwwtty.mybatis_insert.pojo.Emp;
import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;

@SpringBootTest
class MybatisInsertApplicationTests {
        @Autowired
        EmpMapper empMapper;
        @Test
        void contextLoads() {
                Emp emp = new Emp();
//                emp.setId(5);
                emp.setEmail("114514@acceed.com");
                emp.setName("林丹");

                empMapper.Insert(emp);
                System.out.println(emp.getId());
        }
}
```

![image-20250426161006342](C:\Users\27251\Desktop\笔记\javaweb\image-20250426161006342.png)

## 更新操作

### @Update

![image-20250426161909725](C:\Users\27251\Desktop\笔记\javaweb\image-20250426161909725.png)

```java
package com.wwwtty.mybatis_update.Mapper;

import com.wwwtty.mybatis_update.pojo.Emp;
import org.apache.ibatis.annotations.Mapper;
import org.apache.ibatis.annotations.Update;

@Mapper
public interface EmpMapper {
        @Update("update emp set name=#{name},email=#{email} where id=#{id}")
        void update(Emp emp);
}
```

执行结果：

![image-20250426162430561](C:\Users\27251\Desktop\笔记\javaweb\image-20250426162430561.png)

![image-20250426162436087](C:\Users\27251\Desktop\笔记\javaweb\image-20250426162436087.png)

## 查询操作

```java
package com.wwwtty.mybatis_select.Mapper;

import com.wwwtty.mybatis_select.pojo.Emp;
import org.apache.ibatis.annotations.Mapper;
import org.apache.ibatis.annotations.Select;

import java.util.List;

@Mapper
public interface EmpMapper {
        @Select("select* from emp where id = #{id}")
        List<Emp> getById(Integer id);
}
```

```java
package com.wwwtty.mybatis_select;

import com.wwwtty.mybatis_select.Mapper.EmpMapper;
import com.wwwtty.mybatis_select.pojo.Emp;
import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;

@SpringBootTest
class MybatisSelectApplicationTests {
        @Autowired
        EmpMapper empMapper;
        @Test
        void contextLoads() {
                Emp emp = new Emp();
                emp.setId(5);
                System.out.println(empMapper.getById(5));
        }
}
```

运行结果：

![image-20250426164017496](C:\Users\27251\Desktop\笔记\javaweb\image-20250426164017496.png)

### 数据封装

![image-20250426164121784](C:\Users\27251\Desktop\笔记\javaweb\image-20250426164121784.png)

![image-20250426164220088](C:\Users\27251\Desktop\笔记\javaweb\image-20250426164220088.png)

### @Results，@Result

```java
/*
* column:字段名
* property:类中属性名
* */
@Results({
    @Result(column = "",property = ""),
    @Result(column = "",property = "")
})
```

### 开启mybatis驼峰命名自动映射开关 a_column -> aColumn

```properties
#开启mybatis驼峰命名自动映射开关(直接搜索骆驼(camel))
mybatis.configuration.map-underscore-to-camel-case=true
```

## 条件查询

![image-20250426165935370](C:\Users\27251\Desktop\笔记\javaweb\image-20250426165935370.png)

![image-20250426165951149](C:\Users\27251\Desktop\笔记\javaweb\image-20250426165951149.png)

```mysql
select * from user where name like '%张%' and gender=1 and entrydate between '2010-01-01' and '2020-01-01' order by update_time desc
```

这些参数不好封装到一个对象中去，直接传参数

```java
@Select("select * from user where name like '%${name}%' and gender=#{gender} and " +
        "entrydate between #{begin} and #{end} order by update_time desc")
List<User> list(String name, Short gender, LocalDate begin,LocalDate end);
```

**进行模糊匹配的时候，要用'%%'的形式，这样就不能用预编译的#{}(占位符不能出现在引号内)，需要用拼接sql的${}(不推荐)**

```java
@Test
    void test() {
    List<User> res = empMapper.list("张", (short) 1, LocalDate.of(2010, 1, 1), LocalDate.of(2020, 1, 1));
    res.stream().forEach(user -> {
    	System.out.println(user);
    });
}
```

![image-20250426171629304](C:\Users\27251\Desktop\笔记\javaweb\image-20250426171629304.png)

怎么解决拼接的问题

### concat()

```java
@Select("select * from user where name like concat('%',#{name},'%') and gender=#{gender} and " +
        "entrydate between #{begin} and #{end} order by update_time desc")
List<User> list(String name, Short gender, LocalDate begin,LocalDate end);
```

![image-20250426172027177](C:\Users\27251\Desktop\笔记\javaweb\image-20250426172027177.png)

早期版本不会保留形参名

![image-20250426172059490](C:\Users\27251\Desktop\笔记\javaweb\image-20250426172059490.png)

## XML映射文件

![image-20250428203330256](C:\Users\27251\Desktop\笔记\javaweb\image-20250428203330256.png)

![image-20250428203708238](C:\Users\27251\Desktop\笔记\javaweb\image-20250428203708238.png)

与包名一致

![image-20250428204102085](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428204102085.png)

与接口名一致

![image-20250428204545697](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428204545697.png)

xml文件的约束：https://mybatis.p2hp.com/getting-started.html

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "https://mybatis.org/dtd/mybatis-3-mapper.dtd">
<!--mapper根标签-->
<mapper namespace="com.wwwtty.xml_reflect.mapper.EmpMapper">
        <!--    id:Mapper类中的方法名    -->
        <!--   resultType:返回值所封装的单条记录的类型的全类名,比如返回值是List<User>,填的就是User的全类名     -->
        <select id="list" resultType="">
                
        </select>
</mapper>
```

获取全类名：

![image-20250428204919955](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428204919955.png)

原查询语句：

```java
@Select("select * from user where name like concat('%',#{name},'%') and gender=#{gender} and " +
        "entrydate between #{begin} and #{end} order by update_time desc")
List<User> list(String name, Short gender, LocalDate begin,LocalDate end);
```



改用xml映射的方式：

如果xml中sql语句没有高亮，上下文操作中选择注入语言

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "https://mybatis.org/dtd/mybatis-3-mapper.dtd">
<!--mapper根标签-->
<mapper namespace="com.wwwtty.xml_reflect.mapper.EmpMapper">
        <!--    id:Mapper类中的方法名    -->
        <!--   resultType:返回值所封装的单条记录的类型的全类名,比如返回值是List<User>,填的就是User的全类名     -->
        <select id="list" resultType="com.wwwtty.xml_reflect.pojo.User">
                select * from user where name like concat('%',#{name},'%') and gender=#{gender} and
                entrydate between #{begin} and #{end} order by update_time desc
        </select>
</mapper>
```

xml映射适合于复杂sql

## 动态sql

![image-20250428210744924](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428210744924.png)

### < if >

![image-20250428211702486](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428211702486.png)

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "https://mybatis.org/dtd/mybatis-3-mapper.dtd">
<!--mapper根标签-->
<mapper namespace="com.wwwtty.xml_reflect.mapper.EmpMapper">
        <!--    id:Mapper类中的方法名    -->
        <!--   resultType:返回值所封装的单条记录的类型的全类名,比如返回值是List<User>,填的就是User的全类名     -->
        <select id="list" resultType="com.wwwtty.xml_reflect.pojo.User">
                select *
                from user
                where
                <if test="name != null">
                        name like concat('%', #{name}, '%')
                </if>
                <if test="gender != null">
                        and gender = #{gender}
                </if>
                <if test="begin != null and end != null">
                        and entrydate between #{begin} and #{end}
                </if>
                order by update_time desc
        </select>
</mapper>
```

```java
empMapper.list(name,null,null,end);
```

相应的sql语句：

![image-20250428212313281](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428212313281.png)

### < where >

在上面的例子中，如果我们只筛选性别：

![image-20250428212633326](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428212633326.png)

但是这个and还很不好删除（容易别的地方出错）

作用：根据if的结果（子元素），自动添加/删除where；同时自动删除多余的and和or

使用< where >解决

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "https://mybatis.org/dtd/mybatis-3-mapper.dtd">
<!--mapper根标签-->
<mapper namespace="com.wwwtty.xml_reflect.mapper.EmpMapper">
        <!--    id:Mapper类中的方法名    -->
        <!--   resultType:返回值所封装的单条记录的类型的全类名,比如返回值是List<User>,填的就是User的全类名     -->
        <select id="list" resultType="com.wwwtty.xml_reflect.pojo.User">
                        select *
                        from user
                            <where>
                                    <if test="name != null">
                                            name like concat('%', #{name}, '%')
                                    </if>
                                    <if test="gender != null">
                                            and gender = #{gender}
                                    </if>
                                    <if test="begin != null and end != null">
                                            and entrydate between #{begin} and #{end}
                                    </if>
                                    order by update_time desc
                            </where>
        </select>
</mapper>
```

运行生成的sql：

![image-20250428213048653](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428213048653.png)

### < set >

去除set中多余的逗号

#### 案例:动态更新

如果我们这样写动态更新的xml配置文件

```xml
<update id="update">
    update user
    set
    <if test="username != null">
        username=#{username},
    </if>
    <if test="password != null">
        password=#{password},
    </if>
    <if test="name != null">
        name=#{name},
    </if>
    <if test="gender != null">
        gender=#{gender},
    </if>
    <if test="image != null">
        image=#{image},
    </if>
    <if test="job != null">
        job=#{job},
    </if>
    <if test="entrydate != null">
        entrydate=#{entrydate},
    </if>
    <if test="deptId != null">
        dept_id=#{deptId},
    </if>
    <if test="createDate != null">
        create_time=#{createTime},
    </if>

    <if test="updateTime != null">
        update_time=#{updateTime}
    </if>
    where id = #{id}
</update>
```

![image-20250428215649758](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428215649758.png)

会有多一个逗号的情况

使用 < set >解决

![image-20250428215812928](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250428215812928.png) 



### < foreach >

场景：批量删除

```sql
delete from user where id in(3,4,5);
```

```java
void deleteByIds(List<Integer> list);
```

```xml
<delete id="deleteByIds">
    <foreach collection="" item="" separator="" open="" close="">

    </foreach>
</delete>
```

- collection:要遍历的集合

- item:遍历出的元素

- separator:分隔符

- open:遍历开始前拼接的sql片段

- close:遍历结束后拼接的sql片段

    ```xml
    <!--    delete from user where id in(3,4,5)    -->
    <delete id="deleteByIds">
        delete from user where id in
        <foreach collection="list" item="id" separator="," open="(" close=")">
            #{id}
        </foreach>
    </delete>
    ```

    

### < sql >

< sql >用于封装一些重复使用的sql片段，并分配一个唯一的id

### < include >

用< include >包含< sql >封装的sql片段，用refid=id从而完成包含

```java
void selectArgs();

void selectById();
```



```xml
<sql id="basicSelect">
    select username,
    password,
    name,
    gender,
    id,
    username,
    password,
    name,
    gender,
    image,
    job,
    entrydate,
    dept_id,
    create_time,
    update_time
    from user
</sql>

<select id="selectArgs">
    <include refid="basicSelect" />
</select>
<select id="selectById">
    <include refid="basicSelect" />

</select>
```

![image-20250429211401588](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250429211401588.png)

## 案例

![image-20250501194904854](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250501194904854.png)

### 开发规范

![image-20250501200003215](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250501200003215.png)

#### Restful

![image-20250501200305519](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250501200305519.png)

![image-20250501200336571](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250501200336571.png)

#### 统一响应结果

![image-20250501200425157](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250501200425157.png)

### 开发流程

![image-20250501200541756](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250501200541756.png)

### 部门管理

#### 部门管理-查询

##### 接口文档：

![image-20250502104701029](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502104701029.png)

![image-20250502104743935](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502104743935.png)

```java
//使用该注解就不用自己new日志对象
@Slf4j
@RestController
public class deptController {
        @RequestMapping("/dept")
        public Result list(){
                log.info("查询所有部门信息");
                return Result.Success();
        }
}
```

ps：构建项目时不要选lombok，否则要在pom.xml中注释以下内容：

![image-20250502110941701](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502110941701.png)

否则报错：

![image-20250502110956067](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502110956067.png)

##### postman测试：

![image-20250502111138681](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502111138681.png)

##### 日志输出：

![image-20250502111156255](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502111156255.png)

##### 指定请求方法

```java
@RequestMapping(value = "/depts",method = RequestMethod.GET)
//简化版本
 @GetMapping("depts")
```

##### 注入依赖

Controller层

```java
@Slf4j
@RestController
public class deptController {
        @Autowired
        private deptService service;
        @GetMapping("depts")
        public Result list() {
                log.info("查询所有部门信息");
                //查询所有部门信息
                List<Dept> deptList = service.list();
                return Result.success(deptList);
        }
}
```

Service层

```java
@Service
public class deptImpl implements deptService {
        @Autowired
        private deptMapper mapper;

        @Override
        public List<Dept> list() {
                return mapper.list();
        }
}
```

Mapper层

```java
@Mapper
public interface deptMapper {
        @Select("select * from dept")
        public List<Dept> list();
}
```

![image-20250502112504837](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502112504837.png)

#### 部门管理-删除

##### 接口文档

![image-20250502113702239](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502113702239.png)

##### 流程

![image-20250502113924420](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502113924420.png)

##### Controller层

```java
@DeleteMapping("/depts/{id}")
public Result delete(@PathVariable Integer id){
    log.info("根据id删除部门:{}",id);
    service.delete(id);
    return Result.success();
}
```



##### Service层

```java
@Override
public void delete(Integer id) {
    mapper.deleteById(id);
}
```



##### Mapper层

```java
@Delete("delete from dept where id=#{id}")
void deleteById(Integer id);
```

##### postman测试

![image-20250502114723744](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502114723744.png)

##### 执行结果

![image-20250502114642751](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502114642751.png)

![image-20250502114646465](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502114646465.png)

#### 部门管理-新增

##### 接口文档

![image-20250502115239802](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502115239802.png)

![image-20250502115559884](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502115559884.png)

##### Controller层

```java
@PostMapping("/depts")
public Result add(@RequestBody Dept dept){
    log.info("新增部门{}",dept);
    service.add(dept);
    return Result.success();
}
```



##### Service层

```java
@Override
public void add(Dept dept){
    dept.setCreateTime(LocalDate.now());
    dept.setUpdateTime(LocalDate.now());

    mapper.insert(dept);
}
```



##### Mapper层

```java
@Insert("insert into dept (name,create_time,update_time) values (#{name},#{createTime},#{updateTime})")
void insert(Dept dept);
```



##### postman测试

![image-20250502120724193](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502120724193.png)

##### 结果

![image-20250502120905590](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502120905590.png)

![image-20250502120921945](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502120921945.png)

#### 简化RequestMapping

![image-20250502121354174](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502121354174.png)

![image-20250502121723903](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250502121723903.png)

### 员工管理

#### 分页查询

##### 分析

![image-20250513210042683](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513210042683.png)

##### 接口文档

![image-20250513210239794](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513210239794.png)

![image-20250513210246107](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513210246107.png)

![image-20250513210255167](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513210255167.png)

![image-20250513210324909](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513210324909.png)

![image-20250513210538282](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513210538282.png)

##### 封装实体类

![image-20250513210839682](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513210839682.png)

```java
@Data
@NoArgsConstructor
@AllArgsConstructor
public class pageBean {
        private Long total;
        private List rows;
}
```

##### 实现

###### Mapper层

```java
@Mapper
public interface EmpMapper {
        /**
         * 查询总记录数
         * @return
         */
        @Select("select count(*) from emp")
         Long count();

        /**
         *
         * @param page:起始页
         * @param pageSize:查多少页
         * @return
         */
        @Select("select * from emp limit #{page},#{pageSize}")
         List<Emp> page(Integer page,Integer pageSize);
}
```

###### Service层

```java
@Service
public class empImpl implements empService {
        @Autowired
        EmpMapper empMapper;

        @Override
        public PageBean page(Integer page, Integer pageSize) {
                Long total = empMapper.count();
                Integer start = (page - 1) * pageSize;
                List<Emp> rows = empMapper.page(start, pageSize);
                //封装pageBean
                PageBean pageBean = new PageBean(total,rows);
                return pageBean;
        }
}
```



###### Controller层

![image-20250513211738018](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513211738018.png)

用@RequestParam(defaultValue="")设置参数默认值

```java
@RestController
public class empController {
        @GetMapping("/emps")
        public Result page(@RequestParam(defaultValue = "1") Integer page, @RequestParam(defaultValue = "10") Integer pageSize){
                return new Result();
        }
}
```

日志输出

```java
log.info("分页查询,分页查询页码为{},每页记录数为{}",page,pageSize);
```

调用Service层

```java
PageBean pageBean = empservice.page(page,pageSize);
```

```java
@Slf4j
@RestController
public class empController {
        @Autowired
        empService empservice;
        @GetMapping("/emps")
        public Result page(@RequestParam(defaultValue = "1") Integer page, @RequestParam(defaultValue = "10") Integer pageSize){
                log.info("分页查询,起始{},查询{}页",page,pageSize);
//                调用service层
                PageBean pageBean = empservice.page(page,pageSize);
                return Result.success(pageBean);
        }
}
```

##### 测试

postman

![image-20250513215109589](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513215109589.png)

前后端联调

![image-20250513215305299](C:\Users\27251\AppData\Roaming\Typora\typora-user-images\image-20250513215305299.png)

##### PageHelper插件

![image-20250524165534782](../../AppData/Roaming/Typora/typora-user-images/image-20250524165534782.png)

引入依赖

这里的版本不能按照课件的1.4.2，否则会强转异常(ClassCastException)

```xml
<dependency>
    <groupId>com.github.pagehelper</groupId>
    <artifactId>pagehelper-spring-boot-starter</artifactId>
    <version>1.4.6</version>
</dependency>
```

EmpMapper

```java
@Select("select* from emp")
List<Emp> list();
```

EmpServer的实现类

```java
@Override
public PageBean page(Integer page, Integer pageSize) {
    //设置分页参数
    PageHelper.startPage(page,pageSize);

    //执行查询
    List<Emp> empList = empMapper.list();
    Page<Emp> page1 = (Page<Emp>)empList;

    //封装bean对象
    PageBean pageBean = new PageBean(page1.getTotal(),page1.getResult());
    return pageBean;
}
```

