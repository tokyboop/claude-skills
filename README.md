# claude-skills

> ⚠️ **Archived (2026-04-24)**：私人工作流已分叉到 `PrivateSet/claude/skills/`（含 context-backup / brainstorm / calibrate / fp / self-review / req-score / peek-siblings / eval-runner 等 8 个现役 skill，junction 挂载 `~/.claude/skills/`）。
>
> 此公开仓不再维护外发 skill：
> - `skill-vetter`（第三方代码安全审查）保留作独立参考
> - `bubble-sync` 已被 PrivateSet 里的 `context-backup` 取代（功能重叠，context-backup 是现役主力）

我的 Claude Code 自定义技能库。

## 安装方法

把对应目录复制到 Claude Code 的 skills 文件夹：

```
%APPDATA%\Claude\...\skills\<skill-name>\
```

或直接使用 `.skill` 打包文件通过 skill-creator 安装。

重启 Claude Code 后生效。

---

## 技能列表

### 🛡️ skill-vetter

**第三方代码安全审查**

在安装任何第三方脚本、插件或工具前，自动扫描六类安全威胁并输出标准格式报告。

**触发词**：`安装`、`install`、`运行这个脚本`、`这个安全吗`、直接粘贴来源不明的代码

**检查项**：
- 🔴 反弹 Shell / RCE
- 🔑 凭证 / API Key 窃取
- 🌀 代码混淆 / 隐藏 Payload
- 🌐 可疑网络请求
- 📁 文件系统越权
- ⛓️ 供应链投毒特征

**背景**：2026 年 2 月 ClawHavoc 事件后创建，ClawHub 上约 20% 技能为恶意软件。

---

### 🫧 bubble-sync

**对话精华提炼与同步**

说"泡泡 总结同步"，自动回顾当前对话，提炼有价值内容，分类为 memory / skill / wiki，严格脱敏后写入本地并推送 GitHub。

**触发词**：`泡泡 总结同步`、`bubble sync`、`同步今天的内容`

**提炼类型**：工作流、踩坑经验、业务规则、工具用法、决策结论

---

*持续更新中。每个技能目录内有完整的 SKILL.md 说明。*
