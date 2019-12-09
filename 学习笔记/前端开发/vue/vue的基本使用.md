### 1.什么是MVVM模式
- Vue是基于MVVM模式而开发出来的，M-Model,V-View,VM-View Model,其中的Model中存储的数据逻辑可以通过View Model实例传送给视图层，从而实现视图层的数据更新。
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>数据单向传递</title>
         <!--1.下载导入Vue.js-->
        <script src="js/vue.js"></script>
    </head>
    <body>
        <div id="app"><!-- View 视图层 -->
          <p>{{ message }}</p>
        </div>
        <script>
        // 2.创建一个Vue的实例对象
          let vue = new Vue({
        // 3.告诉Vue的实例对象, 将来需要控制界面上的哪个区域
              el: '#app',
        // 4.告诉Vue的实例对象, 被控制区域的数据是什么
           data: {//Model 数据模型
            message: "hello world!"
          }
    });
    </script>
    </body>
</html>
```
- 在上述代码中，vue实例对象是视图层和数据模型层进行数据交换的桥梁。
- data对象中的数据会通过vue实例的传递，传递到视图层对应的插值语法中，实现数据的显示。这个过程数据的传输方向是单向的。
