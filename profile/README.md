# 猎手云 LieShouCloud

**一套代码库，装配出任何行业、任何形态的企业数字化平台。**

<p align="center">
  <img src="https://img.shields.io/badge/Java-21-orange" alt="Java 21"/>
  <img src="https://img.shields.io/badge/Spring%20Boot-3.5-blue" alt="Spring Boot 3.5"/>
  <img src="https://img.shields.io/badge/Spring%20Cloud-2023.0-purple" alt="Spring Cloud 2023.0"/>
  <img src="https://img.shields.io/badge/React-19-61dafb" alt="React 19"/>
  <img src="https://img.shields.io/badge/PostgreSQL%20%26%20MySQL-green" alt="PG & MySQL"/>
  <img src="https://img.shields.io/badge/License-Apache--2.0-brightgreen" alt="Apache-2.0"/>
</p>

企业数字化软件的真实痛点是：**不同行业、不同规模、不同交付要求**，导致每个客户都要重写一遍。
猎手云用「**能力域 + 四维正交装配**」把这个变量收敛掉：

```
产品（行业方案） = core 底座 + 能力域组合（crm / erp / mes / iot / legal / edu …）
交付形态        = 单体 / 微服务       （配置驱动，零重写演进）
数据库          = MySQL / PostgreSQL  （代码只写 JPA，纯配置切换）
部署位置        = 云端 / 客户机房私有化（私有化自动挂载 License / 离线升级）
```

## 🔓 我们开源什么

| 层 | 内容 |
| --- | --- |
| 工程底座 | `framework` / `shared` / `platform` / `midplatform` 模块 |
| 行业能力域 | `industry-legal` / `industry-edu` / `industry-mfg` 等**产品能力**（不含客户内容） |
| 契约层 | **OpenAPI 单一真相源** + 由它生成的前端 API/类型 |
| 前端共享层 | `core` / `ui-web` / `i18n` / `web-kit` + 多端骨架 |

## 🔒 我们不开源什么

- **客户专属层**（一客户一仓）：客户业务代码、客户前端 overlay
- **客户交付包**：只引 Nexus 制品 + 发布冻结的上游版本
- **私有化配置与 License 机制**

> 上游有一条硬门禁：**客户专属内容禁入上游**。开源仓只放上游。

## 📦 仓库索引

**当前主线（前后端各一个单仓，契约先行 · 共享层 · 多端）**

| 单仓 | 内容 |
| --- | --- |
| `lieshou-backend` | `modules/{framework,shared,platform,midplatform,industry}` · `apps/svc-*` · `contracts/openapi.yaml` |
| `lieshou-frontend` | `packages/{contract,core,ui-web,edition,i18n,web-kit,config}` · `apps/{web,mobile,desktop,mini-program,harmony}` |

*主线单仓在内部 GitLab 开发中，公开进度以本组织仓库为准。*

**上一代多仓结构（本组织已公开，标记为 `【旧多仓】`）**

| 层 | 仓库 |
| --- | --- |
| 总入口 | [LieShouCloud](https://github.com/HUNTERCAT-DIGITAL/LieShouCloud) |
| 后端底座 | [lieshou-framework](https://github.com/HUNTERCAT-DIGITAL/lieshou-framework) |
| 装配形态 | [lieshou-standalone](https://github.com/HUNTERCAT-DIGITAL/lieshou-standalone)（单体） · [lieshou-cloud](https://github.com/HUNTERCAT-DIGITAL/lieshou-cloud)（微服务） |
| 微服务模块 | [auth](https://github.com/HUNTERCAT-DIGITAL/lieshou-cloud-auth-services) · [user](https://github.com/HUNTERCAT-DIGITAL/lieshou-cloud-user-services) · [admin](https://github.com/HUNTERCAT-DIGITAL/lieshou-cloud-admin-services) · [approval](https://github.com/HUNTERCAT-DIGITAL/lieshou-cloud-approval-services) · [gateway](https://github.com/HUNTERCAT-DIGITAL/lieshou-cloud-gateway-services) |
| 契约层 | [contract-types](https://github.com/HUNTERCAT-DIGITAL/lieshou-contract-types) · [contract-api](https://github.com/HUNTERCAT-DIGITAL/lieshou-contract-api) · [contract-config](https://github.com/HUNTERCAT-DIGITAL/lieshou-contract-config) |
| 前端 | [core-web](https://github.com/HUNTERCAT-DIGITAL/lieshou-core-web) · [ui](https://github.com/HUNTERCAT-DIGITAL/lieshou-ui) |
| 多端 | [admin-web](https://github.com/HUNTERCAT-DIGITAL/lieshou-app-admin-web) · [mobile](https://github.com/HUNTERCAT-DIGITAL/lieshou-app-mobile) · [desktop](https://github.com/HUNTERCAT-DIGITAL/lieshou-app-desktop) · [mini-program](https://github.com/HUNTERCAT-DIGITAL/lieshou-app-mini-program) |

## 🧭 架构演进

> **上一代**：一个模块一个仓（20+ 仓，依赖用 submodule 串起来）
> **当前**：前后端各收敛为一个单仓 —— 契约先行、共享层、多端同仓，一条 CI 跑全链路

## 🤝 参与

- 需求 / Bug 走 [Issues](https://github.com/HUNTERCAT-DIGITAL)
- 代码以 Apache-2.0 授权，欢迎 issue 与 PR

## 📫 联系

🌐 [huntercat.cn](https://huntercat.cn) · 👤 维护者 [@FutureWL](https://github.com/FutureWL)
