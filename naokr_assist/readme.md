# 脑壳小助手

## 1. 免责声明

* 此脚本，以作者需求为第一优先，适当兼顾大家需求
* 作者不是您的保姆，谢绝[伸手党](https://baike.baidu.com/item/%E4%BC%B8%E6%89%8B%E5%85%9A)
* 文明友善地发言，`您好` `请` `谢谢` 常挂嘴边
* 由于免费，因此作者没有义务替您解决问题、满足您的喜好
* 脚本开源，鼓励您自己动手、丰衣足食

## 2. 这脚本干什么用的？

此脚本做下面几件事（链接供测试效果）：

1. 在 [题目列表](https://www.naokr.com/question) 页面，基于下列 4 项条件，屏蔽（隐藏）列表中的某些题目：
    * 手动隐藏：页面会出现 [[隐]字按钮](https://user-images.githubusercontent.com/3130930/226784596-d379cf97-9c9d-4159-ac8b-a34204191758.png)，点击后，这道题会在列表页面永久隐藏
    * 题型：例如，可选择隐藏全部 `推理故事` 或 `知识百科` 题目
    * 出题者：支持隐藏指定出题者的全部题目
    * 限时题：支持隐藏全部限时题

2. 在 [单个题目](https://www.naokr.com/question/16330) 页面：
    * 点击“[收入题单](https://user-images.githubusercontent.com/3130930/226784872-510ce69e-36f6-473c-9313-08a40ead4c98.png)”弹出的题单列表，自动按照 最近修改时间 排序
    * 点击[隐]字按钮，可在列表页面永久隐藏这道题
    * 折叠评论区，避免意外被剧透；点击评论区的[抬头空白区域](https://user-images.githubusercontent.com/3130930/226801727-308b6d83-b8fa-4dbc-b105-5167d896f904.png)，可切换展开/折叠
    * 遮盖 正确率、共几人一次通过、侧边栏答题记录，点击对应区域可恢复显示
    * 如果已回答过，页面最上方提示
    * 如果题目是多选题，高亮提醒（避免误以为是单选题，而漏选）

3. 在 [问答列表](https://www.naokr.com/ask) 和 [单个问答](https://www.naokr.com/ask/11817) 页面，点击[隐]字按钮，可在问答列表中永久隐藏这道问答

4. 在 [关注的题单](https://www.naokr.com/user/87670/collections/following) 页面，点击[表头空白区域](https://user-images.githubusercontent.com/3130930/226786154-e6dcb34a-5a1e-4dca-a70f-541532a4a1f7.png)后，可显示[隐]按钮，并隐藏指定的题单
    * 虽然这个功能对其他人“关注的题单”也有效，但主要用途是针对使用者自己“关注的题单”

5. 在 [单个题单](https://www.naokr.com/collection/216) 页面：
    * 点击列表上方“[收录题目](https://user-images.githubusercontent.com/3130930/226786831-3b5cc15c-5527-428e-83fd-1077f8eb9c06.png)”四字，会隐藏 回答过的题目 和 手动隐藏过的题目
    * 如果在“关注的题单”页面，您已经手动隐藏了某个题单，则进入该题单的单个页面后，会自动执行上述过滤
    * 添加 载入全部(自动翻页以载入全部题目) 和 正确降序(按照正确率降序排序) 两个按钮

6. 进入 [创建的题单](https://www.naokr.com/user/87670/collections/created) 页面后，自动载入全部题单，并按照 最近修改时间 排序
    * 虽然这个功能对其他人“创建的题单”也有效，但主要用途是针对使用者自己“创建的题单”

## 3. 支持在什么设备上使用？
* Windows 桌面端：
    * 在 Chromium 102.0 浏览器、ViolentMonkey 2.14.0 下测试通过，可正常运行。
    * 在 Firefox 110.0 浏览器、Tampermonkey 4.18.1 下测试通过，可正常运行。
* Android 手机端：在 Kiwi Browser 107 浏览器、ViolentMonkey 2.14.0 下测试通过，可正常运行。
* 其它系统、浏览器和脚本管理器，作者没时间测试，请自行尝试、自行解决问题
    * Android 上的 Via 浏览器和 X 浏览器，由于对 GM_* APIs 的支持太残缺，不可正常运行此脚本

## 4. 怎样使用

#### A. 安装步骤

1. 为您的浏览器，从下列用户脚本管理器中，任选一个安装：
    * Chrome：[Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) 或 [Violentmonkey](https://chrome.google.com/webstore/detail/violent-monkey/jinjaccalgkegednnccohejagnlnfdag)
    * Firefox：[Greasemonkey](https://addons.mozilla.org/firefox/addon/greasemonkey/)、[Tampermonkey](https://addons.mozilla.org/firefox/addon/tampermonkey/) 或 [Violentmonkey](https://addons.mozilla.org/firefox/addon/violentmonkey/)
    * Safari：[Tampermonkey](http://tampermonkey.net/?browser=safari) 或 [Userscripts](https://apps.apple.com/app/userscripts/id1463298887)
    * Microsoft Edge：[Tampermonkey](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd) 或 [Violentmonkey](https://microsoftedge.microsoft.com/addons/detail/violentmonkey/eeagobfjdenkkddmbclomhiblgggliao)

2. 点击 [这里](https://github.com/luboq/release/raw/main/naokr_assist/naokr_assist.user.js) 安装脑壳小助手脚本

#### B. 设置

* 代码开头有一段设置，请根据说明自行修改
* 建议把脚本自动更新关闭，否则将来更新时，您的自定义设置（例如隐藏的题型、出题者等）会被覆盖掉
* **手动隐藏的题目清单，存储在脚本环境变量中，请注意备份**

## 5. TODO

* 给各项小功能，加上开关
* 提供一个不需要动代码，就能修改配置的方式，这样更新脚本时，设置不会被覆盖

目前还不确定，会有多少人用这个脚本。等真的有人用，确认这些改动值得花时间后，再说吧

## 6. License

[GPL-3](https://choosealicense.com/licenses/gpl-3.0/)