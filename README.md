# 流畅阅读 <img src="./public/icon/192.png" alt="流畅阅读" style="width:1em;" />

> Fluent Read，基于母语般的阅读体验，[B站视频介绍](https://www.bilibili.com/video/BV1ux4y1e73x)。

中文 | [English](https://github.com/Bistutu/FluentRead/blob/main/misc/README_EN.md)

流畅阅读是一款高效的浏览器翻译插件，可以将网页上的文字翻译成任何语言，方便、快捷、直观，支持人工智能引擎。流畅阅读使用 JavaScript、TypeScript 语言结合 [Vue3](https://cn.vuejs.org/) + [Element-Plus](https://element-plus.org/) + [WXT](https://wxt.dev/) 框架编写，可以编译成支持绝大多数浏览器的插件。

流畅阅读支持「仅译文模式」和「双语模式」，为所有人提供可选的翻译模式。

<kbd><img src="./misc/sample-git-1.gif" alt="sample-git-1.gif" style="width: 80%; max-width: 100%;border: 1px solid black;"></kbd>

<kbd><img src="./misc/sample-git-4.gif" alt="sample-git-4.gif" style="width: 80%; max-width: 100%;border: 1px solid black;"></kbd>

<kbd><img src="./misc/screenshot-3.png" alt="sample-git-1.gif" style="width: 40%; max-width: 100%;border: 1px solid black;"></kbd>

# 安装指南

> 插件已经上架各大浏览器的应用商店，可以点击下方链接进行安装：
>

- **Chrome 浏览器**：[点击安装](https://chromewebstore.google.com/detail/流畅阅读/djnlaiohfaaifbibleebjggkghlmcpcj?hl=zh-CN&authuser=0)、[备用链接](https://www.crxsoso.com/webstore/detail/djnlaiohfaaifbibleebjggkghlmcpcj)
- **Edge 浏览器**：[点击安装](https://microsoftedge.microsoft.com/addons/detail/%E6%B5%81%E7%95%85%E9%98%85%E8%AF%BB/kakgmllfpjldjhcnkghpplmlbnmcoflp?hl=zh-CN)
- **Firefox（火狐）浏览器**：[点击安装](https://addons.mozilla.org/zh-CN/firefox/addon/%E6%B5%81%E7%95%85%E9%98%85%E8%AF%BB/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)
- **其他浏览器，尝试**：[点击安装](https://www.crxsoso.com/webstore/detail/djnlaiohfaaifbibleebjggkghlmcpcj)

若直接安装失败，也可以下载插件的压缩包，然后打开浏览器的**管理扩展程序窗口**、**激活开发者模式**，将压缩包**拖进浏览器**内进行安装。

<img src="./misc/screenshot-1.png" alt="sample-git-1.gif" style="width: 45%; max-width: 100%;border: 1px solid black;"><img src="./misc/screenshot-2.png" alt="sample-git-2.gif" style="width: 45%; max-width: 100%;border: 1px solid black;">

> 手机版如何安装？

手机版目前只支持使用**油猴插件**进行安装，油猴脚本相对于正式版本有更新延迟，安装方式如下：

1. 在浏览器中安装 [油猴插件](https://www.tampermonkey.net)（如已安装则跳过）
2. 在油猴中安装 [流畅阅读](https://greasyfork.org/zh-CN/scripts/482986-%E6%B5%81%E7%95%85%E9%98%85%E8%AF%BB) 插件

# 特点介绍

1. **支持多种翻译方式**

   - 仅译文模式
   - 双语模式

2. **支持多种翻译引擎**

   微软翻译、谷歌翻译、DeepL翻译、百度翻译、小牛翻译、OpenAI、Claude、Gemini、Kimi（月之暗面）、智谱清言、通义千问、文心一言、百川大模型、零一万物、DeepSeek、MiniMax、无向芯穹、⭐️自定义引擎等。

3. **支持多种快捷方式**

   1. 快捷键翻译：将鼠标悬浮在文本上，并按下设定的快捷键即可翻译，目前支持的快捷键有 Ctrl、Alt、Shift、波浪号键。
   2. 鼠标翻译：**双击鼠标**、**长按鼠标**、**鼠标滚轮单击**可触发翻译。
   3. 滑动翻译：持续按住快捷键，同时用鼠标滑动选择需要翻译的文本区域。

4. **支持缓存与回译**

   为了避免重复翻译句子、减少请求次数，流畅阅读基于每个页面做了翻译缓存，你无需关心具体细节（蓝色表示正常翻译、绿色表示使用缓存），当你使用缓存时，插件不会发生网络请求。

   <kbd><img src="./misc/sample-git-3.gif" alt="sample-git-1.gif" style="width: 80%; max-width: 100%;border: 1px solid black;"></kbd>

   当你将鼠标悬浮在已翻译的文本上并按下快捷键时，会触发**回译功能**。

   <kbd><img src="./misc/sample-git-2.gif" alt="sample-git-1.gif" style="width: 70%; max-width: 100%;border: 1px solid black;"></kbd>

# 常见问题解答

<details>
    <summary>1、我应该如何获取token？</summary>
  &emsp;&emsp;如果你想获取翻译服务的token，建议直接在百度或Google中以关键词 <code>模型名称 + api</code> 进行搜索，如 <code>月之暗面 api</code>
</details>
<details>
    <summary>2、我的token会不会被别人窃取？</summary>
  &emsp;&emsp;不会。流畅阅读会将你的token全部存储在浏览器本地，没有任何第三方能够窃取，包括我们自己。
</details>
<details>
  <summary>3、我的翻译会被其他人获取吗？</summary>
  &emsp;&emsp;不会。流畅阅读会将你的所有翻译请求<strong>直接转发给翻译服务提供商</strong>，没有任何人可以获取你们之间的对话记录。
</details>
<details>
    <summary>4、为什么翻译的内容不准确？</summary>
&emsp;&emsp;翻译质量主要取决于所使用的翻译模型，<strong>可以更换其他模型进行尝试</strong>。
</details>
<details>
    <summary>5、为什么要开源？</summary>
&emsp;&emsp;这是作者在大学期间的最后一份作品，也是一份毕设。
</details>
<details>
    <summary>6、这款软件如何盈利？</summary>
&emsp;&emsp;软件目前没有盈利的地方。
</details>



# 版本更新记录

- 2024-05-28: 0.07 版本
  1. 接入 Coze 国际/国内版
  2. 增加文心一言 ERNIE-Speed、通义千问 Qwen-Long 模型
  3. 增加触屏设备翻译方式，如双指翻译、双击翻译等
  4. 优化其他事项
- 2024-05-19: 0.05 版本
  1. 增加“双语翻译”模式
  2. 接入谷歌翻译、百度翻译、百川大模型、零一万物等引擎
  3. 支持 GPT-4o 等模型
  4. 增加鼠标事件，支持快捷翻译
  5. 增加对自定义接口的支持，兼容 [one-api](https://github.com/songquanpeng/one-api)、[new-api](https://github.com/Calcium-Ion/new-api) 等方式调用
- ...
- 2023-12 beta 版本

# 开源许可证

[GPL-3.0 license](https://github.com/Bistutu/FluentRead#)

# 如何运行程序？

```shell
git clone https://github.com/Bistutu/FluentRead.git
cd ./FluentRead
pnpm install && pnpm dev
```

```shell
pnpm zip	# 打包为支持 Chromium 内核的插件
pnpm zip:firefox	# 打包为支持 FireFox 内核的插件
```

# Star 历史记录

[![Star History Chart](https://api.star-history.com/svg?repos=Bistutu/FluentRead&type=Date)](https://star-history.com/#Bistutu/FluentRead&Date)

# 赞赏码

如果您想向作者表达感谢，请使用微信扫描下方二维码，您的名字将出现在赞助名单上。

<img src="https://oss.thinkstu.com/typora/202406102143926.jpg?x-oss-process=style/optimize" alt="wechat" style="width: 40%; max-width: 100%;border: 1px solid black;">

（赞助名单最后更新于：2024年11月14日）

| 序号 |       🌼赞助者🌼        | 赞助金额 |
| :--: |:--------------------:| :------: |
|  1   |         TOO          |   100    |
|  2   |         匿名          |   100    |
|  3   |        很酷的小当家        |    57    |
|  4   |       coonut🥥       |    36    |
|  5   |      hoochanlon      | 23.7 |
| 6 | Juncai（公众号“译观”） | 20 |
| 7 |        一懒众山小.        |    18    |
| 8 |          嘴馋          |    17    |
| 9 |      听说海能吞掉鱼的眼泪      |    17    |
| 10 | 吆吆好叼啊 | 10 |





























