# 闲鱼 Gemini AI Pro 赠金：在命令行用上 Gemini 4 Argon

> **作者**：[@cgnot996](https://x.com/cgnot996)  
> **原文**：[https://x.com/cgnot996/status/2115647822087544957](https://x.com/cgnot996/status/2115647822087544957)  
> **时间**：2026-10-29 11:32 (Asia/Shanghai)（Asia/Shanghai）  
> **说明**：中文原文整理；保留原作者与源链接，正文为中文。

![](https://upload.maynor1024.live/file/1793376455918_2115647822087544957_0_3_2115643673014935552.jpg)

![](https://upload.maynor1024.live/file/1793376461849_2115647822087544957_1_13_2115645504168374273.jpg)

![](https://upload.maynor1024.live/file/1793376462265_2115647822087544957_2_3_2115645564021051392.jpg)

## 摘要速览

- 闲鱼低价 Gemini AI Pro 也有每月赠金，别浪费
- 关键：AI Studio 付费层 + Cloud Prepay 余额 > 0，赠金才会真正用于 API
- 作者用 Grok Bot 把 Gemini 4 Argon 配到 Pi Agent，与其他模型分流
- 步骤含 Billing、Prepay、Credits、付费项目 Key；以 Google 当前页面为准

---

## 正文

😤 全体起立！我找到了让闲鱼 5 块买的 Gemini AI Pro 也能在命令行用 Gemini 4 Argon 模型的办法！

Gemini AI Pro 每个月都会给 $10 赠金！闲鱼 5 块买的也有赠金！大家这笔钱都别浪费了！

可以在 https://t.co/VofhNaJicI 查看你的赠金额度

我从 3 月开始已经攒了 $70 赠金了，换算港币 468，这个一直没用到，有过期时间的

怎么用上还有些门道，完成 Google 账号这边的配置以后我让 Grok Bot 把 Gemini 4 Argon 配到了 Pi Agent 上，这样不影响 agy 继续使用 Gemini 3.8 Flash，完整的步骤放下面了：

1️⃣ 打开 AI Studio 结算
 https://t.co/iwbntqXfRR（或左栏 Billing / 结算）

2️⃣ 确认已是付费层页面应显示
 Tier / 付费、结算账号/「我的结算账号」。 若还是 Free：按提示 Upgrade / Set up billing，绑卡并选结算账号。

3️⃣ 开 Cloud Prepay 并保证预付余额 > 0
同一 Billing 页 → 预付费 / Cloud Prepay → 充入 $5。预付余额为 $0 → 符合条件的赠金停用，API 会 402 预付有余额后，先扣赠金，再扣预付；赠金用完前一般不会动到预付本金（你问过的那种）

4️⃣ 确认赠金可用
Billing 里找 Credits / 赠金 / 符合条件的 GCP 赠金（你这边约 HK$468，多笔 Google Developer Program monthly，状态「可用」）。 Free Trial 过期的那笔不能给 Gemini API 用。

5️⃣ 用付费项目的 Key 调 API
https://t.co/v5DI5o8Wpn 用挂在付费结算账号上的项目 Key。 不要用还挂在 Free 的项目，否则走不到这套赠金。

6️⃣ 配置 Argon 模型到 Pi Agent
直接把提示词发给 Bot：这是我的 Google AI Studio Key：xxxxx，不要直接配 agy 上，帮我配置到 pi agent 上，没有的话下载一个，帮我测试 argon 模型是否可用

我测试用 Argon 跑了一个鹈鹕骑自行车测试，效果还挺不错的

不要再浪费这笔钱了，蹬起来！

### 配图

![](https://upload.maynor1024.live/file/1793376455918_2115647822087544957_0_3_2115643673014935552.jpg)

![](https://upload.maynor1024.live/file/1793376461849_2115647822087544957_1_13_2115645504168374273.jpg)

![](https://upload.maynor1024.live/file/1793376462265_2115647822087544957_2_3_2115645564021051392.jpg)

---

## 原文链接

[https://x.com/cgnot996/status/2115647822087544957](https://x.com/cgnot996/status/2115647822087544957)
