# 来源、许可证与修改说明

发布者：xunova739。发布日期：2026-10-02。此发布是在现有技能上进行的本地改编与组合，不代表上游项目背书。

## OpenDesign 和 frontend-design

- 来源：[manalkaff/opendesign](https://github.com/manalkaff/opendesign/tree/cecd9bb6b59408cb96a3974449b8e6ef9f5b17bb)。核查固定提交：`cecd9bb6b59408cb96a3974449b8e6ef9f5b17bb`。
- 原版权：Copyright (c) 2026 manalkaff；MIT。许可保留在 `skills/opendesign/LICENSE` 与 `skills/frontend-design/LICENSE`。
- 本地旧版的两个 SKILL.md 与 viewer 已核对来源；本包 viewer 保留上游内容。
- 修改：创建流程按页面目的分流；已有界面也是设计依据；必要澄清取代固定问卷；明确精修与品牌替换边界；负责人接回独立审核结果并复验；详细交付协议下沉到 references；公开版补可选 helper 缺失时的直接执行路径。

## Taste Skill

- 来源：[Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill/blob/3c7017d636c3a4aad378433ea6d0cfa6c921da4a/skills/taste-skill/SKILL.md)。核查提交：`3c7017d636c3a4aad378433ea6d0cfa6c921da4a`。
- 原版权：Copyright (c) 2026 Leonxlnx；MIT。许可保留在 `skills/design-taste-frontend/LICENSE`。
- 修改：短入口与按需参考；去除普适审美禁令、自动装包、强制双主题和强制造图；纠正字号单位；用实际证据取代推测达标。详细映射见该技能的 `references/upstream-notes.md`。

## Impeccable

- 参考来源：[pbakaus/impeccable](https://github.com/pbakaus/impeccable/tree/508d7e8955de3b3caf2d8676e85206723d41a887/.agents/skills/impeccable)，4.5.0；Apache-2.0，许可保留在 `skills/opendesign/references/LICENSE-impeccable.txt`。
- 使用页面目的分类、精修边界、针对实际问题的改进和验收原则，形成原创短规则。没有打包其二进制、检测器、hooks、完整 playbook 或第三方原生平台指南。
- 上游 NOTICE 中的 iOS/Android 第三方指南不在本包复制范围内。

## UI/UX Review 与 Vercel 检查参考

- `ui-ux-review` 是发布者现有审核流程的整理版本：围绕用户主任务，区分代码、截图和运行态证据，保留整改复测与能力缺失时的替代路径。
- Web 检查参考来自 [vercel-labs/web-interface-guidelines](https://github.com/vercel-labs/web-interface-guidelines/blob/e3d624baaf29dc1fc645aff3e38f03e564d2d6b1/command.md)。原版权：Copyright (c) 2025 Vercel Labs；MIT，许可见 `skills/ui-ux-review/references/LICENSE-vercel.txt`。
- 筛选并改写了适用性、中文内容、原生控件、表单恢复和性能证据等条目；未复制许可未核明的 agent-skills 抓取包装。
- 对比度事实参考 W3C 的官方解释，保留对应来源链接；不把本技能描述为完整 WCAG 合规认证工具。

## Anthropic

核查过官方 frontend-design 用于原则对照。本公开包不包含 Anthropic 插件正文；本包的 `frontend-design` 来源是 OpenDesign，不应标注为 Anthropic 官方技能。

除上述上游许可覆盖的部分，未对发布者原创审核规则和包装文档另行声明一份覆盖整个仓库的统一开源许可。公开仓库供本次授权的接收 agent 拉取使用，第三方内容继续遵循各自许可。
