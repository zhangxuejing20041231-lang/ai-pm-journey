# Agent Skills 学习清单

这份清单收集的是 Agent Skills 相关的仓库和资料。Skill 简单说就是给 AI 助手准备的“技能包”：一个文件夹，里面有一份 SKILL.md 说明书（写清楚这个技能是干什么的、什么时候用、按什么步骤做），有需要的话再带上脚本和参考资料。AI 助手碰到对口的任务时把说明书读进去，就能按固定的方法把事做完，不用每次从零交代。

这是第一批，先放最值得看的官方仓库、规范和几个精选合集，以后看到好的会继续往里加。链接都在 2026-11-26 核对过。

## 官方出处

### 1. anthropics/skills（Anthropic 官方技能仓库）

Anthropic 官方放出来的示例技能集合，一共十几个，创作文案、写代码、做文档、企业沟通都有。想搞懂“一个 skill 长什么样”，从这里看原版最靠谱，仓库里还带一份空白模板，照着改就能写自己的第一个 skill。

链接：https://github.com/anthropics/skills

### 2. Agent Skills 规范（agentskills.io）

Skill 这个格式的官方说明书：SKILL.md 开头那几行必填信息怎么写、文件夹怎么组织、为什么要“先看简介、用到时再读全文”（规范里管这叫渐进式披露）。内容不长，想自己动手写 skill 之前先把这一页看完，后面少走弯路。

链接：https://agentskills.io/specification

## 官方仓库里值得单独看的单个 skill

### 3. docx（文档技能，官方仓库内）

教 AI 助手创建和修改 Word 文档的技能，带脚本，是官方实际在用的文档能力背后的实现之一。同一个仓库的 skills 文件夹里还有 pdf、pptx、xlsx 三个姊妹技能，处理 PDF、PPT、Excel 的。这几个是目前能看到的“正经生产环境用的 skill”长什么样，想学 skill 怎么带脚本、怎么处理复杂文件，拆这几个看最直观。

链接：https://github.com/anthropics/skills/tree/main/skills/docx

### 4. skill-creator（官方仓库内）

一个“用来写 skill 的 skill”：你跟它说想做什么技能，它会一步步问清楚需求，帮你把 SKILL.md 搭出来，还带了测试和评估的脚本。现阶段不用真拿它干活，先把它的说明书读一遍，能学到官方认为一份好说明书应该交代哪些事。

链接：https://github.com/anthropics/skills/tree/main/skills/skill-creator

### 5. mcp-builder（官方仓库内）

教 AI 助手帮人搭建 MCP 服务器的技能，里面把“怎么把一个外部工具接给 AI 用”的流程写成了步骤。MCP 和工具调用是后面要学的内容，先收藏，等学到 Agent 和工具调用那部分再回来细看，会顺很多。

链接：https://github.com/anthropics/skills/tree/main/skills/mcp-builder

## 社区合集和成套技能库

### 6. superpowers（obra）

社区里很火的一套给编程助手用的技能库，一共十几个 skill，管的是干活的流程：写代码之前先讨论需求、出方案，再按计划一步步做、写测试、做检查。它的价值不在某个具体功能，而是示范了“怎么用一堆 skill 把 AI 的工作习惯管起来”，对理解 Agent 产品怎么设计流程很有参考意义。

链接：https://github.com/obra/superpowers

### 7. awesome-claude-skills（BehiSecc）

一个人工整理的 Claude Skills 精选目录，按文档处理、开发工具、数据分析、写作研究、科学工具等类别分好。适合当索引用：想找某个方向有没有现成 skill，先来这里翻，顺着链接去看原仓库。

链接：https://github.com/BehiSecc/awesome-claude-skills

### 8. awesome-llm-skills（mvanhorn）

同样是精选合集，范围比上面那个宽一点，不只收 Claude 的，还覆盖 Codex、Gemini CLI 等其他 AI 编程工具的 skill 和相关资源。想横向看看不同平台怎么做技能包、生态有什么差别，看这个。

链接：https://github.com/mvanhorn/awesome-llm-skills

### 9. awesome-agent-skills（mvanhorn）

这个合集只收录链接、不把别人的 skill 文件搬进自己仓库，条目都标了类型和支持的平台，分开发、数据、写作、创意、效率等类。它明确写了自己不是官方背书、收录不等于安全审核，这个态度也值得学：用社区 skill 之前先自己看一遍内容，别直接装。

链接：https://github.com/mvanhorn/awesome-agent-skills-1

## 现阶段怎么用这份清单

不用挨个装。先把官方仓库和规范看一遍，弄明白 SKILL.md 的结构；再挑 docx 或 skill-creator 一个，把说明书从头读到尾，看看别人是怎么把一件复杂的事拆成步骤写给 AI 的。等学到 Prompt 和 Agent 那几课，再回来试着照模板写一个自己的小 skill。
