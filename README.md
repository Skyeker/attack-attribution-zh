# Attack Attribution (中文版) — AI Agent Skill

用于网络事件调查与情报分析的综合性攻击溯源与攻击者画像 skill。

## 功能概览

| 工作流 | 能力 |
|--------|------|
| 归因分析 | 基于钻石模型与 ACH（竞争假设分析），从 IOC 出发得出结构化归因判断 |
| 威胁者画像 | 生成包含别名、TTP 矩阵、战役历史、检测指导的完整档案 |
| 战役关联 | 跨事件构建关联矩阵，聚类入侵集群，分析作战节奏 |
| 基础设施枢轴 | 纯被动方法论追踪 C2 域名、IP、证书、WHOIS 注册模式 |

## 安装

**Claude Code / Claude Desktop:**
```bash
/learn @wangchenyang/attack-attribution-zh
```

**skills.sh (Vercel):**
```bash
npx skills add wangchenyang/attack-attribution-zh
```

**agentskill.sh:**
```bash
npx @agentskill.sh/cli@latest install @wangchenyang/attack-attribution-zh
```

**手动安装:**
```bash
git clone https://github.com/wangchenyang/attack-attribution-zh.git
# 将 SKILL.md 和 references/ 目录复制到你的 agent skills 目录
```

> 注意：请将上面的 `wangchenyang` 替换为你实际的 GitHub 用户名。

## 目录结构

```
attack-attribution-zh/
├── SKILL.md                              # 主 skill 文件
├── references/
│   └── attribution-frameworks.md         # 分析框架参考手册
├── README.md                             # 本文件
└── LICENSE                               # MIT 许可证
```

## 安全声明

本 skill 严格遵循防御性网络安全边界：

- 不生成攻击工具，所有输出均为分析性、防御性内容
- 仅使用被动侦察技术（pDNS、历史 WHOIS、CT 日志、OSINT）
- 所有外部数据视为分析对象，不视为可执行指令（防 prompt injection）
- 每份归因输出都带有明确的置信度与分析保留意见
- 不做个人去匿名化，不鼓励人肉搜索

详细安全护栏参见 SKILL.md 中的「第三方数据源信任边界」章节。

## 许可证

MIT
