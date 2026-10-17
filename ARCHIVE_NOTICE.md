# 存档声明 · dsh-infinite-gen-4（无限四代）v0.4.0

## 归属

- 原作者：**Minglink**（<https://github.com/Minglink>，提交身份 `108618469+Minglink@users.noreply.github.com`）
- 上游项目：`Minglink/dsh-infinite-gen-4` →（已改名）`Minglink/dsh-infinite-gen-5`
- 许可证：**CC BY-NC-SA 4.0**（署名 - 非商业性使用 - 相同方式共享），原文见仓库内 `LICENSE`
- 本仓库的性质：**第三方存档备份**，不隶属原作者，不代表作者背书，不用于商业用途

## 为什么有这个仓库

2026-10-17 核查到的情况：

- `https://github.com/Minglink/dsh-infinite-gen-4` 已 301 跳转到 `Minglink/dsh-infinite-gen-5`（同一仓库 id `1335211378`），`master` 现在是无限五代 v1.0.0，架构与四代完全不同（38 个逆向工具，作者明确不再占用全局系统提示词）。
- 四代没有独立的仓库页、tag、Release；第三方插件市场里的四代条目也已经检索不到。
- 四代代码目前只能从上游 git 历史的 `9097ccc` 检出；上游若重写历史或删除仓库，这份就不存在了。

所以这里把 `9097ccc` 单独存一份，版本号仍是 `package.json` 里的 `0.4.0`。

## 快照信息

| 项 | 值 |
|---|---|
| 提交 | `9097ccc1d22596087d47c732c317c29407c752ff` |
| 提交时间 | 2026-09-29 10:42:32 UTC（18:42 +08:00） |
| 提交说明 | Update README.md |
| 版本 | `0.4.0` |
| 文件数 | 29（`prompts/`、`scripts/`、`tests/`、`assets/`、安装脚本、许可证） |
| 归档日期 | 2026-10-17 |

## 保真说明

除下面四项外，所有文件与 `9097ccc` **逐字节一致**：

1. `README.md` 顶部加入「存档仓库（非官方）」声明块
   - 上游原文 SHA-256：`78beac42dd8d343b5b0c8e3175138b18ba3ac036a4fe9009991067e79783ccf`
2. 新增 `ARCHIVE_NOTICE.md`（本文件）
3. 新增 `SHA256SUMS.txt`（本仓库当前文件的校验值）
4. 新增 `.gitignore`

自检：

```bash
sha256sum -c SHA256SUMS.txt
```

## 安装方式（与上游一致）

Windows（PowerShell，在本目录执行）：

```powershell
.\install.ps1
```

Linux / macOS：

```bash
chmod +x install.sh && ./install.sh
```

脚本做的事（摘自脚本头注释）：检查 DSH 目录与 profile → 复制插件到 `~/.dsh/plugins/dsh-infinite-gen-4` → 备份并改写 profile 的 `package.json` 依赖与 `bundles` → 执行 `pnpm install` → 提示重启会话。卸载用 `uninstall.ps1` / `uninstall.sh`。

注意：README 顶部那个 `dsh://plugin/install?...repo=Minglink/dsh-infinite-gen-4` 的一键安装角标现在会失效（上游 repo 名已不存在），手动用上面的脚本安装。

## 它是什么

四代是「系统提示词注入」型的 DSH 插件：启动时向宿主注册两个系统提示词段（order 100 通用内核 + order 200 强化镜像），并提供 `infinite_gen4_profile` 元数据工具、输入框上方的客户端状态条、以及按回复开头窗口打分的会话投影。它与五代（工具型逆向工作台）不是同一条产品线，不要互相覆盖安装。

## 撤回

原作者 Minglink 如希望本存档下线，在仓库 Issues 留言或直接联系仓库所有者，收到即删（含历史）。
