# funclash-dev

funclash 联合开发仓库，通过 Git 子模块固定多平台客户端与内核仓库的版本，
一次 clone 即可拉齐整套源码用于跨仓库联调。

## 项目

| 目录 | 项目 | 类别 | 说明 |
| --- | --- | --- | --- |
| `apps/funclash` | [funclash](https://github.com/farfarfun/funclash) | app | 基于 mihomo (Clash.Meta) 的多平台代理客户端（Android、Windows、macOS、Linux） |
| `apps/funclash-core` | [funclash-core](https://github.com/farfarfun/funclash-core) | core | FunClash 构建所依赖的 mihomo (Clash.Meta) 内核（默认分支 `funclash`） |

具体的环境准备、构建和开发方式见各子项目 README。

## 获取代码

首次克隆时同时拉取子模块：

```bash
git clone --recurse-submodules https://github.com/farfarfun/funclash-dev.git
cd funclash-dev
```

如果已克隆本仓库但 `apps/` 下子模块尚未初始化，可执行：

```bash
git submodule update --init --recursive
```

## 更新子模块

```bash
git submodule update --remote
git add apps/funclash apps/funclash-core
```

子模块指针的更新由本仓库记录，需要随父仓库一起提交。

---

## 关于 farfarfun

[farfarfun](https://github.com/farfarfun) 是一个专注于实用工具库的开源组织，
涵盖云存储、数据处理、AI、多媒体与开发工具链等方向。

- 🏠 组织主页：<https://github.com/farfarfun>
- 📧 联系：farfarfun@qq.com

本项目基于 [MIT](LICENSE) 协议开源。
