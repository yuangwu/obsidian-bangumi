# Bangumi 集成插件 (obsidian-bangumi)

<p align="center">    
  <a href="https://github.com/yuangwu/obsidian-bangumi/releases/latest">    
    <img src="https://img.shields.io/github/manifest-json/v/yuangwu/obsidian-bangumi?color=blue" alt="version">
  </a>    
  <img src="https://img.shields.io/github/release-date/yuangwu/obsidian-bangumi" alt="release date">
  <a href="https://github.com/yuangwu/obsidian-bangumi/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/yuangwu/obsidian-bangumi" alt="license">
  </a>    
  <img src="https://img.shields.io/github/downloads/yuangwu/obsidian-bangumi/total" alt="downloads">
  <a href="https://github.com/yuangwu/obsidian-bangumi/issues">
    <img src="https://img.shields.io/github/issues/yuangwu/obsidian-bangumi" alt="issues">
  </a>
  <br>
  <img src="https://img.shields.io/tokei/lines/github/yuangwu/obsidian-bangumi" alt="lines">
  <a href="https://www.codefactor.io/repository/github/yuangwu/obsidian-bangumi">
    <img src="https://www.codefactor.io/repository/github/yuangwu/obsidian-bangumi/badge" alt="CodeFactor">
  </a>
</p>

这是一款 [Obsidian](https://obsidian.md/) 插件，支持在 Obsidian 中导入 [Bangumi](https://bgm.tv/) 的 **动画、书籍、音乐、游戏、三次元** 条目，并同步你的收藏状态、评分、评论等信息。  
提供智能追番列表、更新检测、进度看板等完整管理功能。

---

关于插件有任何疑问或功能建议，欢迎提 Issues 或参与开发。  
如果觉得好用，欢迎 ⭐Star 支持！

- [异常、问题 & 新的想法](https://github.com/yuangwu/obsidian-bangumi/issues)
- 阅读其它语言的介绍请点击 [English](README.en.md) | 简体中文

## ✨ 功能

- ☑️ 导入动画、书籍、音乐、游戏、三次元条目
- ☑️ 同步个人 Bangumi 收藏（想看/在看/看过等所有列表）
- ☑️ 导入个人评分、评论时间、阅读/观看状态、个人短评
- ☑️ 支持保存封面至本地或图床（PicGo）
- ☑️ 完全自定义笔记文件名模板（支持多级目录 `{{type}}/{{date}}/{{title}}`）
- ☑️ 追番列表集中看板，显示更新状态、进度、评分
- ☑️ 智能更新检测（Bangumi API / 本地文件夹 / 网页抓取）
- ☑️ 进度条可视化，支持批量标记已同步及撤销
- ☑️ 双视图（列表 / 卡片），统计看板可折叠
- ☑️ 支持移动端导入（封面下载仅在桌面端完全支持）
- ☑️ 自定义模板，按条目类型指定不同模板
- ☑️ 侧边栏快捷入口，快捷键支持
- ☑️ 暗色主题完美适配
- ⬜ 支持 AI 大模型分析导入（规划中）

## 效果展示

结合其他插件可以构建更丰富的工作流：
- 配合 **Dataview** 创建个人媒体库看板、同类推荐
- 配合 **Timeline** 插件生成观看时间线
- 配合自定义主题还原 Bangumi 风格页面

![screenshot](screenshot.png)

## 如何使用

### 单条目导入
使用 <kbd>Ctrl</kbd> + <kbd>P</kbd> 打开命令面板，输入 `Bangumi: 单条目导入`，搜索作品名称，支持翻页浏览更多结果。
![single import](img/single_import.gif)

### 批量同步收藏
执行命令 `Bangumi: 全量批量导入` 或 `Bangumi: 分类筛选批量导入`，可选择类型、列表状态，一键同步所有收藏条目。
![batch import](img/batch_import.gif)

### 追番列表
点击侧边栏 📖 图标或执行 `Bangumi: 打开追番列表`，查看所有条目的更新状态、进度，支持筛选、排序、卡片视图等。
![tracking](img/tracking.gif)

## 设置

- **基础路径**：所有笔记的根目录
- **文件名模板**：支持变量 `{{type}}`、`{{title}}`、`{{id}}`、`{{date}}` 等，可自由组合路径
- **用户 ID**：你的 Bangumi 数字 ID
- **Access Token**：用于访问私有收藏（可选）
- **导入模板**：支持自定义笔记内容模板，可按类型指定
- **附件管理**：封面下载路径、文件名模板、高清封面支持
- **追番设置**：检测方式、视图偏好、分页、快捷键等

详细设置请查阅插件内的设置面板。

## 支持的字段

以下为 Bangumi API 返回以及插件自动生成的 Frontmatter 字段（部分字段需要开启对应选项）：

| 字段                 | 动画 | 书籍 | 音乐 | 游戏 | 三次元 | 说明                   |
|--------------------|----|----|----|----|-----|----------------------|
| 条目类型               | ✅  | ✅  | ✅  | ✅  | ✅   | 自动填入类型名称（如“动画”）      |
| 中文名                | ✅  | ✅  | ✅  | ✅  | ✅   | 优先使用 name_cn         |
| 原名                 | ✅  | ✅  | ✅  | ✅  | ✅   | 日语原名或原始名称            |
| 别名                 | ✅  | ✅  | ✅  | ✅  | ✅   | 数组格式，可自定义            |
| 封面                 | ✅  | ✅  | ✅  | ✅  | ✅   | 本地路径或远程 URL          |
| BGM 评分             | ✅  | ✅  | ✅  | ✅  | ✅   | Bangumi 平均评分          |
| 排名                 | ✅  | ✅  | ✅  | ✅  | ✅   | 全站排名                 |
| 平台                 | ✅  | ✅  | ✅  | ✅  | ✅   | 如 TV、PC 等            |
| NSFW               | ✅  | ✅  | ✅  | ✅  | ✅   | true/false           |
| 公共标签               | ✅  | ✅  | ✅  | ✅  | ✅   | 逗号分隔                 |
| 播出/发售日期            | ✅  | ✅  | ✅  | ✅  | ✅   | YYYY-MM-DD 格式        |
| 总集数 / 卷数 / 曲目数     | ✅  | ✅  | ✅  | ✅  | ✅   | 根据类型自动                |
| 已看 / 已读 / 已听 / 已玩进度 | ✅  | ✅  | ✅  | ✅  | ✅   | 进度数字                 |
| 状态                 | ✅  | ✅  | ✅  | ✅  | ✅   | 如“在看”“想读”“在玩”等        |
| 个人评分               | ✅  | ✅  | ✅  | ✅  | ✅   | 你的评分                 |
| 个人短评               | ✅  | ✅  | ✅  | ✅  | ✅   | 你的评论                 |
| 收藏时间               | ✅  | ✅  | ✅  | ✅  | ✅   | 标记日期                 |
| 用户标签               | ✅  | ✅  | ✅  | ✅  | ✅   | 你添加的标签               |
| 分集信息               | ✅  | ➖  | ➖  | ➖  | ✅   | 动画与三次元支持，可保留观看状态     |
| 角色 / 声优            | ✅  | ➖  | ➖  | ➖  | ➖   | 需在导入设置中开启            |
| 制作人员               | ✅  | ➖  | ➖  | ➖  | ➖   | 需开启                  |
| 关联作品               | ✅  | ✅  | ✅  | ✅  | ✅   | 前传、续集、衍生等            |
| 改编类型               | ✅  | ➖  | ➖  | ➖  | ➖   | 动画专属，检测或手动选择         |
| 下载路径               | 可选 | 可选 | 可选 | 可选 | 可选  | 物理文件夹映射后的路径          |
| Netaba 链接           | ✅  | ➖  | ➖  | ➖  | ➖   | 评分趋势图链接              |
| 记录日期               | ✅  | ✅  | ✅  | ✅  | ✅   | 自动生成                 |
| 更新状态 / 更新集数 / 最后检测 | ✅  | ✅  | ✅  | ✅  | ✅   | 追番列表自动写入             |

> 注：部分字段（如角色、制作人员、关联作品、分集信息）可在设置中按需开启，减少请求次数。

## 如何安装

### 从 Obsidian 插件中心（即将上线）
1. 进入 Obsidian 插件中心
2. 搜索 `obsidian-bangumi`
3. 安装并启用

### 手动安装
1. 从 [Releases](https://github.com/yuangwu/obsidian-bangumi/releases) 页面下载 `main.js`, `manifest.json`, `styles.css`
2. 将文件复制到你的 vault 的 `.obsidian/plugins/obsidian-bangumi/` 文件夹（如不存在请新建）
3. 在 Obsidian 插件中心启用该插件

## 如何开发调试

### 开发
1. 进入你的测试 vault 的 `.obsidian/plugins/` 目录
2. `git clone git@github.com:yuangwu/obsidian-bangumi.git`
3. `cd obsidian-bangumi`
4. `npm install`
5. `npm run build` (或 `npm run dev` 启动热重载)
6. 在 Obsidian 中重新加载插件

### 文档
```shell
npm run docs:dev
```

## 支持开发者

如果觉得插件对你有帮助，欢迎请我喝杯咖啡 ☕，让我有更多动力维护和更新。

![support](support.png)

## 交流社群

- QQ 群：xxxxxxxxx
- Discord: [邀请链接](https://discord.gg/xxxx)

## 免责声明

1. 使用本插件前，请备份你的数据，以防意外。
2. 本插件仅调用 Bangumi 官方公开 API，不进行任何内容爬取，不侵犯版权或平台权益。
3. 本程序仅供学习交流使用。
4. 因使用插件造成的任何数据损失，由使用者自行承担。
5. 使用或修改本插件，即视为同意上述免责声明。

## 影响说明

除在“同步收藏”时勾选“替换同名文档”会覆盖同路径同文件名笔记外，其余操作均不会修改已有笔记。

| 操作      | 条件                              | 影响                                          | 示例                                                                                     |
|---------|---------------------------------|---------------------------------------------|----------------------------------------------------------------------------------------|
| 导入条目   | 默认条件                            | 新建一条笔记，路径由“文件名模板”决定                         | 如模板为 `{{type}}/{{title}}`，导入“葬送的芙莉莲”会创建 `动画/葬送的芙莉莲.md`                            |
| 导入条目   | 已有同名笔记                          | 无任何影响，提示笔记已存在，不会修改                          | 同上，若已存在则不会新建                                                                           |
| 导入条目   | 文件名模板包含多级目录（如 `{{date}}/{{type}}/{{title}}`） | 自动创建所需文件夹                                   | 模板 `{{date}}/{{type}}/{{title}}` 会生成 `202310/动画/葬送的芙莉莲.md` 目录结构                     |
| 封面下载   | 开启“下载封面到本地”                    | 在“附件存储路径”保存封面文件，文件名由附件模板生成                   | 附件模板 `{{title}}`，文件保存为 `assets/葬送的芙莉莲.jpg`                                        |
| 同步收藏   | 以上所有                            | 以上所有                                        | 以上所有                                                                                   |
| 同步收藏   | 开启“替换同名文档”                     | 若笔记已存在 **同路径同文件名**，则直接覆盖                      | 模板 `{{type}}/{{title}}`，已存在 `动画/葬送的芙莉莲.md`，同步时该笔记会被最新数据覆盖                        |
| 追番标记   | 点击“标记已同步”                       | 修改笔记 Frontmatter 中的“更新状态”和“更新集数”字段，不会改动正文内容 | 标记后“更新状态”变为“已同步”，提供 3 秒撤销提示                                                         |

---

**Enjoy your Bangumi experience in Obsidian!** 🎉
