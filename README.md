# 🚀 Meta-Rules-Dat
**Industrial-Grade High-Performance Binary RuleSets for Mihomo**

![Build Status](https://img.shields.io/github/actions/workflow/status/jiaoxb2008/meta-rules-dat/compile_mrs.yml?style=flat-square&label=MRS%20Compiler)
![License](https://img.shields.io/github/license/jiaoxb2008/meta-rules-dat?style=flat-square)
![Release](https://img.shields.io/github/v/release/MetaCubeX/mihomo?label=Mihomo%20Core&style=flat-square)

本仓库致力于通过 **GitHub Actions** 自动化流水线，将原始规则源码（YAML）实时编译为高效的 **Mihomo (Clash Meta) 二进制规则集 (MRS)**。旨在为透明网关（PVE/OpenWrt）提供极速、精准且低负载的流量分流体验。

---

## 💎 项目亮点
* **⚡ 极速检索**：采用二进制 MRS 格式，利用哈希树（Trie）索引，规则匹配延迟降至微秒级。
* **🤖 自动化工厂**：基于 `src/dist` 架构，修改 YAML 后云端自动触发 `mihomo` 内核编译，无需人工干预。
* **🔒 安全可信**：所有二进制产物均由 GitHub Actions 在干净的 Ubuntu 环境中透明编译生成。

---

## 🏗️ 项目架构
遵循现代软件工程的 `src`（源码）与 `dist`（产物）分离原则：

```bash
meta-rules-dat/
├── src/           # 📝 原始规则源码 (YAML 格式，人类可读)
│   ├── xxx_domain.yaml
│   └── xxx_ip.yaml
├── dist/          # 📦 编译后的成品 (Binary MRS，机器高效读取)
│   ├── xxx_domain.mrs
│   └── xxx_ip.mrs
└── .github/       # ⚙️ 自动化流水线配置 (CI/CD)
```
