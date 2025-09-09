## Image Auto Upload(自动图片上传)

### **摘要**

image auto upload插件搭配[PicGo](https://zhida.zhihu.com/search?content_id=169702433&content_type=Article&match_order=1&q=PicGo&zhida_source=entity)使用，能自动将ob中插入的图片上传到图床中，大大优化了图片插件体验。

### **引言**

今天要介绍的自动上传图片到图床的插件，能大大优化obsidian的图片插入。但需要注意的是，目前只能搭配picgo一起使用。本人也仅在win端进行了体验。

### **安装**

- # 【**插件安装**】
	- ## 【安装PicGo工具】
		下载[PicGo-Setup-2.4.0-beta.10.exe](https://picgo-release.molunerfinn.com/2.4.0-beta.10/PicGo-Setup-2.4.0-beta.10.exe)安装包（非STA 成员需要开梯子，STA 成员可以不用点开这个链接直接到 STA 网盘下就行，我已经下好放网盘了）
		![Pasted image 20250410123002.png|500](https://i0.hdslb.com/bfs/article/7f76a6413dbc8ac37bbed6d769a286a1394687087.png)

		> **注意:** 安装完后点击运行只在右下角的任务栏中有一个图标，你需要点击这个图标才会进入下图所示的界面，出现如下所示的界面就说明安装成功。
		![Pasted image 20250410125546.png](https://i0.hdslb.com/bfs/article/5eba87e5f2b17e3268d1fa22f2aac8d0394687087.png)

		
		
	- ## 【安装Image Auto Upload插件】
		由于时间有限，我只提供在线插件安装法(需科学环境)。在Obsidian的扩展浏览器中搜索 Image Auto Upload ,点击 Install ，然后启用该插件
		 ![Pasted image 20250410130008.png](https://i0.hdslb.com/bfs/article/2c29ee679efbba43c661bc0870203a0a394687087.png)
		 ![Pasted image 20250410130133.png](https://i0.hdslb.com/bfs/article/a46ba9af569a4397ed55f1e542660804394687087.png)
		![Pasted image 20250410130328.png](https://i0.hdslb.com/bfs/article/5fc0bdc30fdd867054dba4f47aa57236394687087.png)
		至此插件安装完成，下面我们来介绍插件以及软件的配置


### 配置

- # 1. Ob插件配置
	目前插件设置非常简单只需要输入picGo服务端，服务端地址就是 PicGo 桌面程序PicGo-Server中所示地址
	
	![Pasted image 20250410130719.png](https://i0.hdslb.com/bfs/article/21207a0b3aa70817464c7ec511f10f84394687087.png)
	

- # 2. PicoGo配置

- ## 2.1. PicoGo端口配置
因为插件在不同电脑上同步，所以我会将本机的picgo的端口设置和该插件的一致。

![](https://pic4.zhimg.com/v2-c1a236a7c24ab18673470ad90d61a1f9_1440w.jpg)

![](https://pic3.zhimg.com/v2-f2a7f225fdb069f5731fe2223e040238_1440w.jpg)

- ## 2.2. PicGo插件配置
目前软件默认实现如下图所示的存储方式，但是配合插件，能够实现很多方式。我本次使用`picgo-plugin-bilibili`插件利用B站作为图床

![Pasted image 20250410130951.png](https://i0.hdslb.com/bfs/article/d656f032aca857a9f813aa481cf370dd394687087.png)



- ### 2.2.1. 【安装Bilibili图床插件】
1. 打开插件设置
	![](https://picx.zhimg.com/v2-ca6b948766f028bead3713d13400da9f_1440w.jpg)
	PicGo打开界面
	
2. 检索bilibili插件并安装（没有NodeJs先安装[Node.js ](https://nodejs.org/zh-cn)）
	![Pasted image 20250410132715.png](https://i0.hdslb.com/bfs/article/e9d3f2dec431bf4efba8276e59aba6ac394687087.png)
	![Pasted image 20250410133707.png](https://i0.hdslb.com/bfs/article/281f15f212868291f72da43963aacce1394687087.png)

- ### 2.2.2.获取B站SESSDATA
1. 登录[B站](https://www.bilibili.com/)
2. 按`F12`打开控制台
3. 找到`SESSDATA`还有`bli_jct`复制对应填入`SESSDATA`、`csrf`栏目即可
	[![](https://camo.githubusercontent.com/a1d63f73b2aff9f72559435430792f955086756ddaa8b4434d2eaebfbe20efe3/68747470733a2f2f69302e6864736c622e636f6d2f6266732f616c62756d2f633738353339613438383364613239656430646464666330666134653135303537393131653339642e706e67)](https://camo.githubusercontent.com/a1d63f73b2aff9f72559435430792f955086756ddaa8b4434d2eaebfbe20efe3/68747470733a2f2f69302e6864736c622e636f6d2f6266732f616c62756d2f633738353339613438383364613239656430646464666330666134653135303537393131653339642e706e67)
	![image.png](https://i0.hdslb.com/bfs/article/4c10ea2999d2c93ff30ad938c0c9e2ef394687087.png)
4. 把该图床设置为默认图床
 ![image.png](https://i0.hdslb.com/bfs/article/53216e24806bb2d07285a7259d7f62a5394687087.png)
- ### 2.2.3.测试图床
设置成功后，如果picgo能正常上传图片，当你开启此插件后，在ob中复制进图片，就会出现下图

![](https://picx.zhimg.com/v2-b2853b5e6006909b71ca37d66bc1fc07_1440w.jpg)

然后变成一段图床的链接：

![](https://pic4.zhimg.com/v2-8ddca11f0cfc2d77128748eb51664737_1440w.jpg)

如果你设置不成功，如端口匹配，插件则会返回上传失败的字样，如下

![](https://pic3.zhimg.com/v2-c31532576f2a1682453d25e8bfab4a40_1440w.jpg)

- ### 2.2.4.额外设置

关闭掉一个热键，这个热键是 Ctrl+Shift+P 用于快捷上传的热键，会与 Vscode 的 Ctrl+Shift+P 命令面板调出的热键启冲突，关闭方法如下图所示

| ![image.png](https://i0.hdslb.com/bfs/article/d19663c9f0bb1347844f53990cf77fe3394687087.png)<br> | ![image.png](https://i0.hdslb.com/bfs/article/b793923954004dd0f08236cc857c4669394687087.png)<br> |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |

### 使用

唯一的缺点就是,当你换设备时,你需要重新设置一遍上述过程,且你之前设置好的那台PC的登录信息会过期,等你再次使用之前那台PC时候,你仍需要走一边之前的流程


### 问题

