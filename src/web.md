# web 模块技术总结

## 模块定位
`web/` 是平台前端控制台，负责知识库管理、检索问答、流程编排、系统配置和用户操作界面。

## 目录概览
- `src/pages/`：页面级模块，如知识库、聊天、流程、系统设置、搜索等。
- `src/components/`：复用组件。
- `src/services/`：接口调用封装。
- `src/hooks/`、`src/utils/`：状态逻辑与工具方法。
- `src/routes.ts`：路由总入口。

## 技术栈
- React 18
- Umi 4
- TypeScript
- Ant Design 与 Pro Components
- TanStack Query、Tailwind CSS、图形与编辑器组件

## 核心能力
- 提供登录、知识库、文档查看、聊天、流程编排与系统管理页面。
- 支持前后端分离开发和 Docker 化交付。
- 提供 Jest 测试、ESLint 与 Prettier 规范约束。

## 工程特点
- 页面划分细，业务边界清晰。
- 通过 `routes.ts` 可看出平台已覆盖知识库、聊天、报表、流程、系统设置等多个入口。
- 适合与 `api/` 并行演进，形成完整管理台。
