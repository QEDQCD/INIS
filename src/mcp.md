# mcp 模块技术总结

## 模块定位
`mcp/` 用于把平台能力封装成 MCP 服务，便于外部智能体或客户端以统一协议访问检索能力。

## 目录概览
- `server/`：MCP SSE 服务端实现。
- `client/`：MCP 客户端示例。

## 核心能力
- 暴露 `ragforge_retrieval` 工具。
- 将平台知识库列表和检索接口映射为 MCP Tool。
- 支持自托管模式与 Host 模式两种 API Key 传递方式。

## 关键实现点
- 服务端使用 Starlette、SSE 和 MCP 低层 Server。
- 通过 `RAGForgeConnector` 适配平台 `/api/v1` 接口。
- 客户端示例演示了如何初始化会话、列出工具并发起调用。

## 适用场景
- 将平台能力接入外部 Agent 框架。
- 以工具方式向通用客户端暴露知识库检索。
- 统一协议化接入，减少重复封装成本。
