# html5-demos

> 该仓库是以html5为基础写的一些事例。

html5增加了很多新特性，如下:

## 一、语义标签

语义化标签使得页面的内容结构化。

| 标签 | 描述 |
| :----: | :----: |
| `<header></header>` | 定义了文档的头部区域 |
| `<footer></footer>` | 定义了文档的尾部区域 |
| `<nav></nav>` | 定义文档的导航 |
| `<section></section>` | 定义文档中的节（section、区段） |
| `<article></article>` | 定义页面独立的内容区域 |
| `<aside></aside>` | 定义页面的侧边栏内容 |
| `<detailes></detailes>` | 用于描述文档或文档某个部分的细节 |
| `<summary></summary>` | 标签包含 details 元素的标题 |
| `<dialog></dialog>` | 定义对话框，比如提示框 |

## 二、增强型表单

HTML5 拥有多个新的表单 Input 输入类型，可以更好的输入控制和验证。

| 输入类型 | 描述 |
| :----| :----|
| color	| 主要用于选取颜色 |
| date	| 选取日期 |
| datetime	| 选取日期(UTC时间) |
| datetime-local	| 选取日期（无时区） |
| month	| 选择一个月份 |
| week	| 选择周和年 |
| time	| 选择一个时间 |
| email	| 包含e-mail地址的输入域 |
| number	| 数值的输入域 |
| url	| url地址的输入域 |
| tel	| 定义输入电话号码和字段 |
| search	| 用于搜索域 |
| range	| 一个范围内数字值的输入域 |

HTML5 新增表单元素

| 名称 | 描述 |
| :----| :----|
| `<datalist>` | 用户会在他们输入数据时看到域定义选项的下拉列表 |
| `<progress>` | 进度条，展示连接/下载进度 |
| `<meter>` | 刻度值，用于某些计量，例如温度、重量等 |
| `<keygen>` | 提供一种验证用户的可靠方法,生成一个公钥和私钥,该标签在新的 Web 标准中已废弃。 |
| `<output>` | 用于不同类型的输出,比如尖酸或脚本输出 |

HTML5 新增表单属性

| 属性 | 描述 |
| :----| :----|
| placehoder	| 输入框默认提示文字 |
| required	| 要求输入的内容是否可为空 |
| pattern	| 描述一个正则表达式验证输入的值 |
| min/max	| 设置元素最小/最大值 |
| step	| 为输入域规定合法的数字间隔 |
| height/wdith	| 用于image类型<input>标签图像高度/宽度 |
| autofocus	| 规定在页面加载时，域自动获得焦点 |
| multiple	| 规定<input>元素中可选择多个值 |

## 三、视频和音频

### [video](https://www.runoob.com/tags/tag-video.html)

```html
<video width="320" height="240" controls>
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.ogg" type="video/ogg">
    您的浏览器不支持 video 标签。
</video>
```
> MP4 = MPEG 4文件使用 H264 视频编解码器和AAC音频编解码器
> WebM = WebM 文件使用 VP8 视频编解码器和 Vorbis 音频编解码器
> Ogg = Ogg 文件使用 Theora 视频编解码器和 Vorbis音频编解码器

### [audio](https://www.runoob.com/tags/tag-audio.html)

```html
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  您的浏览器不支持 audio 元素。
</audio>
```

> 目前，<audio> 元素支持的3种文件格式：MP3、Wav、Ogg。

## 四、Canvas绘图

[Canvas详解](https://www.runoob.com/w3cnote/html5-canvas-intro.html)

```html
<canvas id="myCanvas"></canvas>
 
<script type="text/javascript">
var canvas=document.getElementById('myCanvas');
var ctx=canvas.getContext('2d');
ctx.fillStyle='#FF0000';
ctx.fillRect(0,0,80,100);
</script>
```

## 五、SVG绘图

[SVG](https://www.runoob.com/svg/svg-tutorial.html) 意为可缩放矢量图形（Scalable Vector Graphics）。

SVG 使用 XML 格式定义图像。

```html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  <circle cx="100" cy="50" r="40" stroke="black"
  stroke-width="2" fill="red" />
</svg>
```

[SVG 实例](https://www.runoob.com/svg/svg-examples.html)

## 六、地理定位

> HTML5 [Geolocation](https://www.w3school.com.cn/html5/html_5_geolocation.asp)（地理定位）用于定位用户的位置。

## 七、拖放API

[拖放](https://www.runoob.com/html/html5-draganddrop.html)是一种常见的特性，即抓取对象以后拖到另一个位置。在 HTML5 中，拖放是标准的一部分，任何元素都能够拖放。

```html
<div draggable="true" ondragstart="drag(event)"></div>
<script>
function drap(ev){
    console.log(ev);
}
</script>
```

| 拖动生命周期	| 属性名 | 描述 |
| :----| :----| :----|
| 拖动开始	| ondragstart	| 在拖动操作开始时执行脚本 |
| 拖动过程中	| ondrag	| 只要脚本在被拖动就运行脚本 |
| 拖动过程中	| ondragenter	| 当元素被拖动到一个合法的防止目标时，执行脚本 |
| 拖动过程中	| ondragover	| 只要元素正在合法的防止目标上拖动时，就执行脚本 |
| 拖动过程中	| ondragleave	| 当元素离开合法的防止目标时 |
| 拖动结束	| ondrop	| 将被拖动元素放在目标元素内时运行脚本 |
| 拖动结束	| ondragend	| 在拖动操作结束时运行脚本 |

## 八、WebWorker

 [Web Worker](http://www.ruanyifeng.com/blog/2018/07/web-worker.html) 可以通过加载一个脚本文件，进而创建一个独立工作的线程，在主线程之外运行。

 基本使用：Web Worker的基本原理就是在当前javascript的主线程中，使用Worker类加载一个javascript文件来开辟一个新的线程，起到互不阻塞执行的效果，并且提供主线程和新县城之间数据交换的接口：postMessage、onmessage。

 ```html
<!DOCTYPE html>
<html>

<body>

    <p>Count numbers: <output id="result"></output></p>
    <button onclick="startWorker()">Start Worker</button>
    <button onclick="stopWorker()">Stop Worker</button>
    <br><br>

    <script>
        var w;

        function startWorker() {
            if (typeof (Worker) !== "undefined") {
                if (typeof (w) == "undefined") {
                    w = new Worker("demo_workers.js");//创建一个Worker对象并向它传递将在新线程中执行的脚本的URL
                }
                w.onmessage = function (event) {
                    document.getElementById("result").innerHTML = event.data;//通过evt.data获得发送来的数据
                };
            }
            else {
                document.getElementById("result").innerHTML = "Sorry, your browser does not support Web Workers...";
            }
        }

        function stopWorker() {
            w.terminate();
        }
    </script>

</body>

</html>
```

## 九、WebStorage

WebStorage是HTML新增的本地存储解决方案之一，但并不是取代cookie而指定的标准，cookie作为HTTP协议的一部分用来处理客户端和服务器的通信是不可或缺的，session正式依赖与实现的客户端状态保持。WebSorage的意图在于解决本来不应该cookie做，却不得不用cookie的本地存储。

websorage拥有5M的存储容量，而cookie却只有4K，这是完全不能比的。

客户端存储数据有两个对象，其用法基本是一致。

localStorage：没有时间限制的数据存储

sessionStorage:在浏览器关闭的时候就会清除。

```js
localStorage.setItem(key,value);//保存数据
let value = localStorage.getItem(key);//读取数据
localStorage.removeItem(key);//删除单个数据
localStorage.clear();//删除所有数据
let key = localStorage.key(index);//得到某个索引的值
```

## 十、WebSocket

[WebSocket](http://www.ruanyifeng.com/blog/2017/05/websocket.html) 协议为web应用程序客户端和服务端之间提供了一种全双工通信机制。

特点：

  （1）握手阶段采用HTTP协议，默认端口是80和443

  （2）建立在TCP协议基础之上，和http协议同属于应用层

  （3）可以发送文本，也可以发送二进制数据。

  （4）没有同源限制，客户端可以与任意服务器通信。

  （5）协议标识符是ws（如果加密，为wss），如ws://localhost:8023
