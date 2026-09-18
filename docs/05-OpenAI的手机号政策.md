# 05 · OpenAI 的手机号政策（Google Voice / 接码平台 / 虚拟号能不能注册 ChatGPT）

**注册 ChatGPT 时，手机号是一道硬门槛。这一篇把官方规则摊开讲清楚。**

---

## 一、官方原文（OpenAI 帮助中心）

在 OpenAI 帮助中心的搜索页，有一条明确的问题与结论：

> **"Can I use a premium number, landline, Google Voice, or other VoIP phone number?"**
> *（我能用高级号码、固话、Google Voice 或其他 VoIP 号码吗？）*
>
> 官方解答摘要：
> **"Learn which phone numbers are supported for verification and why landlines, VoIP, and premium numbers are not accepted."**
> *（了解哪些号码被支持用于验证，以及**为什么固话、VoIP 和高级号码不被接受**。）*

**结论：**

| 号码类型 | 能否用于 OpenAI 验证 |
|---|---|
| **真实移动运营商号**（含 MVNO，如 T-Mobile / AT&T 及其实体卡 MVNO） | ✅ **可以** |
| **固话（landline）** | ❌ 不接受 |
| **VoIP**（Google Voice / TextNow / Talkatone 等虚拟号） | ❌ **明确不接受** |
| **Premium number**（付费高费率号段） | ❌ 不接受 |

---

## 二、但有一个"曲线"：WhatsApp 验证

同一段官方文字里还提到：

> **"…including WhatsApp verification where available"**
> *（在可用的情况下，也包括 WhatsApp 验证）*

也就是说：**OpenAI 的验证页面除了短信，还可能提供 WhatsApp 选项**。

**它的意义**：
- 如果你的号**已经绑定了 WhatsApp**，可以尝试走 WhatsApp 收码；
- 但**成功率不稳定**（社区反馈不一），且**依赖你的号能否正常注册 WhatsApp**。

⚠️ **注意**：这条不是"绕过规则"的通道，只是**另一种验证通道**；号码本身仍需满足它的要求。

---

## 三、各类号码的实测/社区反馈（仅供参考）

| 号码来源 | 通过 OpenAI 验证的概率 | 说明 |
|---|---|---|
| **美国实体 SIM（真 T-Mobile / AT&T 及 MVNO）** | ✅ **高** | 线路类型检测为 `CELL PHONE` |
| **实体 eSIM（同运营商）** | ✅ 高 | 同上 |
| **一次性接码平台的号** | ❌ **低** | 号段被大量滥用，多数已被风控 |
| **Google Voice** | ❌ **官方明确拒** | VoIP |
| **Talkatone / TextNow 等 VoIP** | ⚠️ 不确定 | 个别社区称 Talkatone 的号段被识别为 `Wireless`，但**极不稳定、且注册本身就有门槛** |
| **+86 中国大陆号** | ❌ 不接受 | 不在支持范围内 |

---

## 四、怎么判断一个号"够不够真"？

社区常用的方法是查**线路类型（Line Type）**：

| 查询结果 | 含义 |
|---|---|
| **`CELL PHONE`** / `WIRELESS` | ✅ 是"真移动号"，最可能通过 |
| **`VOIP`** / `LANDLINE` | ❌ 基本没戏 |

**可用的第三方查询**：`phonevalidator.com` 等（判断 Cells / Landlines / VOIP；多数有免费额度或付费门槛）。

---

## 五、实操建议

```
① 优先找"真实移动运营商"的号（实体 SIM 或 eSIM）
② 拿到号后，先查一次 Line Type（确认是 CELL PHONE）
③ 再去注册 ChatGPT（全程用固定的、干净的网络出口，别中途换 IP）
④ 注册成功后：绑定邮箱作为第二验证方式
⑤ 长期持有该号（保留收码能力）——将来若被要求"重新验证"，你还能收到
```

---

## 六、一个常被忽略的点

> **"能用它注册"和"能长期持有它"是两件事。**

- **一次性接码**：能收一次码 → 但如果 OpenAI 日后要求重新验证，**号已经没了** → 账号可能拿不回；
- **长期持有的号**：贵一些，但**任何一次重新验证都能应付**。

**所以对你的"打算长期用"的目标**：**优先选能长期保号的实体号。**

---

## 一句话

> **OpenAI 只认"真实移动运营商号"。**
> **VoIP（Google Voice / Talkatone / TextNow）被官方明确排除；接码平台因为滥用基本失效。**
> **要稳，就走实体 SIM / eSIM 的真号。**
