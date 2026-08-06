# Obsidian Bangumi 插件

**从 Bangumi 导入条目、管理追番列表、自动检测更新。支持自定义笔记路径模板、封面下载、时间轴视图。**  

[GitHub 仓库](https://github.com/yuangwu/obsidian-bangumi)
[作者主页](https://github.com/yuangwu)

---

## 📖 简介

`obsidian-bangumi` 是一个为 [Obsidian](https://obsidian.md/) 设计的插件，它将 [Bangumi.tv](https://bangumi.tv/) 的动漫、书籍、音乐、游戏等条目无缝整合到您的知识库中。 

本项目的灵感源于以下开源项目: [Bangumi](https://bgm.tv/) 的 [Bangumi 开源项目](https://github.com/bangumi)、@ [月涟 _luvian](https://space.bilibili.com/67571043) 的 [luvian 114/Bangumi-to-obsidian](https://github.com/luvian114/Bangumi-to-obsidian)、@ [北漠海](https://space.bilibili.com/1065768987) 的 [beimohai/Bangumi-to-obsidian-lite](https://github.com/beimohai/Bangumi-to-obsidian-lite)、@ [一般の智人](https://space.bilibili.com/286674433) 的 [Yasikap/Bangumi-Bridge-Obsidian](https://github.com/Yasikap/Bangumi-Bridge-Obsidian)、@ [景深很浅](https://space.bilibili.com/17915477) 的 [Obsidain 影音库的模板](https://www.bilibili.com/video/BV1hiE9zAEj4/)，在此对以上开发者表示感谢！

---

## ⚠️ 许可说明

本软件采用 **AGPL-3.0 双重许可 (Dual Licensing)** 模式：

- **🔓 开源版**：在 [GNU Affero General Public License v3.0](./LICENSE) 下免费提供，适用于**个人、研究人员和开源项目**。您可以在遵守 AGPL-3.0 全部条款的前提下自由使用、修改和分发本软件。
- **💼 商业版**：对于**无法遵守 AGPL-3.0 强互惠条款**的组织（例如需要将本软件集成到专有商业产品中，或提供 SaaS 服务但不希望公开源码），可向作者[购买商业许可证](./COMMERCIAL_LICENSE.md)，获得专有使用权。

**您无需点击任何协议即可使用开源版本。** 首次启动时，插件会展示许可证信息弹窗，仅作告知用途，不会阻塞功能。

### 🤝 贡献者须知

本项目欢迎社区贡献，但所有贡献者需在提交第一个 Pull Request 时签署[贡献者许可协议 (CLA)](./CLA.md)，授予项目维护者对贡献代码进行再许可（包括商业许可）的权利，以维持双重许可模式的可持续性。签署方式详见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

详细条款请阅读：
- [LICENSE](./LICENSE) — AGPL-3.0 完整协议文本
- [COMMERCIAL_LICENSE.md](./COMMERCIAL_LICENSE.md) — 商业许可证说明
- [CLA.md](./CLA.md) — 贡献者许可协议

---

## ✨ 功能

- ☑️ 导入动画、书籍、音乐、游戏、三次元条目
- ☑️ 同步个人 Bangumi 收藏（想看/在看/看过等所有列表）
- ☑️ 支持保存封面至本地或图床（PicGo，实验性）
- ☑️ 完全自定义笔记文件名模板（支持多级目录 `{{type}}/{{date}}/{{title}}`）
- ☑️ 追番列表集中看板，显示更新状态、进度、评分
- ☑️ 智能更新检测（Bangumi API / 本地文件夹 / 网页抓取）
- ☑️ 进度条可视化，支持批量标记已同步及撤销（3 秒），新增 **取消同步** 功能，可重新标记为“有更新”
- ☑️ 三视图切换：**列表 / 卡片 / 时间轴**
- ☑️ **时间轴视图**：按播出日期或记录日期展示条目时间线，支持季度分组、升降序
- ☑️ 统计看板可折叠
- ☑️ 支持移动端导入（封面下载仅在桌面端完全支持）
- ☑️ 自定义模板，按条目类型指定不同模板
- ☑️ 侧边栏快捷入口，快捷键支持（`/` 聚焦搜索，`Esc` 清空）
- ☑️ **首次启动 EULA 协议确认**（已改为非阻塞许可证信息展示，无需点击即可使用）
- ☑️ **打赏支持入口**：命令面板、追番工具栏、设置页均可弹出赞助弹窗（赞助链接由开发者硬编码，不可篡改）
- ☑️ **断点续传批量导入**：若导入过程中断，下次启动会自动检测残留状态文件，询问是否继续或清理
- ☑️ **弹窗与时间轴样式优化**：彻底消除“框中框”，卡片单层透明，融入 Obsidian 原生模态框
- ☑️ 暗色主题完美适配

---

## 📦 如何安装

### 从 Obsidian 插件中心（即将上线）
1. 进入 Obsidian 插件中心
2. 搜索 `obsidian-bangumi`
3. 安装并启用

### 手动安装
1. 从 [Releases](https://github.com/yuangwu/obsidian-bangumi/releases) 页面下载 `main.js`, `manifest.json`, `styles.css`
2. 将文件复制到你的 vault 的 `.obsidian/plugins/obsidian-bangumi/` 文件夹（如不存在请新建）
3. 在 Obsidian 插件中心启用该插件

---

## 🚀 如何使用

### 1. 首次使用与许可证信息

1. 安装并启用插件后，Obsidian 会弹出一个**许可证信息**窗口，展示 AGPL-3.0 开源协议摘要及双重许可说明。您可以直接关闭窗口，无需任何操作即可正常使用全部功能。
2. 如果您想再次查看许可证信息，可通过命令面板执行 `Bangumi: 查看许可证信息`。

> **样式优化**：许可证信息弹窗现已完全融入 Obsidian 原生模态框，无多余背景或边框，自动适配暗色/亮色主题。

### 2. 基础设置

打开 **设置 → 插件选项 → Bangumi**，进行必要配置：

#### 📁 基本设置
- **基础存储路径**：笔记存放的根目录（默认 `📚 媒体库/ACG`）。
- **Bangumi 用户 ID**：你的数字 ID（例如 `1234567`）。可在 Bangumi 个人主页 URL 中找到。
- **Access Token (可选)**：用于访问私有收藏。获取方式：登录 Bangumi → 设置 → Access Token 管理。
- **笔记文件名模板**：定义生成笔记的路径规则，支持变量（见下方“模板变量参考”）。示例：
  - `{{type}}/{{title}}` → `动画/葬送的芙莉莲.md`
  - `{{date}}/{{type}}/{{title}}` → `20231001/动画/葬送的芙莉莲.md`

#### 📥 导入设置
- **冲突处理策略**：导入时若已有同名笔记，可选择“询问”（`ask`）、“覆盖（保留用户字段）”（`overwrite`）或“跳过”（`skip`）。
- **分页延迟 / 条目间延迟**：控制 API 请求频率，避免限流。
- **可选数据**：勾选“角色列表”、“制作人员”、“关联作品”等，会增加请求次数。

#### 📋 模板设置
- **启用自定义模板**：允许使用 Obsidian 笔记模板文件。
- **默认模板路径**：指向你创建的模板笔记，例如 `Templates/Bangumi模板.md`。
- **按类型指定模板**：可为不同类型的条目分配专用模板。

其他设置项在各自标签页中有详细提示，可按需调整。

### 3. 单条目导入

1. 使用 <kbd>Ctrl</kbd> + <kbd>P</kbd> 打开命令面板，执行 **Bangumi: 单条目导入（搜索并选择）**。
2. 在弹出框中输入作品名称（支持中日文），按 Enter 确定。
3. 在搜索结果中点击要导入的条目（可翻页）。
4. 选择“状态”（如“想看”、“看过”），若为动画还可选择“改编类型”。
5. 插件将自动拉取条目详情，生成笔记并打开。

### 4. 批量导入收藏（支持断点续传）

- **全量批量导入**：执行 `Bangumi: 全量批量导入（无筛选）`，选择条目类型（如动画）和列表（如“想看”），直接导入该列表所有条目。
- **分类筛选批量导入**：执行 `Bangumi: 分类筛选批量导入`，在前一步基础上增加筛选条件（平台、标签、NSFW、关键词），只导入符合条件的条目。
- **断点续传**：若导入过程中 Obsidian 被强制关闭或插件重启，下次启动时会自动检测到残留的状态文件（位于基础路径下，命名如 `批量导入状态_动画_看过.json`），并弹出询问窗口，您可以选择“继续导入”或“清理状态文件”。若继续，将从断点处继续导入未完成的条目，避免重复。
- 导入完成后，自动生成导入报告（Markdown 文件）并存于基础路径下，状态文件自动删除。

### 5. 追番列表与更新检测

- 点击侧边栏的 📖 图标，或执行 `Bangumi: 打开追番列表`，进入追番看板。
- 列表自动扫描 `基础存储路径` 下所有 `tags` 包含 `bangumi` 的笔记。
- **更新检测**：插件会根据检测方式（自动/API/本地/网页）扫描每个条目的最新进度，并与笔记中的已看进度对比，显示更新状态。
- **操作**：
  - 筛选：可按类型、状态（有更新/已同步）、具体收藏状态、平台进行过滤。
  - 排序：按更新量、标题、类型、评分、最后检测时间排序。
  - 视图：点击 📋 列表 / 🔲 卡片 / 🕐 时间轴 切换。
  - 快速标记：点击 ✅ 将某一有更新的条目标记为“已同步”（可撤销，3 秒内）。点击 ↩️ 可将已同步的条目重新标记为“有更新”，以便重新检测。
  - 批量操作：底部操作栏可批量标记已同步、**批量取消同步**、批量打开观看网址、导出表格到剪贴板。
- **时间轴视图**：按作品的播出/发售日期或你的记录日期生成纵向时间线，支持年份/季度节点，卡片点击打开笔记。时间轴卡片现已采用透明背景、无边框设计，仅保留左侧状态色条，视觉更轻盈。

### 6. 支持开发者

- 命令面板执行 **Bangumi: 支持开发者 / 打赏**。
- 追番列表标题栏点击 ☕ 按钮。
- 设置 → “☕ 支持” 标签页点击“打赏支持”。
- 赞助链接已在代码中固定，点击后将在浏览器中打开赞助页面。

---

## 📋 模板变量参考

### 笔记文件名模板变量

在设置 → 基本 → 笔记文件路径模板中可使用以下变量：

| 变量 | 含义 | 示例输出 |
| ---- | ---- | -------- |
| `{{type}}` | 条目类型（中文） | 动画 |
| `{{title}}` | 中文名（优先 name_cn） | 葬送的芙莉莲 |
| `{{name}}` | 原名 | 葬送のフリーレン |
| `{{name_cn}}` | 中文名 | 葬送的芙莉莲 |
| `{{id}}` | Bangumi 条目 ID | 393858 |
| `{{date}}` | 播出/发售日期（去除所有连字符） | 20231001 |
| `{{typeId}}` | 条目类型数字 ID | 2 |

> 示例：`{{date}}/{{type}}/{{title}}` 会生成 `20231001/动画/葬送的芙莉莲.md`。

### 附件文件名模板变量

在设置 → 输出与附件 → 附件文件名模板中可使用：

| 变量 | 含义 | 示例输出 |
| ---- | ---- | -------- |
| `{{title}}` | 中文名 | 葬送的芙莉莲 |
| `{{id}}` | Bangumi 条目 ID | 393858 |
| `{{type}}` | 条目类型（中文） | 动画 |

> 例如模板为 `{{title}}`，封面保存为 `assets/葬送的芙莉莲.jpg`。

### 笔记内容模板变量（自定义模板文件）

当启用自定义模板时，模板文件内可使用以下变量（除 Frontmatter 外）：

| 变量 | 含义 |
| ---- | ---- |
| `{{frontmatter}}` | 自动生成的完整 Frontmatter 文本 |
| `{{title}}` | 中文名 |
| `{{name}}` | 原名 |
| `{{name_cn}}` | 中文名 |
| `{{type}}` | 条目类型 |
| `{{platform}}` | 平台 |
| `{{rating}}` | Bangumi 评分 |
| `{{rank}}` | 排名 |
| `{{summary}}` | 简介 |
| `{{date}}` | 播出日期 |
| `{{cover}}` | 封面路径（本地或 URL） |
| `{{url}}` | Bangumi 条目链接 |
| `{{netaba}}` | Netaba 链接 |
| `{{state}}` | 观看/阅读状态 |
| `{{progress}}` | 进度（数值） |
| `{{detail}}` | 详细信息对象（需进一步取值，如 `{{detail.导演}}`） |
| `{{watchUrl}}` | 观看网址（从旧笔记提取，如有） |
| `{{personalSummary}}` | 个人总结（从旧笔记提取，如有） |
| `{{recordDate}}` | 记录日期（YYYYMMDD） |

---

## ⚙️ Frontmatter 字段参考

插件生成的笔记包含以下 YAML 前置元数据（部分字段因条目类型而异）：

| 字段名 | 类型 | 说明 | 适用类型 |
| ------ | ---- | ---- | -------- |
| `条目类型` | String | 如“动画”“书籍” | 全部 |
| `中文名` | String | 作品中文名 | 全部 |
| `原名` | String | 作品原始名称（通常为日文） | 全部 |
| `别名` | Array/String | 作品别名，格式由数组设置决定 | 全部（若有） |
| `封面` | String | 封面图片本地路径或 URL | 全部 |
| `排名` | String/Number | Bangumi 全站排名 | 全部 |
| `平台` | String | 如 TV、Web、PC 等 | 全部 |
| `NSFW` | Boolean | 是否为 R 18 内容 | 全部 |
| `公共标签` | String | Bangumi 公共标签，逗号分隔 | 全部 |
| `卷数` | Number | 书籍卷数 | 书籍 |
| `系列作品` | String | 是否为系列作品（是/否） | 全部 |
| `锁定状态` | String | 条目是否锁定（正常/已锁定） | 全部 |
| `播出/发售日期` | String | 格式 YYYY-MM-DD | 全部 |
| `用户标签` | Array/String | 用户自定义标签 | 全部（若有） |
| `收藏人数` | Number | 标记为“看过”等的人数 | 全部 |
| `想要人数` | Number | 标记为“想看”等的人数 | 全部 |
| `评分人数` | Number | 总评分人数 | 全部 |
| `总集数` | Number | 动画/三次元总集数 | 动画、三次元 |
| `已看集数` | Number | 用户已观看的集数 | 动画、三次元 |
| `观看进度` | Number | 百分比（已看/总集数） | 动画、三次元 |
| `阅读进度` | Number | 百分比或已读册数 | 书籍 |
| `游戏进度` | Number | 百分比或已玩部分 | 游戏 |
| `BGM链接` | String | Bangumi 条目链接 | 全部 |
| `BGM评分` | Number | Bangumi 评分 | 全部 |
| `下载路径` | String | 物理文件夹下载路径（若配置映射） | 可选 |
| `Netaba链接` | String | Netaba 评分趋势图链接 | 动画（若有） |
| `记录日期` | String | 导入/创建日期（YYYYMMDD） | 全部 |
| `tags` | String/Array | 固定包含 `bangumi` | 全部 |
| `completion_status` | String | 预留字段，默认为空 | 全部 |
| **状态字段（按类型）** | | | |
| `阅读状态` | String | 书籍状态：在读/想读/读过/搁置/抛弃 | 书籍 |
| `观看状态` | String | 动画/三次元状态：在看/想看/看过/搁置/抛弃 | 动画、三次元 |
| `收听状态` | String | 音乐状态：在听/想听/听过/搁置/抛弃 | 音乐 |
| `游戏状态` | String | 游戏状态：在玩/想玩/玩过/搁置/抛弃 | 游戏 |
| **追番检测字段（由追番列表自动维护）** | | | |
| `更新状态` | String | “有更新”或“已同步” | 全部 |
| `更新集数` | Number | 上次检测时发现的新增集数/进度 | 全部 |
| `最后检测时间` | String | 最后更新检测时间（ISO 字符串） | 全部 |
| `最新进度` | Number | 从 API/本地/网页获取的最新总进度 | 全部 |

> **别名** 与 **用户标签**（若存在）的数组输出格式可在设置 → 输出与附件 → 数组显示格式中自定义。

---

## 📄 高级用法

### 📋 自定义笔记模板

1. 在设置中启用“自定义模板”并指定模板路径。
2. 模板文件是一个普通的 Obsidian 笔记，可使用 `{{变量}}` 占位符。
3. 可用变量参见上方“笔记内容模板变量”表格。
4. 示例模板片段：

```markdown
---
{{frontmatter}}
---

# {{title}}

- 原名：{{name}}
- 评分：⭐ {{rating}}
- 状态：{{state}}
- 进度：{{progress}} 集

! [cover] ({{cover}})

## 简介
{{summary}}

## 个人总结
{{personalSummary}}
```

### 📁 物理文件夹映射（仅桌面端）

如果希望将下载文件夹创建在 Obsidian 库外的真实硬盘目录，可在设置中配置映射关系：将某个笔记路径前缀映射到一个物理文件夹路径。导入条目时，插件会在物理路径下自动创建与笔记同名的子文件夹（仅桌面端，依赖 Node.js `fs` 模块）。

### 🖼️ 图床上传（实验性）

开启后，封面会通过 PicGo 上传到图床，笔记中写入返回的 URL。需本地运行 PicGo 并正确设置上传地址（设置中的“PicGo 上传地址”）。

---

## ⚙️ 快捷键

在追番列表视图中（需在设置中启用“启用快捷键”）：
- 按 `/` ：聚焦搜索输入框。
- 按 `Esc` ：清空搜索并刷新列表。

---

## 🤝 贡献与反馈

本项目欢迎社区贡献。所有贡献者需签署[贡献者许可协议 (CLA)](./CLA.md)，详见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

如有 Bug 报告或功能建议，请在 [GitHub Issues](https://github.com/yuangwu/obsidian-bangumi/issues) 中提出。

---

## 🙏 支持开发者

如果觉得插件对你有帮助，欢迎**打赏赞助**，让我有更多动力维护和更新。

[Donate.md](https://github.com/yuangwu/obsidian-bangumi/blob/main/yuangwu/Donate.md)

---

## 📜 许可证

本软件采用 **AGPL-3.0 双重许可** 模式：

- **开源版**：在 [GNU Affero General Public License v3.0](./LICENSE) 下免费使用，适用于个人、研究人员和开源项目。
- **商业版**：可向作者[购买商业许可证](./COMMERCIAL_LICENSE.md)，获得专有使用权。

**贡献者须知**：所有贡献者需签署[贡献者许可协议 (CLA)](./CLA.md)。详见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

Copyright © 2026 yuangwu. All rights reserved.

---

## 📜 免责声明

1. 使用本插件前，请备份你的数据，以防意外。
2. 本插件仅调用 Bangumi 官方公开 API，不进行任何内容爬取，不侵犯版权或平台权益。
3. 本程序仅供学习交流使用。
4. 因使用插件造成的任何数据损失，由使用者自行承担。
5. 使用或修改本插件，即视为同意上述免责声明。

---

## 📜 影响说明

除在导入时根据“冲突处理策略”选择“覆盖（保留用户字段）”会覆盖同路径同文件名笔记外，其余操作均不会修改已有笔记。

| 操作 | 条件 | 影响 | 示例 |
| --- | --- | --- | --- |
| 导入条目 | 默认条件 | 新建一条笔记，路径由“文件名模板”决定 | 如模板为 `{{type}}/{{title}}`，导入“葬送的芙莉莲”会创建 `动画/葬送的芙莉莲.md` |
| 导入条目 | 已有同名笔记，且冲突策略为“跳过” | 无任何影响，提示笔记已存在，不会修改 | 同上，若已存在则跳过 |
| 导入条目 | 已有同名笔记，且冲突策略为“覆盖（保留用户字段）” | 覆盖原笔记，但保留原有的“观看网址”、“个人总结”等用户内容 | 旧笔记中的个人总结会被合并到新笔记 |
| 导入条目 | 文件名模板包含多级目录 | 自动创建所需文件夹 | 模板 `{{date}}/{{type}}/{{title}}` 会生成 `20231001/动画/葬送的芙莉莲.md` 目录结构 |
| 封面下载 | 开启“下载封面到本地” | 在“附件存储路径”保存封面文件，文件名由附件模板生成 | 附件模板 `{{title}}`，文件保存为 `assets/葬送的芙莉莲.jpg` |
| 追番标记 | 点击“标记已同步” | 修改笔记 Frontmatter 中的“更新状态”和“更新集数”字段，不会改动正文内容 | 标记后“更新状态”变为“已同步”，提供 3 秒撤销提示 |
| 追番标记 | 点击“取消同步” | 将已同步的条目标记为“有更新”，并将“更新集数”重新计算（基于最新进度与已看进度之差） | 标记后“更新状态”变为“有更新” |
| 批量导入断点续传 | 导入中断后重新启动 Obsidian | 检测到残留状态文件，弹窗询问是否继续导入或清理 | 若选择继续，从断点处恢复导入流程 |

---

## ⚡ 效果展示

![Pasted image 20260804160758.png](https://github.com/yuangwu/obsidian-bangumi/blob/main/image/Pasted%20image%2020260804160758.png)
![Pasted image 20260804160934.png](https://github.com/yuangwu/obsidian-bangumi/blob/main/image/Pasted%20image%2020260804160934.png)
![Pasted image 20260804161024.png](https://github.com/yuangwu/obsidian-bangumi/blob/main/image/Pasted%20image%2020260804161024.png)
![Pasted image 20260804161100.png](https://github.com/yuangwu/obsidian-bangumi/blob/main/image/Pasted%20image%2020260804161100.png)
![Pasted image 20260804160519.png](https://github.com/yuangwu/obsidian-bangumi/blob/main/image/Pasted%20image%2020260804160519.png)

> 结合其他插件可以构建更丰富的工作流：
> - 配合 **Dataview** 创建个人媒体库看板、同类推荐

---

## 🔗 相关文档

- [README.md](./README.md) — 项目介绍（本文件）
- [LICENSE](./LICENSE) — AGPL-3.0 完整协议
- [COMMERCIAL_LICENSE.md](./COMMERCIAL_LICENSE.md) — 商业许可证说明
- [CLA.md](./CLA.md) — 贡献者许可协议
- [CHANGELOG.md](./CHANGELOG.md) — 更新日志
- [CONTRIBUTING.md](./CONTRIBUTING.md) — 贡献指南

---

## 🙏 致谢

> - 感谢 [Bangumi](https://bgm.tv/) 的开源项目 [Bangumi开源项目](https://github.com/bangumi)
> - 感谢[月涟_luvian](https://space.bilibili.com/67571043) 的开源项目 [luvian114/Bangumi-to-obsidian](https://github.com/luvian114/Bangumi-to-obsidian)
> - 感谢[北漠海](https://space.bilibili.com/1065768987) 的开源项目 [beimohai/Bangumi-to-obsidian-lite](https://github.com/beimohai/Bangumi-to-obsidian-lite)
> - 感谢[一般の智人](https://space.bilibili.com/286674433) 的开源项目 [Yasikap/Bangumi-Bridge-Obsidian](https://github.com/Yasikap/Bangumi-Bridge-Obsidian)
> - 感谢[景深很浅](https://space.bilibili.com/17915477) 的开源项目 [Obsidain影音库的模板](https://www.bilibili.com/video/BV1hiE9zAEj4/)

**在 Obsidian 中享受你的 Bangumi 体验！** 🎉