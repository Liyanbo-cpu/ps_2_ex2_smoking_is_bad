# PS2 Exercise 2 — collaboration setup

<!-- PS2_FINAL_TEAM_PLAN_START -->
## PS2 最终分工与前置顺序

本组完成第 1、2、3、5 题。A-E 为成员占位，确认后替换姓名。第 1、5 题沿用 PS1 的 Conda；第 2、3 题使用 Pixi。整合、报告、复跑和过程检查均明确到人；仅最终验收不预设人员。

### 仓库与环境

| 题目 | 小组仓库 | 环境安排 |
| --- | --- | --- |
| 第1题 | [first_repo](https://github.com/zcyMary/first_repo) | 沿用 PS1 的 Conda，补充检查工具 |
| 第2题 | [Smoking](https://github.com/starries-creator/ps_2_ex2_smoking_is_bad) | Pixi，环境名 `smoke` |
| 第3题 | [NBA](https://github.com/starries-creator/ps_2_ex3_database) | 沿用老师的 Pixi 配置，Python 3.12，环境名 `nba` |
| 第5题 | [Titanic](https://github.com/starries-creator/ps1_ex4_nb_to_repo_forked) | 沿用 Conda，Python 3.13.16、pandas 2.3 |

### 成员分工

| 成员 | 第1题 | 第2题 | 第3题 | 第5题 |
| --- | --- | --- | --- | --- |
| **A** | 工具配置、全文件检查、跟进工具 PR | 变量分布图与解释 | 洞见① | 家庭变量分析 |
| **B** | 忽略/CSV 验证、跟进忽略 PR | **优先配置环境**，完善锁文件、README、nbstripout | 洞见② | 年龄、票价分析 |
| **C** | data_cleaner 类型标注、跟进标注 PR | 数据清理、TODO、总体生存率 | **准备数据与表结构**，完成打包及加载模块解释 | 图表取舍、报告/README 整合及复跑 |
| **D** | data_loader、visualizer 类型标注 | 分组生存率比较、notebook 整合及复跑 | 洞见③ | 性别、舱位分析 |
| **E** | mypy 依赖验证，结合 B 的结果回答两问 | 年龄分组敏感性检查 | 洞见④、分析 notebook 整合及复跑 | 缺失值与变量可用性 |

### 前置顺序

箭头表示先后；【并行】内的工作可同时开展。过程执行、整合、报告和检查按下面人员分工；每题最后均保留“最终验收”，不指定验收人员。

#### 第1题：并行修改，按顺序检查和合并

**【并行：A 工具配置｜B 忽略/CSV 验证｜C/D 类型标注｜E 两问验证】→ B 跟进忽略 PR、C 协同 D 跟进标注 PR，审查后分别合并 → A 同步工具 PR、运行全文件检查，各作者各自修正 → B/D 审查工具 PR，A 合并并清理分支 → 最终验收**

A 运行检查、记录问题并复核，各作者修自己的问题，不设全组统一合并协调人。C 标注 data_cleaner.py；D 标注 data_loader.py 和 visualizer.py。忽略 PR 由 A/D review，标注 PR 由 A/E review，工具 PR 由 B/D review，各需两名非作者批准。A/B/C 分别跟进工具/忽略/标注 PR 的审查、合并和来源分支清理；E 完成两问答案。各人合并后同步并安装 hooks，合并按仓库权限执行。

#### 第2题：环境先行，分析并行，D 负责整合

**B 配好 Pixi smoke 环境、锁文件和 README → C 清理并准备数据 →【并行：A 变量分布｜D 分组生存率｜E 年龄分组敏感性】→ A/C/D/E 交齐各自结果 → D 整合 notebook、复跑 → A 审查，D 修正并协调合并、清理来源分支 → 最终验收**

B 可并行完善 nbstripout；提交前各成员在自己的 clone 安装 hook。D 的整合工作限于接入、复跑和统一格式，各部分作者负责自己的代码、图表和解释。

#### 第3题 NBA：数据可读后并行，E 负责整合

**C 明确数据入口、路径和表/列，各人在本机验证可读 →【并行：A 洞见①｜B 洞见②｜D 洞见③｜E 洞见④｜C 打包】→ A/B/D/E 交齐洞见，C 验证打包和函数导入 → E 接入 analysis.ipynb 并复跑 → D 审查，E 协调各作者修正、合并并清理来源分支 → 最终验收**

warm-up 同步开展：C 路径/连接，A 数据库结构，B 数据表列表，D 指定表字段，E 最早/最晚比赛日期。已自行验证数据可读者可先分析；选题可与数据准备并行。无需先完成整份 warm_up.ipynb、pyproject.toml 或 analysis.ipynb；C 的打包/导入验证需在最终整合前完成。

#### 第5题：并行分析，C 负责报告和 README

**各自确认原 Conda 环境可用 →【并行：C 审阅已有图表｜A 家庭变量｜B 年龄/票价｜D 性别/舱位｜E 缺失值/变量可用性】→ A/B/D/E 交齐结果和解释 → C 筛图、整合报告及 README 并复跑 → B 审查，C 协调各作者修正、合并并清理分支 → 最终验收**

C 以报告整合替换原家庭分析任务，不额外承担独立 NBA 洞见；先释放 NBA 可读数据入口，待 A/B/D/E 交齐图表和解释后整理≤500词报告（不含图），更新 README 并保留原说明。各作者自行修复分析和代码，C 不代做。最终验收不指定人员。

### 交付与协作

各作者交齐自己的代码、必要图表和简短解释；第3题每条洞见还需包含查询和相关函数。过程检查用于修正提交；最终验收用于最后确认整体完成。第1题由 A 运行全文件检查，各作者修复自己的问题，各 PR 作者跟进自己的审查与合并，第2题由 D 整合并复跑，第3题由 E 整合并复跑，第5题由 C 整合报告/README 并复跑；过程审查人员见各题流程，最终验收不指定人员。整合者负责接入、复跑、统一格式及已分配的报告整理；各作者负责自己的分析和修复。B 优先完成第2题环境，C 优先交付 NBA 可读数据入口；各人再按依赖开展后续工作。通过分支和 PR 协作，开工前划清函数、文件和 notebook 修改范围。PR 合并后删除对应远程和本地来源分支；未合并的分支保留。

作业占位文件和原 notebook 中的 TODO 由对应成员完成；本次只同步分工及操作说明，不预填分析、答案或报告。
<!-- PS2_FINAL_TEAM_PLAN_END -->

## Start here: Pixi environment preparation

本题使用 **Pixi**。B 优先完成仓库根目录的 `pixi.toml`，建立 `smoke` 环境，生成锁文件并更新本 README；同时配置 nbstripout。根配置目前仍为空，是待完成的作业，其他成员在 B 的正式配置合并后按更新后的步骤安装。环境可用后 C 进行数据准备，再开展并行分析；提交前各自在本机安装 hook。

现有 `environment/pixi.toml` 和对应锁文件是可选的临时前置环境，供 B 配置时参考；它们不替代根目录的正式作业配置。以下原有启动及验证说明保留为临时环境参考。

<details>
<summary>可选临时前置环境：保留原有 Pixi 启动说明</summary>

## Start here

The PS2 setup uses Python 3.12 and a committed lock file. Four platforms are
resolved: macOS Apple Silicon, macOS Intel, Linux x86-64, and Windows x86-64.
Runtime validation is performed on macOS Apple Silicon; other platforms are
dependency-resolved, not runtime-tested. Install Pixi from https://pixi.sh/ .

From the repository root:

```bash
pixi install --manifest-path environment/pixi.toml --locked -e smoke
pixi run --manifest-path environment/pixi.toml -e smoke jupyter
```

Use the Python kernel from that environment. Do not use a global Python or a
teammate's absolute environment path. Other CPU architectures require a team
manifest/lock update first. See [CONTRIBUTING.md](CONTRIBUTING.md) for branches,
reviews, notebook editing, and local-file rules.

Use the explicit manifest commands above while the root manifest is empty.
The assigned environment owner still completes the root `pixi.toml` with a
`smoke` environment and configures the nbstripout hook. The bootstrap includes
the nbstripout package, but DOES NOT implement or install the coursework hook.
After the team completes the root manifest, regenerate its lock file and agree
the switch to root commands in the same PR. Do not change both manifests independently.

</details>

## Files and unfinished coursework

- `smoking_is_bad.ipynb`: original notebook and TODOs, unchanged.
- `data/smoking_data.csv`: original supplied data, retained.
- Root `pixi.toml` and `.pre-commit-config.yaml`: intentionally EMPTY coursework placeholders.
- `environment/pixi.toml` + `environment/pixi.lock`: a separate runnable bootstrap environment.
- `figures/`: final figure exports, tracked by Git.
- `docs/findings.md`: intentionally EMPTY optional working notes; final analysis belongs in the notebook.

B completes the formal root `pixi.toml`, lock file, nbstripout configuration,
and startup instructions. Other members use those instructions once the formal
configuration is merged. The optional bootstrap is a reference for B, not the
completed coursework environment.



## Setup verification

Verified on 2026-11-03 with Python 3.12.16 on macOS Apple Silicon.
Checks passed: notebook valid: smoking_is_bad.ipynb; headless PNG rendering; provided CSV readable (no analysis performed); nbstripout clears a disposable notebook; coursework hook remains empty; fresh Jupyter kernel executes disposable Python/pandas cell.
Other platforms were lock-resolved only. No coursework analysis, answers,
model training, or Kaggle data download was performed.

## Original repository instructions (retained)

# PS 2, ex 2 Smoking is bad

# Setup

To install the required packages, run the following command in the terminal (!Your task is to set up the environment using Pixi such that the following works!):

```bash
pixi install
pixi shell
```

## Pre-commit

This repository uses pre-commit to run some checks before each commit. !You have to first create
the .pre-commit-config.yaml!

To install pre-commit, run:

```bash
pre-commit install
```

To run the checks manually, run:

```bash
pre-commit run --all-files
```
