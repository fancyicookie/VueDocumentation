各种教程都让我依旧迷惑，所以开始书写自己的教程。就从Vue文档阅读这儿开始吧。如果你不小心看见了这篇文章，请注意啦，这非常非常地基础，以及很不成熟，只是我想找一个记录并不断进行更新git的一个理由而已。不太具备高深阅读价值，你如果也是小白，那就可以一起看看啦！

首先你需要具备的：了解html、css、JavaScript.

通常在写页面的时候你一定会碰到这种情况，html只写页面，需要引用样式就引入css文件，需要操作dom就引入js文件。

那你说说为什么 Vue 是 Vue.js 呢？它当然就是你写的一些js文件了，只不过它用的语法可能比较高级罢了。

然后让我们跟着 Vue 教程一步一步往下阅读：

第一段讲什么是 Vue，用于构建用户界面的渐进式框架。emm其实我也不太懂它在说什么，那我们就先跳过去。从上手开始。

### 声明式渲染

Vue.js 的核心是 一个允许采用简洁的模板语法来声明式地将数据渲染进DOM的系统，好了（￣▽￣），一定是我的问题，还是看不懂。

然后官方给了一个例子，我们可以自己试试看

![image1](D:\A-Document\Typora\typora-user-images\VueDocumentation\image1.png)

当然以上在页面上显示的结果就是 Hello Vue! 

然后让我们思考一下没有引用js之前的写法，一定是这样的：

![image2](D:\A-Document\Typora\typora-user-images\VueDocumentation\image2.png)

然后陷入沉思，不知道为什么用Vue，明明看起来更复杂了

但后面的解释能看懂了，用了Vue之后 数据 和 Dom 已经被建立起来了，所有东西都是**响应式**的，修改 app.message 的值，页面更新会显示修改后的值。

注意这里修改值不和html直接交互了。

那么为什么呢？

那一定是这个新建立起来的 vue实例 和 dom 之间产生了关联，如何进行关联的呢？比如我们猜测一下，可能是 Vue.js 里面将这个实例对象里的 app.message 的值重新获取，再重新渲染到了页面上，渲染数据的位置为{{ }}。

比如说如果我们再原本的html脚本上修改 Hello Vue! 不是直接利用 `<div id="app">Hello Vue!!!</div>` 修改，而是获取dom之后呢？那么你可能会想到的是这种写法：

![image3](D:\A-Document\Typora\typora-user-images\VueDocumentation\image3.png)

当修改 app.innerText 的时候，同样在页面刷新就会出现相应的值，好像也没有什么不方便的。但是会明显感觉到 {{ message }} 的书写方式可以使用在任何地方，但是以上的书写方式，必须和div在一起使用。
