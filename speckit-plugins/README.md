# Spec Kit Plugin for Claude Code

<div align="center">
    <h3><em>规范驱动开发工具包 - Claude Code 插件版</em></h3>
</div>

## 📖 简介

Spec Kit 是一个开源的规范驱动开发（Spec-Driven Development）工具包，现已打包为 Claude Code 插件。通过一系列结构化的斜杠命令，帮助你从需求定义到代码实现的完整开发流程。

## ✨ 功能特性

- **🎯 规范驱动** - 先定义"做什么"，再决定"怎么做"
- **📋 结构化流程** - 从需求到实现的完整工作流
- **🔧 多平台支持** - 同时支持 Linux/macOS (bash) 和 Windows (PowerShell)
- **📝 模板系统** - 内置多种文档模板，确保输出一致性
- **🤖 AI 原生** - 专为 AI 代理设计的开发流程

## 🚀 安装方法

### 方式 1：本地加载

```bash
# 克隆或下载此插件目录
cd /path/to/speckit-plugins

# 使用 --plugin-dir 标志加载插件
claude --plugin-dir /path/to/speckit-plugins
```

### 方式 2：从仓库加载

```bash
# 克隆包含插件的仓库
git clone https://github.com/github/spec-kit.git
cd spec-kit

# 加载插件
claude --plugin-dir ./speckit-plugins
```

## 📚 可用命令

插件提供以下斜杠命令（命名空间：`speckit:`）：

### 核心命令

| 命令 | 描述 |
|------|------|
| `/speckit:constitution` | 创建或更新项目治理原则和开发指南 |
| `/speckit:specify` | 定义需求和用户故事 |
| `/speckit:plan` | 创建技术实现计划 |
| `/speckit:tasks` | 生成可执行的任务列表 |
| `/speckit:implement` | 执行所有任务并构建功能 |

### 可选命令

| 命令 | 描述 |
|------|------|
| `/speckit:clarify` | 澄清不明确的需求 |
| `/speckit:analyze` | 跨工件一致性和覆盖率分析 |
| `/speckit:checklist` | 生成质量检查清单 |
| `/speckit:taskstoissues` | 将任务转换为 GitHub Issues |

## 💡 使用示例

### 基本工作流程

```bash
# 1. 建立项目原则
/speckit:constitution 创建注重代码质量、测试标准和用户体验的原则

# 2. 定义需求
/speckit:specify 构建一个照片管理应用，支持按日期组织相册...

# 3. 创建技术方案
/speckit:plan 使用 React + TypeScript，后端使用 Node.js...

# 4. 生成任务列表
/speckit:tasks

# 5. 执行实现
/speckit:implement
```

### 高级用法

```bash
# 在创建方案前澄清需求
/speckit:clarify

# 在实现前分析一致性
/speckit:analyze

# 生成质量检查清单
/speckit:checklist
```

## 📦 插件结构

```
speckit-plugins/
├── .claude-plugin/
│   └── plugin.json              # 插件清单
├── commands/                    # 斜杠命令定义
│   ├── analyze.md
│   ├── checklist.md
│   ├── clarify.md
│   ├── constitution.md
│   ├── implement.md
│   ├── plan.md
│   ├── specify.md
│   ├── tasks.md
│   └── taskstoissues.md
├── memory/                      # 记忆文件
│   └── constitution.md
├── scripts/                     # 辅助脚本
│   ├── bash/                   # Linux/macOS 脚本
│   └── powershell/             # Windows 脚本
└── templates/                   # 文档模板
    ├── agent-file-template.md
    ├── checklist-template.md
    ├── plan-template.md
    ├── spec-template.md
    ├── tasks-template.md
    └── vscode-settings.json
```

## 🔧 依赖说明

### 必需依赖

- **Claude Code** - AI 代理运行环境
- **Git** - 版本控制（用于分支管理）
- **Bash** (Linux/macOS) 或 **PowerShell** (Windows) - 脚本执行环境

### 可选依赖

- **GitHub CLI (gh)** - 用于 `/speckit:taskstoissues` 命令
- **Python 3.11+** - 某些高级功能可能需要

## 📋 工作流程说明

Spec Kit 遵循以下开发流程：

1. **建立原则** (`/speckit:constitution`) - 定义项目的治理原则
2. **定义需求** (`/speckit:specify`) - 描述要构建什么
3. **澄清细节** (`/speckit:clarify`) - 可选：澄清模糊的需求
4. **创建方案** (`/speckit:plan`) - 决定技术栈和架构
5. **生成任务** (`/speckit:tasks`) - 分解为可执行任务
6. **分析验证** (`/speckit:analyze`) - 可选：验证一致性
7. **执行实现** (`/speckit:implement`) - 构建功能

## 🎯 适用场景

- **0-to-1 开发** - 从零开始构建新项目
- **功能迭代** - 为现有项目添加新功能
- **技术探索** - 尝试不同的技术方案
- **团队协作** - 统一开发流程和标准

## 📝 版本信息

- **当前版本**: 1.0.0
- **插件名称**: speckit
- **命名空间**: `speckit:`

## 👥 贡献者

- **维护者**:
  - Den Delimarsky ([@localden](https://github.com/localden))
  - John Lam ([@jflam](https://github.com/jflam))
- **组织**: GitHub

## 📄 许可证

本项目采用 MIT 开源许可证。详见 [LICENSE](../LICENSE) 文件。

## 🔗 相关链接

- [Spec Kit 主仓库](https://github.com/github/spec-kit)
- [完整文档](https://github.github.io/spec-kit/)
- [问题反馈](https://github.com/github/spec-kit/issues)

## 💬 支持

如有问题或建议，请在 [GitHub Issues](https://github.com/github/spec-kit/issues) 中提出。

---

<div align="center">
    <p><strong>让 AI 帮你构建更好的软件</strong></p>
</div>
