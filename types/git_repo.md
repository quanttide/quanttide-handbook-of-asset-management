# Git仓库

Git仓库指的是项目代码托管的版本控制仓库。

以标准资产体系为准，GitHub优先，围绕GitHub建立生态。


## 保留文件

保留文件指的是具有特定业务意义的文件。

标准保留文件包括：
- `README.md`: 项目简介。关于当下的语义记忆。
- `CHANGELOG.md`: 版本历史记录，遵循 [Keep a Changelog](https://keepachangelog.com/) 规范。关于过去的事件记忆。
- `ROADMAP.md`: 项目路线图。关于未来的事件记忆。
- `CONTRIBUTING.md`: 贡献指南。程序性记忆。
- `AGENTS.md`: 智能体README。智能体的元认知记忆。

### README.md

项目概述，包含：
- 项目简介（一句话）
- 目录结构
- 快速开始

### CONTRIBUTING.md

详细工作流文档，包含：
- 项目结构说明
- 开发环境配置
- 提交规范
- 发布流程
- 环境变量维护规则
- 人机协作原则

### AGENTS.md

Agent导航文档，简洁（约50行），包含相关文档表格、快速索引、协作原则、重要提示。

**内容结构**：
- 相关文档表格
- 快速索引表格
- 协作原则（3条）
- 重要提示（5条）
- 如何维护AGENTS.md

**完整示例**：

```markdown
# AGENTS.md

本仓库维护量潮科技工程标准资产。

## 规范文档

| 规范 | 路径 | 用途 |
|------|------|------|
| 文档格式标准 | docs/format.md | Markdown写作规范 |
| 版本发布标准 | devops/release.md | 版本发布流程 |

## 快速索引

| 任务 | 查看文档 |
|------|---------|
| 编写文档 | docs/format.md |
| 发布版本 | devops/release.md |

## 协作原则

- 最小干预：仅用户明确请求时操作
- 原子提交：每次提交独立完整
- 遵循规范：参照规范文档执行
```

**维护规则**：
- 新增文档、新增任务类型时更新
- 不重复README/CONTRIBUTING已有的内容
- 详细说明写在CONTRIBUTING，导航索引写在AGENTS.md

### CHANGELOG.md

版本变更记录，格式：

```markdown
# Changelog

## [版本号] - 日期

### Added
### Changed
### Fixed
### Removed
```


## 保留目录

保留目录指的是具有特定业务意义的目录。

标准保留目录包括：
- `.agents/`: 智能体配置目录
- `.quanttide/`: 量潮配置目录

### 智能体配置

- `skills/`: 技能目录。每个技能装在一个次级目录里，即`.agents/skills/<skill-name>`。次级目录固定包括一个`SKILL.md`和AgentSkills规范定义的其他文件。

### 量潮配置

- `asset/`: 数字资产。包括`contract.yaml`数字资产契约等。
- `code/`: 氛围编程。包括`contract.yaml`氛围编程契约等。
- `docs/`: 文档工程。包括`contract.yaml`文档工程契约等。
