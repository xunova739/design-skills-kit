# Design Skills Kit

面向 AI 编程 agent 的四个设计技能：从页面目的与品牌出发，完成制作、预览、审核和复验。此仓库是本地改编版的公开发布，不是 OpenDesign、Taste、Anthropic、Impeccable 或 Vercel 的官方版本。

## 包含什么

| 目录 | 职责 |
|---|---|
| `skills/opendesign` | 创建流程总入口：读取上下文、按场景选择执行方式、组织产物、接回审核结果 |
| `skills/frontend-design` | OpenDesign 的无品牌视觉探索助手：排版、配色、构图和中文可读性 |
| `skills/design-taste-frontend` | 营销页、作品集和视觉改版；短入口加按需参考，尊重品牌与现有依赖 |
| `skills/ui-ux-review` | 审核入口：真实任务、状态、键盘、响应式及实现检查，区分代码/截图/运行证据 |

## 给另一个 agent 的拉取说明

```bash
git clone --depth 1 --branch v1.0.0 https://github.com/xunova739/design-skills-kit.git
cd design-skills-kit
```

也可以下载 GitHub Release 中的 ZIP。优先固定发布标签；不要把未来的主分支变化当成已经验证的同一版本。

安装时复制 `skills/` 下的四个完整目录（包括 references、ALIASES、LICENSE、viewer 等），不要只复制 `SKILL.md`。目标路径由接收端 agent 的实际环境决定；不要照搬发布者电脑的路径。

可把下面这段交给接收端 agent：

> 拉取 https://github.com/xunova739/design-skills-kit 的 v1.0.0，先读 README 和 NOTICE，校验 SHA256SUMS。查明当前环境实际支持的技能目录，把 skills/ 下的 opendesign、frontend-design、design-taste-frontend、ui-ux-review 四个完整文件夹安装进去。同名目录如已存在，先比较并备份，合并或替换时保留原有定制；不要直接覆盖不相关文件。不要安装可选插件、hook、浏览器扩展或额外运行依赖。安装后核对文件、相对引用和技能发现状态，并说明哪些可选工具当前不可用。

文件校验（二选一，使用系统已有命令）：

```bash
sha256sum -c SHA256SUMS
# macOS 也可使用：shasum -a 256 -c SHA256SUMS
```

## 怎么使用

- 创建 HTML 页面、原型或大幅视觉改版：从 `opendesign` 开始。
- 营销页与作品集：由创建入口选择 `design-taste-frontend`，按任务加载参考。
- 无既有品牌的视觉探索：可选择本包 `frontend-design`。
- 只审核现有页面/流程：从 `ui-ux-review` 开始；明确允许整改时才修改。

同一页面选择一个主要审美执行技能；不要把多个字体、配色和布局偏好同时当作硬性要求。页面的用户任务、真实内容和品牌约束优先。

## 可选能力与缺失时的处理

本包只包含上述四个 skill。它不是浏览器、模型或前端框架，也没有内置业务组件库。

`setup-opendesign`、`run-opendesign`、`interactive-prototype`、`make-a-deck`、`wireframe`、`critique`、`visual-verdict`、Anthropic 的 `example-skills:frontend-design`、`example-skills:webapp-testing`、Product Design 和 React Bits 等别名目标均为可选能力，未随包提供。

- 缺少 setup：将 `skills/opendesign/viewer.html` 复制为项目的 `opendesign/index.html`，按 delivery 参考建立目录和 manifest。
- 缺少预览 helper：使用已安装的本地 HTTP 运行时，绑定 loopback，并检查服务确实指向当前项目；不要为此自动下载软件。
- 缺少创建专家：依据主入口在现有技术栈中直接完成请求的 HTML 产物。
- 缺少审核专家：使用 UI/UX Review 的自带检查表和实际可用工具取证。
- 没有浏览器/真实交互证据：交付代码预审或带明确未验证项的草稿，不能声称功能已经验收。

所有别名的边界见各 skill 的 `ALIASES.md`。本包 `frontend-design` 与 Anthropic 的同名插件是不同入口。

## 版本与验证边界

`v1.0.0`，2026-10-02。技能正文来自本轮已落地改编版本；公开分发补齐上游许可、来源及缺失可选 helper 的处理说明。

本轮本地评测覆盖中文营销页、后台精修、表单代码审查；旧/新版本各通过 15/15 项约束检查。还检查了桌面和窄屏、Tab 路径、筛选恢复、表格横滚、弹窗关闭和焦点恢复。两版均通过只能支持已测能力未见回退，不能证明视觉优胜或“90% 更好看”。

这些是单次、非完全盲测的有限样例；未验证自动触发准确率、跨模型稳定性、真实触摸设备、读屏器、生产接口或线上性能。本公开仓库仅发布技能和必要文档，不包含本机记录、私人环境、测试会话或凭据。

## 许可与归属

本仓库包含不同来源的改编内容，**没有一份覆盖所有上游内容的自有统一许可**。各来源许可及改写说明见 [NOTICE.md](NOTICE.md) 和相应文件夹内的 LICENSE。继续复制或发布时保留适用的版权和许可声明。
