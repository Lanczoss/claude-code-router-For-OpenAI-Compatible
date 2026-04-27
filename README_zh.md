<p align="center">
  <img src="docs/static/img/ccr-banner.svg" width="100%" alt="Claude Code Router Banner">
</p>

<h1 align="center">Claude Code Router (CCR)</h1>

<p align="center">
  <strong>连接 Anthropic Claude Code 与 OpenAI 生态系统的极致桥梁。</strong>
</p>

<p align="center">
  <a href="README.md">English</a> |
  <a href="LICENSE"><img src="https://img.shields.io/github/license/Lanczoss/claude-code-router-For-OpenAI-Compatible" alt="License"></a>
</p>

---

Claude Code Router (CCR) 是一个功能强大、高性能的反向代理与管理套件，旨在将 [Claude Code](https://docs.anthropic.com/en/docs/claude-code/quickstart) 从单一的模型锁定中解放出来。它允许你将请求路由到任何兼容 OpenAI 接口的 API，让你完全掌控成本、模型选择和隐私。

> [!IMPORTANT]
> **版本支持**: CCR 已针对 **Claude Code CLI v2.1.115 及以上版本** 进行了深度优化。

## ✨ 为什么选择 CCR?

| 特性 | 原版 Claude Code | 使用 CCR 🚀 |
| :--- | :--- | :--- |
| **模型选择** | 仅限 Anthropic Sonnet | **任何** OpenAI 兼容模型 (DeepSeek, GPT-4o, Llama 等) |
| **成本控制** | 固定 Anthropic 计费 | 使用更便宜的渠道、本地模型或免费额度 |
| **透明度** | 黑盒请求 | 全实时的请求监控与日志审计 |
| **灵活性** | 静态配置 | 动态模型切换与自定义 Transformer 插件 |
| **思维链支持** | 标准输出 | 完美支持兼容模型的 **Thinking/Reasoning** 思维链回传 |

## 🏗️ 三位一体架构

CCR 由三个核心组件构建：

1.  **Router 引擎 (核心)**: 一个智能代理，拦截 Anthropic 风格的请求并将其转换为标准的 OpenAI 载荷，处理复杂的工具调用 (Tool Use)、流式传输和图像处理。
2.  **CLI 命令行 (`ccr`)**: 强大的终端工具，用于管理服务、安装预设 (Presets)，并通过一个命令无缝启动 Claude Code。
3.  **Dashboard (Web UI)**: 精美的本地 Web 界面，用于配置供应商、管理 API Key 以及实时监控请求历史。

## 🚀 快速上手

### 1. 安装

```shell
# 安装 Claude Code (如果尚未安装)
npm install -g @anthropic-ai/claude-code

# 安装 Claude Code Router
npm install -g @musistudio/claude-code-router
```

### 2. 启动与配置

启动 CCR 服务并进入仪表盘：

```shell
ccr start
```

在浏览器中打开 `http://localhost:3000`（默认），添加你的第一个供应商（例如 DeepSeek, OpenRouter 或 SiliconFlow）。

### 3. 开始编程

CCR 提供了一个包装命令，会自动为你配置好环境变量：

```shell
ccr code
```

## 🛠️ 高级特性

### 动态路由
为不同的任务配置不同的模型。在 Claude Code 中使用 `/model` 命令即可实时切换后端模型。

### Transformer 系统
针对不同供应商的特殊性提供自定义逻辑。无论是强制开启思维链，还是调整最大 Token 数，CCR 的 Transformer 系统都能确保完美兼容。

### 社区预设 (Presets)
不想手动配置？直接安装社区优化好的预设方案：
```shell
ccr install deepseek-v3
```

## 🌐 支持的供应商

CCR 兼容任何 OpenAI 格式的端点，包括但不限于：
- **OpenRouter** (全模型聚合器)
- **DeepSeek** (高性能、低成本)
- **SiliconFlow (硅基流动) / 火山引擎 / 通义千问**
- **本地模型** (Ollama, vLLM, LM Studio)
- **Groq / Cerebras** (极致推理速度)

---

<p align="center">
  为 AI 开发者社区精心打造。
</p>
