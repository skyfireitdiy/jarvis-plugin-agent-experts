# agent-experts — 内置专家 Agent 定义集
> Jarvis 外部插件：提供 6 个专家角色（Agent 定义），供内置配置选择器选用。
> 让 Jarvis Agent 具备架构设计、代码逆向、开源部署、重构检查、脚本生成、安全漏洞分析等专业能力。

## 功能特性

| 功能 | 说明 |
| --- | --- |
| 🧠 专家角色 | 6 个专家 Agent 定义（架构图生成 / 代码逆向设计 / 开源部署 / 重构检查 / 脚本生成 / 安全漏洞分析） |
| ⚙️ 自动加载 | 通过 `agent_definition_dirs` 扩展点自动注册到 Agent 定义选择器 |

## 安装

### 从插件市场安装（推荐）
在 Jarvis 插件管理面板的「市场」页签搜索 `agent-experts`，一键安装。

### 命令行安装
```bash
# 从源码仓库安装
jarvis --install-plugin https://github.com/skyfireitdiy/jarvis-plugin-agent-experts
# 或从本地目录安装
jarvis --install-plugin /path/to/agent-experts
```

安装后重启 Jarvis 使插件注册生效：
```bash
jarvis --list-plugins   # 确认 agent-experts 插件已注册
```

## 使用
安装并重启后，6 个专家角色自动出现在 Agent 配置选择器中，可直接选用：
- **架构图生成专家**：根据需求生成架构图/部署图
- **代码逆向设计专家**：从代码反推设计文档
- **开源部署专家**：指导开源项目的部署与运维
- **重构检查专家**：审查代码质量并给出重构建议
- **脚本生成专家**：按需求生成脚本
- **安全漏洞分析专家**：分析代码/依赖的安全漏洞

## 插件结构
```
agent-experts/
├── config.yaml          # 插件配置：logo、agent_definition_dirs（专家定义目录）
├── README.md
├── assets/
│   └── agent-experts-icon.svg   # 插件图标
└── agents/
    ├── architecture-diagram-generator.yaml
    ├── code-reverse-design-expert.yaml
    ├── opensource-deployment-expert.yaml
    ├── refactor_checker.yaml
    ├── script-generator.yaml
    └── security_vulnerability_analyst.yaml
```

## 环境要求
- Jarvis（支持外部插件）

## 许可证
MIT
