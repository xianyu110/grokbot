# 将 Grok Bot 接入 QQ 的教程（NapCat + OneBot）

> **作者**：[@lv_chen2006](https://x.com/lv_chen2006)  
> **原文**：[https://x.com/lv_chen2006/status/2116189778060378563](https://x.com/lv_chen2006/status/2116189778060378563)  
> **时间**：2026-10-30 23:25 (Asia/Shanghai)（Asia/Shanghai）  
> **说明**：中文原文整理；保留原作者与源链接，正文为中文。

![封面](https://upload.maynor1024.live/file/1793376476922_cover_2116189778060378563.jpg)

## 摘要速览

- 用 NapCat（NTQQ + OneBot）让 Agent 调 QQ 能力
- 可让 Grok Bot / 其他 harness 在 VPS 或自带主机上一键部署
- 注意：Grok Bot 内置主机可能重置，重要数据勿只放那里
- 第二步把 NapCat 接到 Grok Bot（双向桥接），细节见原文飞书文档

---

## 正文

底部可以阅读飞书文档原文哦
前提：本教程是一篇基于 harness 的教程，请你或多或少对 Codex、Deepseek Harness、Workbuddy 等 harness 软件有一定的接触；另：最好拥有一台自己的云 VPS，没有也无妨，关于 VPS 服务器购置比价平台推荐，请参照上一篇统括版教程。
第一步：部署 NapCat 并登录 QQ
先讲讲什么是 NapCat：NapCat 就是一个托管在 Linux 服务器上的 NTQQ 协议端 + OneBot 适配层。人话讲，就是让 agent 可以通过调用 API 来实现众多的 QQ 功能，包含但不限于流媒体推送、QQ 空间发送、QQ 签名等个人信息更改……
先附上 NapCat 的仓库地址：github.com/NapNeko/NapCatQQ
建议直接把仓库地址粘贴给你的 harness 助理（Grok Bot、Workbuddy、DSH、Codex……能干活的 harness 就行），让它帮你一键部署在服务器上。没有服务器也没关系，可以直接让你的 Grok Bot 在自己的主机上部署并启动服务。注意：Grok Bot 内置主机随时可能重置，且数据有丢失风险，别问我怎么知道的 :)
【配图】部署过程截图（请在发布前从附件里补上）
参考提示词：
 
如果机器人没有直接给你二维码，而是给你 NapCat dashboard 公网访问地址，点进去登录你要部署的 QQ 机器人账号即可。Token 在启动日志，建议直接问你的 Bot。
【配图】NapCat 登录页 / Token（请在发布前补上）
登录上 NapCat 之后，恭喜你！完成了第一步。
感兴趣的可以上 dashboard 看看，UI 还是很精美的。
【配图】NapCat Dashboard（请在发布前补上）
 
第二步：把 NapCat 接到 Grok Bot（双向聊天）
还是老规矩，把下面这段提示词丢给你的 Bot：
 
大致链路：QQ 用户先发「你好」，把消息附上账号 ID 或群聊 ID 等信息拼成 JSON，POST 到 Grok Bot 的 webhook Routine；Bot 作答后，再通过 OneBot 的 send_*_msg 发回同一会话。
即：QQ 消息 → 桥拼 JSON → POST 到主 Bot 的 webhook Routine → Bot 作答 → 调 OneBot send_*_msg 发回同一会话；主聊天留一份 ≤50 字回显。
配置过程中会新建 webhook 触发的例程任务，需要你提供 webhook URL 以及密钥，点击对应例程打开详情填写即可。
最好别指望 Grok Bot 内置主机一直托管服务，主机随时会重置，还是建议入手一台价格合理的 VPS，月付几十块就 OK。
【配图】Webhook 例程配置（请在发布前补上）
 
第三步：验收测试
【配图】QQ 发「你好」与 Bot 回执（请在发布前补上）
是的，现在你可以直接在 QQ 上使唤接待机器人，让她去调度别的机器人执行任务并把成果回执到 QQ，这样就方便许多。
 
结尾
QQ OneBot 接口功能远远不止这些！可以作为管理员管理群文件、群相册，接受闪传文件等等。通过 NapCat 这个开源项目，把 Grok Bot 生态无缝对接进腾讯 QQ，我觉得这是一件很值得做的事。
至于由此扩展出的玩法，后期抽空会分享一些，也欢迎在评论区分享你的玩法！
是土豆还是马铃薯？
我是毛小驴，关注我，获取更多的一手玩法实践技巧～

### 封面

![封面](https://upload.maynor1024.live/file/1793376476922_cover_2116189778060378563.jpg)

---

## 原文链接

[https://x.com/lv_chen2006/status/2116189778060378563](https://x.com/lv_chen2006/status/2116189778060378563)
