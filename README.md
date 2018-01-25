文章目录
=======

<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.title }}</a>
      <!-- post.url 的链接是 / 根目录 -->
      <!-- 但是 github.io 是带有 deepinss 前缀的 -->
      <!-- 所以这里加了个点, 表示相对路径 -->
    </li>
  {% endfor %}
</ul>

Welcome to SSS
--------------

该项目始于 2017.12.13 , 致力于让每个人读懂 shadowsocks 的源码, 项目被命名为 SSS, 理解成 shadowsocks study, 或者是 study shadowsocks 都可.

该项目是我定于 2018 年完成的目标.

我是 google 的忠实粉丝, 也经常使用 Wikipedia. 由于 SS 现在过于明显, 总有一天会有被检测出来的风险, 与其静待被封, 不如看下源码, 理解下原理, 也许有一天可以为下一代的科学上网奉献一份力量.

2018.1.23 TODOS
---------------

* 程序流执行面板
* 增加在线的 python 执行环境, 基于[pythonanywhere](www.pythonanywhere.com)

起源
----

在我的第一台 Linode 被封的时候就诞生了这个想法, 但是作为一名底层前端开发攻城狮, 对于网络协议, 加密算法, socket 编程还是有所畏惧, 在第二台 Linode 被限速的时候终于决定要读一读源码.

关于写这个项目
-----------

也许有很多人都诞生了读源码的想法, 但是 python 版本的 shadowsocks 的源码注释还是不足, 而且客户端服务端混合编码, 对于服务端和客户端的思维转换还是有点难度, 所以我希望可以用文档记录下来, 另外在我看源码的时候接触到了很多需要记录下来的地方, 有 shadowsocks 里用到的, 还有 shadowsocks 依赖里面用到的.

我是极客思维, 每一个参数, 每一个变量, 每一个单词缩写, 这些的含义我都想知道. 为此付出了很多, 有时候为了一个单词的缩写, Google, Stack Overflow, Wikipedia, 官方文档, 全部翻遍, 仅仅是为了一个变量的全称是什么, 在这期间也看到了很多人都有这样的想法, 记录下来这些都可以对 SS 的源码阅读有帮助, 这也不仅仅是 SS 的源码解读, 包含 python 的一些模块, openssl, 以及加密, 混淆, 摘要算法, socket编程. 也是这些技术成就了 SS, 致敬开源.

读源码的过程
----------

* 该项目内容几乎全部为原创, 如果有引用全部会指定出处, **尊重原创**是我的原则.

* 我会尽量图形化过程, 而不是贴代码

* 所有的过程我都会在我的本地跑一遍, 确保是正确的

* 该项目不是粗浅的阅读源码, 一定会是深入, 刨根问底式的读源码, 如果你能坚持下来读完整个教程, 相信你可以很明了的知道你的请求是怎么穿过GFW的

* 整个流程不会说一些浅显的道理, 不过会给出详述的链接

获取源码
-------

```shell
git clone https://github.com/shadowsocks/shadowsocks.git
```

克隆下 shadowsocks 主仓库, 该仓库目前有两个分支, **rm**分支的源代码被移除, **master**分支的代码依旧是可用.

致敬
-----

* [github.io](https://github.io)

项目维护者
--------

* [Jiang Xuan](https://github.com/Jiang-Xuan)


动画流程书写
----------

跳转行, 解释这一行代码的作用, 如果该代码调用其他函数, 出现调转函数栏, 
