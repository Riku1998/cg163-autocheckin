# cg163-autocheckin
青龙脚本网易云游戏每日自动签到，并使用pushplus推送签到状态到微信

由GamerNoTitle的项目[wyycg-autocheckin](https://github.com/GamerNoTitle/wyycg-autocheckin "wyycg-autocheckin")修改而来

![](https://pic.imgdb.cn/item/654d13ccc458853aef000336.jpg)

## 目录

- [使用方法](#使用方法)
- [变量获取](#变量内容获取)
- [Q&A](#qa)
![](https://pic.imgdb.cn/item/654d0c37c458853aefe92883.jpg)
## 使用方法

### 变量添加

1、下载本项目的cg163-autocheckin.py文件并上传到青龙面板

2、创建定时任务（如图）

图中命令/脚本中task后面的WYCloudGame是文件夹名称，随便填写，第二个WYCloudGame.py填写上传的cg163-autocheckin.py

图中定时规则是每天7点45分执行

![](https://pic.imgdb.cn/item/654d0c37c458853aefe92883.jpg)

3、进入设置，设置环境变量`wyycg_cookies`和 `PPKEY`

## 变量内容获取

### cookie获取

首先我们进入[官网](https://cg.163.com)，进行登录，然后用<kbd>F12</kbd>打开开发者工具后使用<kbd>Ctrl</kbd>+<kbd>F5</kbd>进行刷新，会刷出很多结果

我们在里面找到`@me`这一项，然后在右边找到`Authorization`将冒号后面的内容复制下来就是我们所需要的Cookie

**如果使用多用户，多个cookie请使用`#`分隔**

![](https://img-blog.csdnimg.cn/img_convert/8916bfbda33b93061206f2571665987d.png)

### PPKEY获取

访问[PushPlus官网](https://www.pushplus.plus/)，使用微信登录，直接在[一对一推送](https://www.pushplus.plus/push1.html)复制自己的Token填入变量即可！

## Q&A

## 返回值400并附带一串不知道什么鬼的字符串

例子：
```
    感谢使用来自GamerNoTitle的网易云游戏自动签到脚本！
    今日签到结果如下：
    成功数量：0/1
    失败数量：1/1
    具体情况如下：
    第1个账号签到失败，回显状态码为400，具体错误信息如下：GL8B/hH+v9cYGsm/Ag8PAAwBAr/XztPNzsm/Ag8PChAEv9e/EhACD70QBgQLvREMAf4Wv8m/Ag8PChAEAAu/17/5EtID0tD5EtLWz9b5EtIBA8/5EtT/1AL5EtLP0M2/Gqc=
    GamerNoTitle: https://bili33.top
    网易云游戏自动签到脚本: https://github.com/GamerNoTitle/wyycg-autocheckin
```

首先你需要确认你当天是否已经签到过了才运行的脚本，如果确实先签了到再运行脚本，网易确实会返回400

目前也只发现这种情况会返回400


## 免责声明

使用本脚本造成的封号或任何违反相关法律法规造成的任何责任，由使用者自行承担，开发者不担负任何责任！
