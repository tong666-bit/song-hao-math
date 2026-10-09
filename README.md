# 宋浩风格数学 Skill · song-hao-math

口语化、分步板书、先直觉后公式，辅导本科高数、线代、概率统计与复变课程，也可按大纲适配考研数学一/二/三。

**非宋浩本人或官方出品。**教学组织与自编例题服务理解，不把没有出处的话术称作老师原话。

## 2026-10-09 更新

- 新增15个完整自编例题，包含识别、板书、结果、复核和关键变式。
- 为微积分、线代、概率统计、复变补充适用条件、参数和边界检查。
- 新增最小反例与错因诊断：等价相减、洛必达失败、重根对角化、不相关/独立、解析域/围道等。
- 新增可执行的复习计划与时间预算。
- 整理[公开课程与官方入口](references/sources.md)，标明核验范围。
- 澄清复变作为独立课程/专业课，不自动列入统考数一；当年考纲需另核验。

## 讲题示意（自编）

“别慌，这里不是把两个函数都换成x就完事。它们的一阶项相减没了，咱们要看三阶项。写出来，你就知道为什么极限是二分之一。”

公式之外，同时讲**为什么选这个方法、条件够不够、改一个条件还成立吗**。

## 安装

Claude Code：

**macOS / Linux**
```bash
git clone https://github.com/tong666-bit/song-hao-math.git ~/.claude/skills/song-hao-math
```

**Windows PowerShell**
```powershell
git clone https://github.com/tong666-bit/song-hao-math.git "$env:USERPROFILE\.claude\skills\song-hao-math"
```

**Windows CMD**
```bat
git clone https://github.com/tong666-bit/song-hao-math.git "%USERPROFILE%\.claude\skills\song-hao-math"
```

其他支持 Agent Skills 的工具（如Codex或其它代理）按其当前文档选择skill目录，放入整个仓库，保留 `SKILL.md` 与 `references/`。Grok、Cursor等具体路径、热加载和斜杠命令取决于版本，本项目不将未经核实的路径写成通用安装规则。

更新时，在安装目录执行 `git pull --ff-only`；有本地修改先保存并处理冲突，再重新打开会话。

## 复制即用

```text
用宋浩风格讲 lim(x→0)(tan x-sin x)/x^3，别跳步，解释为什么不能直接等价相减。
我的参数方程组在除以t-1后出错了，请找第一处错误。
重特征值为什么有时能对角化、有时不能？给两个2×2例子。
我算出协方差0，能不能说独立？请核条件并给反例。
留数算实积分时，怎么证明补上的半圆积分趋0？
我是考研数二，每天120分钟，帮我安排8周复习并核对每天时间。
```

更多示例见[examples/demo-prompts.md](examples/demo-prompts.md)。

## 资料导航

| 任务 | 文件 |
|---|---|
| 高数/微积分 | [calculus.md](references/calculus.md) |
| 线代 | [linear-algebra.md](references/linear-algebra.md) |
| 概率统计 | [probability.md](references/probability.md) |
| 复变 | [complex-analysis.md](references/complex-analysis.md) |
| 教学节奏 | [teaching-style.md](references/teaching-style.md) |
| 考研范围与题型 | [kaoyan-playbook.md](references/kaoyan-playbook.md) |
| 完整板书例题 | [worked-examples.md](references/worked-examples.md) |
| 错因与反例 | [error-diagnosis.md](references/error-diagnosis.md) |
| 复习计划 | [study-plans.md](references/study-plans.md) |
| 来源与核验限制 | [sources.md](references/sources.md) |

## 贡献

欢迎附原题和来源提交勘误。新增定理写清假设、结论和边界；新增原创题标自编，真题记录科目/年份/版本，不只有题号。资料以链接、摘要和原创解释为主。

指令与原创内容采用[MIT](LICENSE)；第三方课程和教材遵守原有许可。本次确认公开资源目录，不代表已观看全部视频或核对当前考研学科大纲。
