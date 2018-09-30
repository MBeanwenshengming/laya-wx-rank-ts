# laya-wx-rank-ts
Layabox(windows版本，因为没钱买苹果)开发的微信小游戏排行榜demo，使用开放数据域，开发用的Typescript语言，对应Laya类库版本为1.7.19

# 使用步骤
为了同时使用版本管理和图集加载，做了一些特殊的处理，具体原理会在下一小节说明，这里请先照着用吧:)。
1. 下载本项目解压，可以看到三个文件夹,main为主代码，open-data为开放数据域代码，wxgame对应最后发布出来的小游戏代码（现在是空的，等这些步骤执行完，它就有东西了)。
2. 在两个Layabox窗口中分别打开main项目和open-data项目。
3. 在两个项目中都切换到编辑模式，按F12导出资源。
4. 执行main项目下的copy.bat脚本，将排行榜图集拷贝到单独的文件夹下。
5. main项目切换回代码模式，编译，然后发布项目。这里是重点，发布项目的选项，要勾选启用版本管理，后续执行脚本要选择main项目下的release.bat文件。然后就能看到与main平级的wxgame文件夹下有内容了。
6. 继续发布open-data项目，注意，发布选项，*不要*勾选版本管理，后续执行脚本选择open-data项目下的release_opendata文件。
7. 用微信web开发者工具打开wxgame文件夹，填入你自己的小游戏AppID，即可执行看到效果了。

界面比较丑，请忽略
![view](./view.png)

# 代码说明
### 基础实现

### 版本管理&图集使用