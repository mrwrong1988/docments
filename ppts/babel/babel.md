title: Babel及其插件开发
speaker: 王宇
plugins:
    - echarts

<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

# Babel及其插件开发 {.text-landing.text-shadow}

By 王宇 {.text-intro}


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

# Babel 是什么
> 官网定义： Babel is a JavaScript compiler.

Babel 就是一套解决方案，用来把 ES6 的代码转化为浏览器或者其它环境支持的代码。
注意这里不是转化为 ES5 ，因为不同类型以及不同版本的浏览器对 ES6 新特性的支持程度都不一样，对于浏览器已经支持的部分，Babel 可以不转化。


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

## Babel 的历史
Babel 的作者是 FaceBook 的工程师 Sebastian McKenzie。他在 2014 年发布了一款 JavaScript 的编译器 6to5。从名字就能看出来，它主要的作用就是将 ES6 转化为 ES5。
于是很多人评价，6to5 只是 ES6 得到支持前的一个过渡方案，它的作者非常不同意这个观点，认为 6to5 不光会按照标准逐步完善，依然具备非常大的潜力反过来影响并推进标准的制定。正因为如此 6to5 的团队觉得 '6to5' 这个名字并没有准确的传达这个项目的目标。加上 ES6 正式发布后，被命名为 ES2015，对于 6to5 来说更偏离了它的初衷。于是 2015 年 2 月 15 号，6to5 正式更名为 Babel。


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

# Babel 怎么用

了解了 Babel 是什么后，我们就要开始考虑怎么使用 Babel 来转化 ES6 的代码了。
- Babel 本身提供的 cli 等工具
- 支持和其它打包工具配合使用，譬如 webpack、rollup 等等，可以参考[官网对不同平台提供的配置说明](https://link.zhihu.com/?target=https%3A//babeljs.io/setup.html)。


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

## 使用babel构建基于ES6的node项目

- 安装依赖包
```
npm install --save-dev @babel/core @babel/cli @babel/preset-env
```

- 增加 Babel 配置文件

- 增加构建命令


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

# Babel 工作原理

在了解了如何使用后，我们一起来探寻一下编译背后的事情，同时会熟悉 Babel 的组成和进阶用法。


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

## Babel 工作流程

- Parser 解析源文件
- Transfrom 转换
- Generator 生成新文件

<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">
<img src="/img/babel-principle.jpg">
Babel 使用是 acorn 这个引擎来做解析，这个库会先将源码转化为抽象语法树 (AST)，再对 AST 作转换，最后将转化后的 AST 输出，便得到了被 Babel 编译后的文件。
Babel 为每一个新的语法提供了一个插件，在 Babel 的配置中配置了哪些插件，就会把插件对应的语法给转化掉。插件被命名为 @babel/plugin-xxx 的格式。


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

## Babel 组成
<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">
<img src="/img/babel-composition.jpg">

<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

# Babel 插件开发


<slide class="bg-black-blue aligncenter" image="/img/babel.png .dark">

# Q & A
