iframe通信
====================

通过 HTML5 的 postMessage() 函数，让主页面 index.html 和 子页面 iframe.html 进行数据通信。

实现功能包括：

+ 设置 iframe.html 页面的高度
+ 设置 iframe.html 页面的全屏

实现原理：

+ 主页面加载 同域或不同域的 iframe 子页面。
+ 通过 iframe 的onload事件，实现主页面和子页面的握手通信。
+ 子页面，获得主页面的通信句柄 handler
+ 子页面，发起修改高度的请求，通过 handler 的 postMessage() 函数，告诉主页面，主页面调用修改高度的事件进行响应。

程序启动

```{node}
anywhere -p 8000
```
