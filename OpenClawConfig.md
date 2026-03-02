# 本教程主要是对于学习过程中，OpenClaw快速配置的一个心路历程，希望对你有所帮助。

#### （1）基础环境的安装

- ##### 安装 Node.js （https://nodejs.org/en）

- ##### 安装 OpenClaw（npm i -g openclaw）

#### （2）环境配置

采用 openclaw onboard 进行openclaw的配置，配置步骤如下：

① 先以管理员的方式打开powershell

![1772440515630](./assets/1772440515630.png)

② 输入 openclaw onboard

![1772440608994](./assets/1772440608994.png)

![1772440676012](./assets/1772440676012.png)

![1772440721596](./assets/1772440721596.png)

![1772440798359](./assets/1772440798359.png)

![1772440892971](./assets/1772440892971.png)

将上述页面最小化，然后进行 MiniMax API Key 申请：https://platform.minimaxi.com/docs/guides/models-intro

![1772441050153](./assets/1772441050153.png)

进入账户管理后进行实名认证后生成 API Key。

然后继续以下步骤

![1772441188091](./assets/1772441188091.png)



 ![1772441353714](./assets/1772441353714.png)

![1772441423518](./assets/1772441423518.png)

![1772441486463](./assets/1772441486463.png)

![1772441507613](./assets/1772441507613.png)

![1772441558504](./assets/1772441558504.png)

![1772441622463](./assets/1772441622463.png)

接下来是安装feishu插件：

由于直接安装会出错[openclaw] Failed to start CLI: Error: spawn EINVAL ，因此可以采用以下安装方式：

```
npm install -g @m1heng-clawd/feishu
# 将~\AppData\Roaming\npm\node_modules\@m1heng-clawd\下的feishu 复制到~\.openclaw\extensions目录下（需要先创建extensions文件夹）
# 如果~\AppData\Roaming\npm\node_modules\@m1heng-clawd\找不到，可能是在nodejs安装目录下。
```

然后就可以进行飞书后续配置了，配置见下：

1. 访问飞书开放平台-开发者后台：https://open.feishu.cn/app
2. 创建企业自建应用 

![1772442021704](./assets/1772442021704.png)

3. 添加机器人应用能力 

![1772442075607](./assets/1772442075607.png)

4. 发布应用版本 

![1772442101863](./assets/1772442101863.png)

![1772442140179](./assets/1772442140179.png)

![1772442177411](./assets/1772442177411.png)

然后输入 openclaw channels add，进行飞书配置。

![1772442360435](./assets/1772442360435.png)

![1772442401004](./assets/1772442401004.png)

![1772442498406](./assets/1772442498406.png)

![1772442553728](./assets/1772442553728.png)



在Powershell 输入 openclaw gateway 打开网关，进行后续飞书配置，不然会出现无法连接。

![1772442603909](./assets/1772442603909.png)

![1772442656818](./assets/1772442656818.png)

![1772442746347](./assets/1772442746347.png)

![1772442762130](./assets/1772442762130.png)

![1772442705049](./assets/1772442705049.png)

![1772442729441](./assets/1772442729441.png)

![1772442800192](./assets/1772442800192.png)

![1772442898860](./assets/1772442898860.png)

确认开通权限。然后创建新版本，与上面的步骤类同。



#### （3）测试

在 PowerSheel 键入 openclaw gateway --port 18789

![1772443103474](./assets/1772443103474.png)

然后在飞书进行交互即可。

![1772443145257](./assets/1772443145257.png)


由于未添加各种skills，后续可以通过配置，得到例如每日新闻的功能。




