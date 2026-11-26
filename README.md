# Engineering Learning Hub

求职导向的个人工程学习中心。课程依次为 Python、Java、Spring、AI Agent 和 AI Infra。CS Fundamentals 按主课穿插复习，Engineering 随实践推进。

## 接续学习

从 [AGENTS.md](AGENTS.md) 开始，再读 [LEARNING_STATE.md](LEARNING_STATE.md)、[ROADMAP.md](ROADMAP.md) 和 [SPACE_INDEX.md](SPACE_INDEX.md)。当前课程见 [Python 大纲](docs/02-python/curriculum.md)。

Space 保存权威学习文档，GitHub 私有仓库保存实践代码及 Space 的单向 Markdown 备份。备份时间、内容哈希和读取结果见 [备份清单](metadata/space-backup-manifest.json)。

## 仓库目录

| 目录 | 内容 |
| --- | --- |
| `docs/` | Space 快照、课程、能力档案、规范与模板 |
| `exercises/` | 学习者独立练习及验证材料 |
| `projects/` | 课程项目代码与测试 |
| `experiments/` | 可复现实验代码 |
| `scripts/` | 仓库辅助脚本 |
| `metadata/` | 页面备份清单及校验信息 |

## 本机 Python 与调试

本仓库用 CPython 3.14 的标准库 `venv`。Windows 从仓库根目录运行：

```powershell
py -3.14 -m venv .venv
.\.venv\Scripts\python.exe -c "import sys; assert sys.prefix != sys.base_prefix; print(sys.version.split()[0]); print(6 * 7)"
```

macOS / Linux 对应命令：

```sh
python3.14 -m venv .venv
./.venv/bin/python -c 'import sys; assert sys.prefix != sys.base_prefix; print(sys.version.split()[0]); print(6 * 7)'
```

两条最小程序都应得到版本及 `42`。在 VS Code 打开仓库根目录并安装或启用 Python 与 Python Debugger 扩展。通过 `Python: Select Interpreter` 选本机的 `.venv`（已选过其他解释器时需要手动切换）。打开要调试的 Python 文件，设置断点，按 `F5` 选 `Python: Debug Current File`。配置见 [.vscode](.vscode)。环境验收与课程证据分别记录。 [VS Code Python 调试文档](https://code.visualstudio.com/docs/python/debugging)

## 版本管理

从已认证的 GitHub 账号访问 [私有仓库](https://github.com/TobiichiMaster/engineering-learning-hub)。同步前运行 `git status --short --branch`，确认干净后使用 `git pull --ff-only`。各设备各自建立 `.venv`。需要 SSH 时，可使用 [GitHub SSH 443 指引](https://docs.github.com/en/authentication/troubleshooting-ssh/using-ssh-over-the-https-port)。
