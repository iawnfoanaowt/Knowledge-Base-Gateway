<p align="right">
  <a href="./README.md">简体中文</a> | <a href="./README_EN.md">English</a>
</p>

# OneFind（中文：知寻）

> 明明看过，却想不起来？  
> **OneFind 让你的本地知识随时可用**，帮助用户在毕业论文、科研论文、文献综述、文献阅读以及基金和项目书撰写中，实现一键安装、快速检索与 AI 辅助回答，解决“文献太多、笔记太散、真正要用时却找不到、想不起、串不起来”的常见痛点。
><img width="1536" height="1024" alt="第二期视频封面" src="https://github.com/user-attachments/assets/da0d5d0d-4b49-445d-af3e-4274cfdf966b" />

---

## 下载

- 下载地址：[OneFind Releases](https://github.com/iawnfoanaowt/OneFind/releases)
- 视频介绍：[文献、资料看过就忘？OneFind 让你的知识随时可调用](https://www.bilibili.com/video/BV1kSdaBeEBt)
- 公众号：**OneFind**（内含教程、社群与最新联系方式）

![公众号：OneFind](https://github.com/user-attachments/assets/9488ebce-b03e-4c64-ad3b-a9c542b92601)

---

## 🚀 OneFind 是什么

OneFind 是一个供 AI Agent 调用的**本地知识库插件**。它可以把你电脑里的文献、笔记、附件和文件夹资料接入 AI，让 AI 不只是泛泛回答，而是完全基于你的本地资料进行检索、总结和分析。

你可以用它：

- 🔍 一个入口搜索 Zotero / EndNote / Obsidian / Notion / Mendeley / Citavi / 本地文件夹
- 💬 用自然语言提问，而不是只搜关键词
- 📚 基于本地知识库回答，减少 AI 脱离资料泛泛生成
- ⚡ 自动建立索引，后续检索更快
- 🧠 按任务难度在 Balance / Deep 模式间自动切换
- 🤖 通过 Codex 或 ZCode 调用更多 AI Agent 和模型
- 🧩 支持 Skill / MCP 双路径调用：可选择 `onefind` Skill，也可直接在对话中要求调用 OneFind

一句话理解：

> **OneFind 不是替代你的文献管理软件，而是让 AI 能调用你已经积累的知识。**

---

## ✨ 当前支持

### 支持的 AI 平台

- **Codex**：适合已经使用 ChatGPT / Codex 的用户
- **ZCode**：使用统一的 ZCode Agent，并可搭配 ZCode 中已接入的第三方模型 API 调用 OneFind

两者可以按需选择，也可以同时安装。OneFind 会根据本地环境自动适配。

### 调用方式

Codex 和 ZCode 均支持两种调用方式：

- **Skill 唤起**：在输入框中选择或输入 `OneFind` Skill，再提出检索或分析需求。
- **直接对话调用**：直接说“请调用 OneFind 检索……”“基于 OneFind 查找……”，AI Agent 会通过 MCP 路径调用 OneFind。

两种方式均可使用 OneFind 功能，能减少因电脑环境差异导致无法检测或调用 OneFind 的问题。

### 支持的系统

- **Windows**
- **macOS Apple Silicon（M 系列芯片）**

### 支持的数据源

- Zotero
- Obsidian
- Notion
- Mendeley Reference Manager
- Citavi 7
- EndNote（需授权）
- 本地文件夹（需授权）
- Word / PPT / PDF / Excel / Markdown / CAJ 等文件解析（部分需授权）

> EndNote、本地文件夹、Office 文档和 CAJ 等高级解析能力，可发送机器码至 `zhtaogis@163.com` 获取授权。个人学习与科研使用可申请授权。

---

## 📸 功能演示

### 统一搜索所有知识源

![](https://fastly.jsdelivr.net/gh/bucketio/img1@main/2026/04/16/1776322224610-f069fd40-0e94-4fcf-97a2-6237ddcb06a6.png)

---

### 直接提问，让 AI 基于本地知识回答

![](https://fastly.jsdelivr.net/gh/bucketio/img7@main/2026/04/16/1776322324969-0f13f752-6131-45f2-96e5-7c222afe1ee0.png)

---

### 跨源搜索 or 指定知识源

![](https://fastly.jsdelivr.net/gh/bucketio/img17@main/2026/04/16/1776322355773-3fec2ef3-b09a-4f11-9eed-17a516251928.png)

---

### 自动索引

![](https://fastly.jsdelivr.net/gh/bucketio/img4@main/2026/04/16/1776322397884-f1ce8919-e12e-47ca-8615-e984a5774cab.png)

---

### 本地 + 联网结合

![](https://fastly.jsdelivr.net/gh/bucketio/img15@main/2026/04/16/1776322442958-cffc6d9d-ef03-48bf-80a5-41ffd92e7e87.png)

---

## 💡 它解决什么问题

你可能遇到过：

- 看过很多文献，真正写作时想不起来
- Zotero / EndNote / Obsidian / 本地文件夹分散在不同地方
- 找资料要来回切软件、翻文件、搜关键词
- AI 回答很好看，但不知道来源，不确定是否可信
- 写综述、论文、基金、项目书时，很难把已有材料快速串起来

OneFind 的目标很直接：

> **让知识在你需要的那一刻，可以被立刻调出来。**

---

## ⚡ 快速开始（3 步）

### 1️⃣ 下载

前往 Releases 下载对应系统的最新版安装包：

```text
https://github.com/iawnfoanaowt/OneFind/releases
```

### 2️⃣ 安装

安装前建议先准备好：

- Codex 或 ZCode，至少安装一个
- 至少 1 个有效知识库路径，例如 Zotero、Obsidian、Notion 或本地文件夹
- 如需 Deep 模式，预留一定磁盘空间

安装时可以：

- 自定义 OneFind 安装位置，不限定于 C 盘
- 填写知识库路径，包括最多三个本地文件夹
- 按需安装 deep 模块
- 按需导入授权文件
- 按需启用 MinerU，并填写自己的 API Token

### 3️⃣ 初始化

在 Codex 或 ZCode 中，可以通过 `onefind` Skill 唤起，也可以直接对话调用 OneFind，然后输入：

```text
请调用 OneFind 初始化索引，并检测 deep 模式能否正常调用
```

首次索引耗时取决于资料数量和电脑性能。索引完成后，就可以直接提问。

---

## 🧠 使用方式

在 Codex 或 ZCode 中，OneFind 有两种常用调用方式：

1. **Skill 唤起**：选择或输入 `onefind` Skill 后提问；
2. **直接对话调用**：在问题中写明“请调用 OneFind”或“基于 OneFind 检索”。

例如：

```text
请调用 OneFind，总结我本地知识库里关于水资源匮乏的研究进展
```

你也可以这样问：

- 只在 Zotero 中查找某个方向的文献
- 在 EndNote 和本地 PDF 中对比某几篇论文的方法差异
- 从我的项目材料里提取与监测预警有关的内容
- 基于本地文献整理一个综述框架
- 查找哪些论文提到了某个模型的局限性

---

## 🔬 Balance vs Deep 模式

| 模式 | 适用场景 |
| ---- | -------- |
| Balance | 快速检索、日常查找、简单问答 |
| Deep | 深度分析、正文证据检索、复杂文献问题 |

OneFind 会根据问题难度自动选择合适模式，也可以按需指定。

---

## ⚙️ 安装说明（详细版）

<details>
<summary>点击展开</summary>

### 安装前准备

1. 安装 Codex 或 ZCode，二者至少选择一个。
2. 准备至少 1 个有效知识库路径。
3. 如需使用 EndNote、本地文件夹、现代 Office 文档或 CAJ 解析，请提前准备授权。
4. 如需 Deep 模式，请预留一定磁盘空间。
5. 如需使用 MinerU 增强解析，可提前在 [MinerU API 管理页面](https://mineru.net/apiManage/token) 创建 Token；不使用 MinerU 不影响 OneFind 的本地解析和检索。

> 新版 ZCode 使用统一的 ZCode Agent。需要使用第三方模型时，请先在 ZCode 中配置对应的模型 API。

---

### Windows 安装

1. 从 [OneFind Releases](https://github.com/iawnfoanaowt/OneFind/releases) 下载 Windows 安装包。
2. 双击安装器。
3. 选择 OneFind 安装位置。
4. 填写知识库路径。
5. 按需安装 deep 模块和导入授权文件。
6. 打开 Codex 或 ZCode，通过 `onefind` Skill 或直接对话调用 OneFind。

![OneFind 1.8 安装位置与目标平台](https://paperead-zt.oss-cn-beijing.aliyuncs.com/img/20260811160853259.png)

---

### macOS 安装

当前主要支持 **Apple Silicon（M 系列芯片）** 设备。

1. 先安装 Codex 或 ZCode。
2. 安装 OneFind macOS 版本。
3. 设置 Zotero、Obsidian、Notion 或本地文件夹等知识库路径。
4. 按需完成授权。
5. 开启必要的本地文件访问权限。
6. 通过 `onefind` Skill 或直接对话调用 OneFind，并初始化索引。

![](https://paperead-zt.oss-cn-beijing.aliyuncs.com/img/20260511174720228.png)

首次使用建议输入：

```text
请初始化索引，并检测 deep 模式是否可用
```

![](https://paperead-zt.oss-cn-beijing.aliyuncs.com/img/20260511182059902.png)

---

### ZCode Agent 使用说明

**ZCode**：新版使用统一的 ZCode Agent。安装 OneFind 后，可直接通过 `onefind` Skill 或 MCP 检索本地知识库，也可以搭配 ZCode 中已接入的第三方模型 API 使用。

![image-20260811170840657](https://paperead-zt.oss-cn-beijing.aliyuncs.com/img/20260811170840775.png)

### Skill / MCP 调用说明

Codex 与 ZCode Agent 均支持 Skill 和 MCP 双路径调用 OneFind：

- 选择或输入 `onefind` Skill 后提问，适合希望明确指定工具的场景；
- 直接在对话中说“请调用 OneFind 检索……”或“基于 OneFind 查找……”，适合日常自然语言使用。

两种方式功能一致。双路径设计主要用于提升兼容性，减少因不同电脑环境、平台检测方式或 Skill 识别不稳定导致无法调用 OneFind 的问题。

其他支持 MCP 或 Skill 的 Agent 也可以适配 OneFind。可以向对应 Agent 提出：

```text
请适配访问 OneFind 的 onefind Skill，并配置 OneFind MCP 服务。
```

![image-20260512212949130](https://paperead-zt.oss-cn-beijing.aliyuncs.com/img/20260512212949222.png)

![image-20260512212957559](https://paperead-zt.oss-cn-beijing.aliyuncs.com/img/20260512212957632.png)

更详细的 AI Agent 选择与安装说明，可参考：

[AI Agent 选择与安装指南](https://mp.weixin.qq.com/s/M_8_JRf6MmcWQwPw4Nj8PQ)

---

### 授权说明

默认可访问常见知识库，如 Zotero、Obsidian、Notion 等。

如需启用以下能力，可发送机器码至 `zhtaogis@163.com`：

- EndNote 调用
- 本地文件夹资料解析
- Word / PPT / Excel 文件解析
- CAJ 文件解析

---

### 更新与卸载

**更新：**

1.5 及以上版本可以直接覆盖安装，无需重复填写路径或重新授权。

**卸载：**

OneFind 不会删除你的原始知识库文件。需要卸载时，请使用安装目录中的卸载工具；macOS 端可使用：

```text
/Users/用户名/Library/Application Support/OneFind/OneFind 卸载工具.app
```

**修改知识库路径：**

可以直接通过对话让 OneFind 修改，例如：

```text
请帮我把 Obsidian 知识库路径改为 XXX
```

---

### 常见问题

**Q：安装失败怎么办？**
A：通常与网络中断、权限或旧版本残留有关。可切换网络后重试，或删除旧安装目录后重新安装。

**Q：ZCode 是否必须使用？**
A：不是。已有 Codex 的用户可以继续使用 Codex；希望调用更多模型的用户可以使用 ZCode。

**Q：Mac Intel 芯片能用吗？**
A：当前 macOS 端主要支持 Apple Silicon（M 系列芯片），过老的 Mac 电脑，会影响检索的性能。

**Q：需要 MinerU 处理的 PDF 超过每日限额怎么办？**
A：MinerU API 每天最多处理 200 篇 PDF。超过限额后，可以在接下来的几天中每天重新刷新或重建一次索引。当天已经成功处理的正文会保存在 OneFind 本地缓存中，后续会自动跳过；OneFind 只继续处理尚未完成的 PDF。本地解析成功的 PDF 不会进入 MinerU 队列，也不占用 MinerU 处理数量。

**Q：使用 MinerU 会上传所有 PDF 吗？**
A：不会。OneFind 优先在本地解析，只有解析失败或正文质量较差的 PDF 才会在启用 MinerU 并配置 Token 后提交处理。

**Q：OneFind 会修改我的原始文献吗？**
A：不会。OneFind 对本地只读访问和索引构建，不会替代或破坏原有知识库。

</details>

---

## 📌 适合人群

- 科研人员 / 学生
- 写论文、综述、基金和项目书的用户
- 长期使用 Zotero / Obsidian / EndNote 等知识库软件的人
- 有大量 PDF、现代 Word/PPT/Excel、Markdown、TXT、CAJ 或项目材料的人
- 希望 AI 基于自己资料回答，而不是只靠通用知识生成的人

---

## ⚠️ 注意

- OneFind 不替代科研判断
- OneFind 不自动下载文献
- OneFind 更适合长期知识管理者
- 第三方模型 API、Codex 和 ZCode 等服务需按各平台规则自行配置或订阅

---

## 📄 License

仅限个人学习与科研使用。
如需商用授权或其他特别授权，请联系版权所有者 CrazyGIS。

联系邮箱：`zhtaogis@163.com`

公众号：OneFind

