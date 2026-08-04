# 宋浩风格高等数学 Skill · song-hao-math

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Skill](https://img.shields.io/badge/Grok%20%2F%20Claude%20%2F%20Cursor-Skill-00DC82)](#安装)
[![Math](https://img.shields.io/badge/考研数学-数一%20%7C%20数二%20%7C%20数三-blue)](#覆盖科目)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/tong666-bit/song-hao-math)

> **把会讲课的数学老师，装进你的 AI。**  
> 口语化 · 板书式推导 · 先直觉后公式 · 专治「公式会背题不会做」

**非官方致敬作品**：蒸馏公开教学中常见的通俗讲法与课堂节奏，**不是宋浩老师本人或官方出品**。

---

## 为什么会 Star？

| 痛点 | 这个 Skill 怎么治 |
|------|-------------------|
| AI 直接甩答案，过程像天书 | **板书式分步**，每步写清「为什么」 |
| 只记公式，没有几何直觉 | **先图像 / 人话，再严格定义** |
| 考研题型多，没有套路 | 每题附 **题型卡片**（识别 → 步骤 → 易错 → 变式） |
| 高数线代概率复变切换懵 | **分科 reference 按需加载**，体系完整 |

适合：**本科高数、考研数学一/二/三、复变入门、考前抢分复盘**。

---

## 30 秒感受差异

**普通 AI：**

> 由洛必达法则，原式 \(=\lim\dfrac{f'}{g'}=1\)。

**启用 song-hao-math 后（风格示意）：**

> 别慌，这是 **0/0 型**。  
> 你就想：分子分母一起趋于 0，比的是「谁变快」——洛必达用导数比速度。  
> **注意**：先确认是 0/0 或 ∞/∞，且导数极限存在，才能下结论。  
> 板书：……（逐步）  
> **易错点**：等价无穷小用在「相减抵消」时可能翻车。  
> **考研卡片**：未定式 → 化型 → 等价/洛必达/展开 → 回代。

---

## 覆盖科目

```text
高等数学 / 微积分    极限·导数·中值·Taylor·积分·ODE·多元·重积分·级数
线性代数            行列式·矩阵·秩·方程组·特征值·相似·二次型
概率论与数理统计    事件·分布·期望方差·CLT·估计检验
复变函数            解析·CR·Cauchy·Laurent·奇点·留数
考研综合            数一/数二/数三题型打法与得分策略
```

---

## 安装

### 方式一：Grok Build / Grok CLI

```bash
# 克隆到你的 skills 目录
git clone https://github.com/tong666-bit/song-hao-math.git

# 用户级（全局可用）
# Windows: %USERPROFILE%\.grok\skills\song-hao-math
# macOS/Linux: ~/.grok/skills/song-hao-math
```

把本仓库内容放到：

```text
~/.grok/skills/song-hao-math/
  SKILL.md
  references/
```

或在项目内：

```text
你的项目/.grok/skills/song-hao-math/
```

重启或等待 skills 自动热加载后，使用：

- 斜杠命令：`/song-hao-math`
- 或直接说：「用宋浩老师的方式讲这道极限题」

### 方式二：Claude Code / Codex / 兼容 Agent Skills 的工具

将本仓库作为 skill 目录安装（保证存在 `SKILL.md`）：

```bash
git clone https://github.com/tong666-bit/song-hao-math.git ~/.claude/skills/song-hao-math
```

（路径按你使用的工具文档微调；**核心是 SKILL.md + references/**。）

### 方式三：Cursor / 手动

1. Clone 本仓库  
2. 把 `SKILL.md` 内容加进项目规则 / Custom Skill  
3. 需要分科深度时，让 AI 读取 `references/` 下对应文件  

---

## 怎么用（复制即用）

```text
用宋浩风格讲：极限 lim(x→0) (tan x - sin x) / x^3，我是考研数二。
```

```text
/song-hao-math
特征值到底在说矩阵的什么几何意义？再给一个 2×2 例子。
```

```text
这道线代证明我写到一半卡了：（粘贴过程）
请按板书改错，并总结题型卡片。
```

```text
留数定理为什么能拿来算实积分？用大白话 + 一个经典例题。
```

---

## 仓库结构

```text
song-hao-math/
├── SKILL.md                          # 核心：触发条件 + 讲课协议
├── README.md                         # 你正在看的说明
├── LICENSE                           # MIT
├── examples/
│   └── demo-prompts.md               # 更多示例提问
└── references/
    ├── teaching-style.md             # 口吻与板书细则
    ├── calculus.md                   # 高数 / 微积分
    ├── linear-algebra.md             # 线性代数
    ├── probability.md                # 概率统计
    ├── complex-analysis.md           # 复变函数
    └── kaoyan-playbook.md            # 考研题型与得分策略
```

---

## 设计理念

1. **人话 → 图像 → 公式 → 板书 → 坑点 → 题型**  
2. **禁止「显然」跳步**——学生卡住的地方正是要展开的地方  
3. **分科 reference 渐进加载**——省 context，也更专业  
4. **致敬而非冒充**——开源社区友好、可审计、可改进  

---

## 贡献

欢迎 PR：

- 补充真题题型卡片  
- 纠错（笔误、条件遗漏）  
- 增加「经济数学 / 工科应用」案例  
- 改进触发 description，让更多学生在该用时自动命中  

提 Issue 时尽量带：**科目 + 原题 + 你期望的讲法**。

---

## 致谢与声明

- 教学风格向**优秀高数公开课讲法**致敬，尤其是让无数同学「豁然开朗」的通俗路线  
- **与宋浩老师无官方合作或授权关系**；若权利人希望调整命名或表述，请开 Issue，我们会积极响应  
- 数学内容以教材与考研大纲为准；AI 可能出错，**考试与作业请以老师/教材为准**，重要推导建议人工复核  

---

## License

[MIT](./LICENSE) — 可自由使用、分享、改进；来都来了，**点个 Star** 让更多考研的朋友搜到它 ⭐

---

<p align="center">
  <b>公式会背 ≠ 题会做 · 会讲的 AI，才像老师</b><br/>
  <sub>song-hao-math · 开源数学陪练</sub>
</p>
