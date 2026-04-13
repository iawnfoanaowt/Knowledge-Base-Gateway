# OneFind

`OneFind` （中文名：知寻）是一款供 `ChatGPT Codex` 调用的本地知识库插件，可将 `EndNote`、`Zotero` 与 `Obsidian` 中积累的文献、PDF 和笔记快速接入 AI 工作流，帮助用户在毕业论文、科研论文、文献综述、文献阅读以及基金和项目书撰写中，实现一键安装、快速检索与 AI 辅助回答，解决“文献太多、笔记太散、真正要用时却找不到、想不起、串不起来”的常见痛点。

说明：插件名称Knowledge Base Gateway修改为OneFind（中文名：知寻），并在下一版本1.5 开始使用，感谢社群各位小伙伴取名的建议

## 下载

- 下载地址：[OneFind Releases](https://github.com/iawnfoanaowt/Knowledge-Base-Gateway/releases)
- 视频介绍：[【写论文神器】AI 自动处理文献，一个工具打通 EndNote、Zotero、Obsidian](https://www.bilibili.com/video/BV13CDtBsEcg/?share_source=copy_web&vd_source=31d7ef23294e8878d5a5a9aa3c5763ff)
- 公众号：OneFind
  
![公众号：OneFind](https://github.com/user-attachments/assets/9488ebce-b03e-4c64-ad3b-a9c542b92601)

## 界面示意

### 1. 安装器界面
![安装器界面](docs/screenshots/installer-ui.png)

### 2. 在 Codex 中调用技能
![Codex 技能入口](docs/screenshots/codex-skill-entry.png)

### 3. deep 检测与索引初始化
![deep 检测与索引初始化](docs/screenshots/deep-check-and-index-init.png)

### 4. 普通模式问答示例
![普通模式问答示例](docs/screenshots/answer-example.png)

### 5. deep 模式分析示例
![deep 模式分析示例](docs/screenshots/deep-analysis-example.png)




## 当前版本

- 版本号：`v1.4.2026.10104`
- 发布日期：`2026-04-11`

## 1. 这是什么

做科研时，真正麻烦的通常不是“找不到文献”，而是文献、笔记、批注和 PDF 长期积累后，真正要用时很难快速想起、翻出并串联起来。  
`OneFind` 的目标不是把所有资料一股脑塞给大模型，而是让 `Codex` 先在本地知识库中完成检索、筛选和证据定位，再基于这些证据组织回答。

它更像是一套面向科研场景的本地研究检索引擎：

- 先在本地建立索引
- 再从 `Obsidian`、`Zotero`、`EndNote` 中快速找出最相关证据
- 最后再交给 `Codex` 做分析、梳理和回答

它解决的核心问题是：

- 文献太多，真正要用时翻不到
- 笔记太散，过去看过的内容想不起来
- Zotero、EndNote、Obsidian 分散存放，难以统一调用
- 在线 AI 上下文有限，不能稳定容纳长期积累的大量本地资料

需要特别说明的是：

- 本工具不做文献自动下载
- 更强调用户自己长期阅读、收藏、整理和理解文献
- AI 负责辅助检索、证据梳理和粗略参考
- AI 不能替代研究者自己的理解、判断与思考

## 2. 它适合谁

适合：

- 博士、硕士、本科毕业论文写作
- 科研论文撰写
- 文献综述整理
- 文献阅读与知识回顾
- 基金申请书与项目书撰写
- 已经长期使用 `Zotero`、`Obsidian` 或 `EndNote` 管理资料的研究者

不太适合：

- 只偶尔看几篇文献、没有长期资料积累的人
- 不需要调用本地知识库、只想问通用问题的人

## 3. 它能处理什么

从用户视角看，它可以处理你平时真正会反复调用的本地科研知识：

- `Obsidian` 中的研究笔记、专题整理、长期总结
- `Zotero` 中的题录、摘要、笔记、批注和可提取文本的附件
- `EndNote` 中的文献条目、摘要、关键词、笔记、附件路径，以及可提取文本的 PDF
- 这些内容之间跨来源、跨时间的关联线索

从技术层面看，当前稳定支持的证据层包括：

- `Obsidian` Markdown 内容分块
- `Zotero` 条目元数据
- `Zotero` notes / annotations / fulltext
- `EndNote` 元数据与附件路径
- `EndNote` 可提取文本的 PDF 全文切块

## 4. 默认模式与 deep 模式

### 默认模式

默认模式对应：

- `fast`

适合：

- 快速确认有没有相关研究
- 快速查结论、方法、关键词
- 做初步整理与日常高频检索

特点：

- 更快
- 更适合日常使用
- 不安装 `deep` 也可以正常使用

### deep 模式

`deep` 模式适合：

- 精读某篇论文
- 比较多篇论文的方法、实验和局限
- 梳理更细的证据链
- 当默认模式证据不足时继续深挖

特点：

- 更慢，但更适合重分析任务
- 需要额外安装依赖和模型
- 如果电脑有 `NVIDIA GPU`，会优先利用 GPU版本的deep模块，如果只有核显，则默认安装调用CPU版本的deep模块

如果安装时不启用 `deep`，不会影响下面这些功能：

- 索引建立
- 默认检索
- `Obsidian / Zotero / EndNote` 的日常调用

只是不能使用更重的深度阅读、语义精排和更深入的分析链路。

### 如何手动要求使用 deep

在对话里直接说即可，例如：

- `请用 deep 模式分析这篇论文`
- `请开启 deep 模式，对这几篇论文做方法比较`
- `请使用 deep 模式，基于全文证据回答`

## 5. 安装前需要准备什么

安装时，至少填写下面三类路径中的一个：

- `Obsidian` 库文件夹路径
- `Zotero` 的 `zotero.sqlite`
- `EndNote` 的 `.enl` 文件路径

三者支持任意组合：

- 三选一
- 三选二
- 三者全开

只要至少有一个有效路径，就可以安装和使用。

如果安装后又想补充、替换或禁用某个知识库路径，可通过自然语言的命令，来新增、替换、禁用 Obsidian/Zotero/EndNote 路径，修改后刷新索引即可，无需卸载重装。比如：“把 Zotero 路径改成 D:\Zotero\zotero.sqlite，并重建索引。”

### 路径填写示例

`Obsidian`：

- `C:\Users\用户名\OneDrive\Obsidian`
- `D:\Notes\ObsidianVault`

`Zotero`：

- `C:\Users\用户名\Zotero\zotero.sqlite`
- `D:\Zotero\zotero.sqlite`

`EndNote`：

- `M:\EndNote\My EndNote Library.enl`
- `M:\EndNote\Project A.enl`
- `D:\EndNote\Project B.enl`

当前安装器支持最多填写 `3` 个 `EndNote` `.enl` 文件。多个 EndNote 库会在默认检索时一起参与；如果只想查其中某一个库，可以在对话中说明“只查某个 EndNote 库”，插件会使用对应的库过滤参数。

## 6. 安装后会放到哪里

安装程序只会把文件放到当前用户的 `.codex` 目录下：

- `C:\Users\你的用户名\.codex\Function\kb_gateway`
- `C:\Users\你的用户名\.codex\skills\kb-answer`

如果 `.codex\Function` 不存在，安装器会自动创建。

## 7. 安装程序不会做什么

安装程序默认不会做下面这些事：

- 不写 Windows 注册表
- 不创建桌面快捷方式
- 不创建开始菜单快捷方式
- 不修改系统环境变量
- 不安装系统级 Python
- 不编辑或修改 `Obsidian` 源资料
- 不编辑或修改 `Zotero` 数据库或 storage
- 不编辑、删除或修改 `EndNote` 的 `.enl`、`.Data`、`.eni` 和附件目录

也就是说，安装器只管理它自己的运行目录，不会主动去改你的本地知识库源文件。

## 8. 首次使用与索引说明

首次使用时，程序会先建立本地索引。  
这一步通常比普通问答稍慢，因为要先把本地资料整理成可检索结构。

后续日常使用时，通常直接基于已有索引检索，因此速度会明显更快。

如果出现下面情况：

- `Obsidian` 或 `Zotero` 或 `EndNote` 内容变化较大
- 很久没有使用这个功能
- 例如超过约 `7` 天没有更新索引

系统会判断索引偏旧，并提示刷新或重建。

建议安装完成后，先在 `Codex` 对话中执行：

`请检测deep模式能否正常调用，并初始化建立索引`

这样可以一次完成：

- 检查 `deep` 是否可正常调用
- 完成首次索引构建
- 尽早发现当前机器上的环境问题

## 9. 自动版本与兼容性检查

程序运行时会自动检查：

- 当前本地版本号
- 是否与 GitHub 最新公开版本一致
- `Obsidian / Zotero / EndNote` 当前是否仍可正常适配

如果检测到：

- 本地版本落后
- 数据库结构因软件升级发生变化

系统会给出“建议更新”的提示，但不会阻断当前继续使用。

## 10. 对话安全提醒

建议在 `Codex` 对话中开启完全访问权限。  
原因不是为了修改数据库，而是因为本功能在运行过程中会连续调用多个本地脚本、索引程序和运行环境；如果不给权限，往往会反复弹授权确认，影响使用流畅度。

这里的“完全访问权限”不代表本工具会去修改数据库。  
按照当前设计，`Obsidian`、`Zotero` 与 `EndNote` 源资料始终按只读方式访问。

## 11. 如何卸载

推荐直接使用安装目录中的卸载程序：

- `C:\Users\你的用户名\.codex\Function\kb_gateway\OneFindUninstall.exe`

建议操作顺序：

1. 先关闭 `Codex`
2. 关闭仍在运行的 `Knowledge Base Gateway` 相关窗口或服务
3. 进入 `kb_gateway` 安装目录
4. 双击运行 `OneFindUninstall.exe`
5. 按界面提示完成卸载

卸载时只会移除：

- `C:\Users\你的用户名\.codex\Function\kb_gateway`
- `C:\Users\你的用户名\.codex\skills\kb-answer`

不会删除：

- `Obsidian` 笔记库
- `Zotero` 文献库
- `EndNote` 文库与附件目录
- 其他 `Codex` 技能
- 其他系统文件

## 12. 如何更新

推荐更新方式：

1. 先卸载当前版本
2. 再从 GitHub 下载最新版安装包
3. 重新安装，并按需要重新检查索引与授权状态

这种方式最稳，能避免旧版残留文件与新版逻辑混用。

## 13. 如果安装程序被 Windows 阻止

如果出现“智能应用控制已阻止可能不安全的应用”等提示，通常不是安装脚本本身报错，而是 Windows 对未签名安装器做了拦截。

可临时通过 `Windows 安全中心` 调整：

1. 打开 `设置`
2. 进入 `隐私和安全性`
3. 打开 `Windows 安全中心`
4. 进入 `应用和浏览器控制`
5. 在“智能应用控制”中，将运行模式改为 `评估模式` 或 `关闭`

安装完成后，如有需要可再切回原来的状态。

## 14. EndNote 授权说明

`Obsidian` 和 `Zotero` 默认即可使用；`EndNote` 属于授权控制数据源。

这意味着：

- 这里授权的是 `Knowledge Base Gateway` 的 `EndNote 数据访问功能`
- 不是 `EndNote` 软件本身
- 即使配置了 `.enl` 路径，只要本机没有有效授权 JSON，程序也不会访问 `EndNote`
- 没有授权、授权过期、机器码不匹配、签名无效或时间回拨异常，都会导致 `EndNote` 被禁用
- `EndNote` 被禁用时，不影响 `Obsidian` 和 `Zotero`

### 安装时如何授权

安装器界面会提供单独的 `EndNote` 授权区域，包含：

- 当前机器码显示
- 复制机器码
- 导入授权 JSON

如果安装时没有导入有效授权：

- 安装仍然可以完成
- 但 `EndNote` 会保持禁用
- 后续导入授权后即可恢复可用

### 安装后如何补授权

安装目录中附带独立授权工具：

- `OneFindAuthorization.exe`

可用于：

- 查看当前机器码
- 导入授权 JSON
- 查看当前授权状态

如需申请授权，请联系：

- `zhtaogis@163.com`

## 版权说明

版权归 `CrazyGIS` 所有，仅限个人学习与科研使用，禁止商用、二次售卖和未授权再分发。  
联系邮箱：`zhtaogis@163.com`
