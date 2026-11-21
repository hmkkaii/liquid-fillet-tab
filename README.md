# 液态内凹圆角标签页 · 开箱即玩源码与 1 分钟免费部署指南

欢迎体验这套**纯原生 HTML + 单条闭合 SVG 动态路径 + 二阶阻尼弹簧**实现的液态浏览器标签页微交互实验室！无需安装 Node.js 或任何前端依赖，零代码基础的设计师也能 **1 秒双击把玩、30 秒魔改手感、1 分钟免费上线生成公开网页链接**。

---

## 一、 包内文件说明

- **`index.html`**：完整单文件可交互源码（开头 **第 9～59 行** 已专门留出中文注释的 `USER_CONFIG` 新手调参区）。
- **`01_新手必看_怎么玩与1分钟免费部署指南.pdf`**：本指南的图文精排 PDF 版。
- **`02_底层原理_4步手搓公式与Prompt手册.pdf`**：底层数学公式拆解与 Vibe Coding 一键复刻提示词。
- **`README.md`**：上传到 GitHub 仓库时会自动渲染为项目说明主页。

---

## 二、 怎么玩这个项目？（2 种上手姿势）

### 玩法 1｜1 秒本地直接运行（零环境配置）
1. 解压压缩包后，直接**双击 `index.html`**（用 Chrome、Edge 或 Safari 浏览器打开即可）。
2. **鼠标自由交互**：
   - 按住任意标签（如 `General`）**向上拖离**，观察底部两侧 `16px` 液态反向圆角如何像水滴一样收缩闭合为悬浮胶囊；
   - 按住标签**左右划过隔壁标签中线**，体验真实二阶阻尼弹簧丝滑让位换槽；
   - 点击左下角 **`Debug overlay`** 荧光绿拨杆，实时透视翡翠绿 `R_in` 与珊瑚红 `R_out` 相切辅助圆。
3. **内置效率快捷键**：
   - 按 **`D` 键**：一键开关 `Debug` 几何透视层
   - 按 **`S` 键**：一键开关 `0.2x` 慢动作显微镜（物理帧步长放慢 5 倍）
   - 按 **`H` 键**：一键隐藏顶部黑框进入沉浸录屏画幅（按 `Esc` 恢复）

### 玩法 2｜30 秒 DIY 魔改物理手感
用 **VS Code / Cursor / 系统自带「文本编辑」或「记事本」** 打开 `index.html`，开头 **第 12 行** 就是 `window.USER_CONFIG`，改完数字保存（`Cmd+S` / `Ctrl+S`）刷新浏览器立刻生效！推荐试试这 3 组超好玩的预设配方：

| 预设风格 | 修改 `USER_CONFIG` 参数 | 视觉与物理手感变化 |
| :--- | :--- | :--- |
| **果冻 Q 弹震荡模式** | `SPRING_STIFFNESS: 420`<br>`SPRING_DAMPING: 11`<br>`MAX_TILT_DEG: 9` | 松手落回槽位与邻居换位时会产生明显的果冻回弹余震，空中摇摆幅度更大 |
| **大圆角水银拉丝模式** | `MAX_FILLET_R: 26`<br>`MAX_BOTTOM_R: 22`<br>`PEEL_DIST: 44` | 贴合态底部两侧铺开 `26px` 超宽液态裙边，剥离过程拉丝感极强 |
| **个人作品集导航栏模式** | 修改 `TABS` 数组里的 `title` 为 `'Portfolio' / 'Works' / 'About'` | 秒变你个人网站的专属液态顶部导航栏原型，可直接录屏放进作品集 |

---

## 三、 1 分钟免费部署成公开网页链接（3 种零成本方案）

想把这个可拖拽的交互 Demo 变成一个 `https://...` 在线链接，直接嵌进你的 **Notion 作品集、Figma 原型或个人简历**？下面 3 种方案任选其一，全程 0 元：

### 方法 A｜拖拽 10 秒上线（零代码推荐：Netlify Drop / EdgeOne Pages）
适合不想注册代码仓库、希望 10 秒钟立刻拿到在线链接的朋友：
1. 浏览器打开 **`https://app.netlify.com/drop`**（免费登录账号；国内也可搜 **EdgeOne Pages 静态托管**）。
2. 直接把解压后的**整个源码包文件夹**（确保里面有 `index.html`）用鼠标拖进网页中央的虚线上传框。
3. 等待约 5～10 秒，页面会自动生成一个 `https://xxx.netlify.app` 公开网址！点击 `Domain settings` 还能免费改成你喜欢的英文名前缀（如 `https://yourname-liquid-tab.netlify.app`）。

### 方法 B｜GitHub Pages 永久免费托管（适合长期放简历）
1. 登录 `github.com`，点击右上角 **`+` → `New repository`**：
   - `Repository name` 填 `liquid-tabs-demo`
   - 勾选 **`Public`（公开）**，点击绿色按钮 **`Create repository`**。
2. 在新建好的仓库页面，点击 **`uploading an existing file`**（或 `Add file` → `Upload files`）。
3. 把文件夹里的 `index.html` 和 `README.md` 拖进去，点击底部绿色按钮 **`Commit changes`**。
4. 点击仓库顶部菜单栏的 **`Settings`** → 左侧栏找到 **`Pages`**：
   - 在 `Build and deployment` 下，`Branch` 下拉框选择 **`main`**，点击右侧 **`Save`**。
5. 等待约 45 秒刷新页面，顶部就会出现永久在线链接：`https://你的GitHub用户名.github.io/liquid-tabs-demo/`！

### 方法 C｜Vercel 一键绑定加速（自动同步更新）
1. 先按「方法 B」前 3 步把文件传到 GitHub 仓库。
2. 打开 `vercel.com` 用 GitHub 账号一键登录，点击 **`Add New...` → `Project`**。
3. 找到刚才的 `liquid-tabs-demo` 仓库点击 **`Import`**，什么配置都不用改，直接点 **`Deploy`**。
4. 15 秒即可生成全球边缘节点加速的在线链接；以后你在 GitHub 里改任何 `USER_CONFIG` 数字，线上网页会自动同步更新！

---

## 四、 进阶玩法：用 AI 把液态标签栏移植进你的个人网站

如果你想在 Cursor / Claude / Antigravity 里把这套液态标签页直接改造成你个人作品集网站的真实导航栏，把 `index.html` 拖进对话框并发送下面这段提示词即可：

```markdown
请参考我上传的 index.html 中的「单条闭合 SVG <path> 液态内凹圆角 + Spring(380, 28) 二阶弹簧」实现逻辑，帮我把它封装成一个可复用的顶部导航栏组件，接入我的个人作品集页面：
1. 导航项改为：Works（作品集）、Playground（交互实验）、Notes（设计思考）、About（关于我）；
2. 点击或拖拽切换标签时，下方白色点阵内容区平滑切换对应栏目的卡片内容；
3. 保留贴合态 16px 反向内凹圆角零灰缝细节，并在右下角保留一个精致的小开关供访客开启 Debug 几何透视彩蛋。
```

---
*整理出品：@设计招财头 · UI 细节放大镜系列*
