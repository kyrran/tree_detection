# jekyll-dataset 模板
***
- 本模板不需要像GitHub给的主题一样用gem管理插件，克隆本仓库直接调试:
```angular2html
jekyll serve --livereload
```
或者
```angular2html
bash run.sh
```

### 截图
- 横屏<img src="/home/sakurinn/project/blog/Screenshot_XL.png" title="大型设备"/>

- 竖屏<img src="/home/sakurinn/project/blog/Screenshot_SM.png" title="小型设备"/>

### 引入本地文件
- (官方提供的引入本地css)错误用法：
```angular2html
<link rel="stylesheet" href="/assets/css/love.css">
<!- 部署后永远找不到这个路径，调试可用 -->
```
- 正确用法：
```angular2html
<link rel="stylesheet" href="assets/css/love.css">
```
- 引入本地图片正确用法为:
```angular2html
<img src="assets/img/love.jpg">
```
### 新增和修改

- _layout文件夹为页面，通过设计_include内html组件并在页面中引用:
```angular2html
<!- 这里是default.html。我要引用_include文件夹中的eye.html，顺便传点常量过去给它 -->
<body>
{% include eye.html word="to_there" myname="foreverlz1111" %}
</body>
```
```angular2html
<!- 这里是eye.html ，现在可以用刚刚传过来的变量，实际输出内容为 to_there -->
<body>
<p>{{ include.word}}</p>
</body>
```


### How jekyll design template,unfortunately they do not

  ![](jekyll.jpg)