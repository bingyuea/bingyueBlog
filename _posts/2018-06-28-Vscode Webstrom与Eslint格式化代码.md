---
	layout:     post
	title:      Vscode Webstrom与Eslint格式化代码
	subtitle:   个人学习总结
	date:       2018-06-28-Vscode Webstrom与Eslint格式化代码
	author:     饼yue
	header-img: img/post-bg-web-standard.jpg
	catalog: true
	tags:
	    - Eslint
---
### vscode webstrom 保存自动按照 Eslint 格式化代码实践

#### vscode 相关配置

- 安装 ESlint 插件

![](http://ww1.sinaimg.cn/large/e9ff3c49gy1fsr0wn12t1j21hc0sv0xa.jpg)

- 设置 vscode 的 用户设置

![](http://ww1.sinaimg.cn/large/e9ff3c49gy1fsr12gnglgj21hc0u0n3m.jpg)

```
 // 控制编辑器是否应在键入后自动设置行的格式
 "editor.formatOnType": true,
 // 控制编辑器是否应在保存后自动设置行的格式
 "editor.formatOnSave": true,

"eslint.validate": [
    "javascript",
    "javascriptreact",
    "html",
    "vue",
    {
        "language": "vue",
        "autoFix": true
    },
    {
        "language": "vue",
        "autoFix": true
    }
],
"eslint.options": {
    // 这个是需要装的一个插件
    "plugins": ["html"],
    // 这个是你配置的eslintrc文件的地址
    "configFile": "C:/spareWork/vueeslint/.eslintrc.js"
}
```

这样就配置好了保存使用 eslint 格式化代码

#### 安装 Eslint

- 如果你初始化 vue 项目时已经安装过 Eslintj 就不需要做任何操作了，可以直接玩耍了

- 如果没有安装过 Eslint

1.  如果只有在当前项目中使用 Eslint 则在项目根目录下面安装 ：

    ```
        npm install eslint --save-dev
    ```

2.  如果全局安装

    ```
        npm install -g eslint
    ```

最后附上 一份 .eslintrc 配置[vue-element-admin](https://github.com/PanJiaChen/vue-element-admin/blob/master/.eslintrc.js)

---

#### webstrom配置相关插件

1. 设置引用eslint的引用路径

Preferences | Language & Frameworks | JavaScript | Code Quality Tools | ESLint->Configuration file

![](https://img-blog.csdn.net/20180402230835823?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM0NzQxMDQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

2. 绑定快捷键

Preferences | Keymap->搜索“eslint”关键字，找到Fix ESLint Problems，添加你喜欢的快捷键。

！[](https://img-blog.csdn.net/2018040223082686?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTM0NzQxMDQ=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

    本文参考

[手摸手，带你用 vue 撸后台 系列一(基础篇)](https://segmentfault.com/a/1190000009275424)
[使用 VSCode + ESLint 实践前端编码规范](https://segmentfault.com/a/1190000009077086?from=timeline&isappinstalled=0)
[Vscode 一些常用插件](https://github.com/varHarrie/varharrie.github.io/issues/10)
[webstrom配置按照eslint格式化代码](https://blog.csdn.net/u013474104/article/details/79796853)
