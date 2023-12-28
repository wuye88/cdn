### 如何使用资源

使用方法：

```
https://cdn.jsdelivr.net/gh/你的用户名/你的仓库名@发布的版本号/文件路径

例：
https://github.com/wuye88/cdn/blob/main/README.md
https://cdn.jsdelivr.net/gh/wuye88/cdn@main/README.md

# 官方路径转换工具：https://www.jsdelivr.com/github
```

官网有更多说明：

```
// 加载任何Github发布、提交或分支
// 注意：我们建议在支持NPM的项目中使用它
https://cdn.jsdelivr.net/gh/user/repo@version/file

// 加载 jQuery v3.6.4
https://cdn.jsdelivr.net/gh/jquery/jquery@3.6.4/dist/jquery.min.js

// 使用版本范围而不是特定版本
https://cdn.jsdelivr.net/gh/jquery/jquery@3.6/dist/jquery.min.js
https://cdn.jsdelivr.net/gh/jquery/jquery@3/dist/jquery.min.js

// 完全省略该版本以获取最新版本
// 你不应该在生产环境中使用它
https://cdn.jsdelivr.net/gh/jquery/jquery/dist/jquery.min.js

//  将“.min”添加到任何JS/CSS文件中以获取缩小版本，如果不存在，将为会自动生成
https://cdn.jsdelivr.net/gh/jquery/jquery@3.6.4/src/core.min.js

// 在末尾添加 / 以获取资源目录列表
https://cdn.jsdelivr.net/gh/jquery/jquery/
```

⚠️默认情况下不支持大于 150 MB 的包或大于 20 MB 的单个文件（对于 GitHub）。 

### 参考

jsdelivr: https://www.jsdelivr.com/



### 一些问题

有时候会碰到`cdn.jsdelivr.net`无法访问的问题，可以使用如下方案解决：

> 相同问题描述：[issues_18397](https://github.com/jsdelivr/jsdelivr/issues/18397) and [issues_18413](https://github.com/jsdelivr/jsdelivr/issues/18413) 。

**解决方法：**

参考使用[jsdelivr-auto-fallback](https://github.com/PipecraftNet/jsdelivr-auto-fallback)项目进行解决，或者更简单的直接使用`fastly.jsdelivr.net`；

```js
  const DEST_LIST = [
    'cdn.jsdelivr.net',
    'fastly.jsdelivr.net',
    'gcore.jsdelivr.net',
    'quantil.jsdelivr.net',
+   'static.mysite.xxx',
  ];
```

