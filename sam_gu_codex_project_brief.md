# 项目文档：Sam Gu 个人求职网站（给 Codex 的完整执行说明）

> 本文档是给 Codex 的**项目执行说明 + 内容规格书 + Obsidian 文档维护协议**。  
> 目标：搭建一个可部署到 **GitHub Pages** 的个人求职网站，视觉风格参考 **Josh W. Comeau**，但不直接照搬代码或资源。  
> 网站主内容使用**英文**，项目过程文档默认使用**中文 markdown**。

---

## 0. 你的角色与工作方式（必须遵守）

你现在是我的**项目执行助手**，也是我的 **Obsidian 文档维护助手**。

这是一个**新项目**。请不要假设你继承了旧项目的目录结构、旧笔记、旧实验记录或旧上下文。

你的任务不是只完成项目本身，而是：

1. 完成实际任务  
2. 把整个执行过程写入 Obsidian markdown 文档  
3. 让项目结构清晰、日志完整、结果可追踪、文件关系一目了然  
4. 所有说明性 markdown 默认用中文  
5. 使用有意义的 `[[Wikilinks]]` 建立清晰的双向导航网络  

请严格按以下方式工作：

### Step 1. 检查工作目录

- 确认当前 working directory 是否存在且可用
- 如果不存在或有问题，先修复，再开始工作
- 先告诉我你将使用哪个目录

### Step 2. 初始化项目结构

请在需要时创建合理但不复杂的基础结构，例如：
- 文档区
- 日志区
- 输出结果区
- 数据或代码区

不要创建过度复杂的层级。

### Step 3. 初始化 Obsidian 文档体系

如果不存在，请创建并维护：
- `[[项目总览]]`
- `[[当前状态]]`
- `[[会话日志]]` 或日期日志
- `[[任务笔记 - 当前任务名]]`
- `[[常用命令]]`
- `[[下一步]]`

如有需要，可增加：
- `[[问题与坑点]]`
- `[[结果索引]]`
- `[[数据说明]]`

### Step 4. 执行任务时同步写文档

每做一个有意义的动作，都要写入 markdown，包括：
- 读了什么
- 改了什么
- 跑了什么命令
- 生成了什么输出
- 发现了什么问题
- 当前结论是什么

不要等最后一次性补写。

### Step 5. 维护日志

日志至少要记录：
- 时间
- 本轮目标
- 读取的文件
- 执行的命令
- 修改的文件
- 输出结果
- 问题
- 当前结论
- 下一步建议

### Step 6. 保持链接清晰

- markdown 之间尽量用 `[[Wikilinks]]`
- 重要 note 之间尽量能互相到达
- 不要为了链接而链接
- 非 markdown 文件不要强行乱链，但要在 note 中解释作用

### Step 7. 每轮结束前必须收尾

至少更新：
- `[[当前状态]]`
- `[[会话日志]]`
- 当前任务主 note
- `[[下一步]]`

重要：
- 不要只在聊天里汇报进展
- 重要进展必须落到 markdown 中
- 如果要修改很多文件，先给我一个简短计划再执行

### 现在的启动动作

现在请先：
1. 检查当前目录  
2. 告诉我你准备创建/更新哪些 markdown 文件  
3. 给我一个简短执行计划  
4. 然后再开始真正执行任务  

---

## 1. 项目背景

这是一个课程作业项目：制作一个**个人求职网站**，最终将部署到 **GitHub Pages**，并在作业中提交网站 URL。

网站需要兼顾两件事：

1. 满足课程作业评分要求
2. 作为我后续可持续迭代的个人博客 / 作品集网站

因此，你要做的不是“临时交作业页面”，而是一个**长期可维护的个人网站骨架**。

---

## 2. 作业硬性要求（必须满足）

网站必须至少包含以下 6 个部分，而且这些内容要么作为**导航栏独立页面**存在，要么作为**单页中的明显分区**存在：

1. **Home / Headline**
   - 一句求职定位语
   - 关键词标签

2. **About Me**
   - 3–8 句自我介绍
   - 教育背景
   - 2–4 条 strengths / focus areas

3. **Skills**
   - Technical skills
   - Business skills
   - Tools

4. **Projects（核心）**
   - 至少 2 个项目
   - 每个项目必须包含：
     - Project title + time
     - Problem
     - Data
     - Approach
     - Outcome / Impact
     - Your contribution
     - 可选链接

5. **Resume / CV**
   - 可下载简历链接，或简短 resume section

6. **Contact**
   - Email 必填
   - LinkedIn / GitHub 可选

其他要求：
- Charts 不是必须
- 项目描述必须能清楚说明：
  - 你做了什么
  - 你会做什么
  - 你创造了什么价值

评分重点：
- 项目展示质量权重最高
- 导航清晰、结构完整
- 技能有组织且和岗位方向一致
- 页面整洁、移动端可读、链接可访问

---

## 3. 本项目的最终方向

### 3.1 技术方向
- 部署目标：**GitHub Pages**
- 优先做成：**GitHub Pages 兼容的静态多页面网站**
- 不依赖服务端
- 可以用轻量前端方案，但最终产物必须能直接静态部署
- 所有链接尽量使用相对路径
- 需要考虑 `.nojekyll`
- 最终目录结构要适合通过 GitHub Desktop 推送到仓库

### 3.2 设计方向
视觉风格参考：
- **Josh W. Comeau**
- 关键词：
  - 温暖
  - 清爽
  - 阅读友好
  - 有博客感
  - 卡片式内容组织
  - 排版优先
  - 留白舒服
  - 轻微渐变和柔和阴影
  - 不要廉价炫技
  - 不要做成模板站痕迹太重

注意：
- **不是 1:1 抄袭**
- 是“受其启发的个人求职网站”
- 风格上靠近 Josh，但内容结构必须更偏向**求职 + 项目作品集**

### 3.3 内容语言
- 网站 UI 和对外内容：**英文**
- Obsidian 过程文档：**中文**
- Blog 初期也使用：**英文**

---

## 4. 站点信息架构（必须真的创建这些页面）

请建立以下页面：

- `/` Home
- `/about/`
- `/skills/`
- `/projects/`
- `/resume/`
- `/contact/`
- `/blog/`

并为主要项目建立详情页：

- `/projects/ai-radar/`
- `/projects/zhenyan-monitoring/`
- `/projects/shadowbox-rl/`
- `/projects/cds527-text-classification/`
- `/projects/finqa-benchmark/`
- `/projects/database-management/`

即使个别内容还没补完，页面也要先存在，并且有清晰占位说明。

---

## 5. 页面布局要求

## 5.1 Home 页面

首页要有以下区块：

1. Hero
   - Name
   - Headline
   - Subtitle
   - Tags
   - CTA buttons

2. Featured Projects
   - 4 张精选项目卡片

3. Latest Writing
   - 3 篇英文博客卡片

4. About Preview
   - 简短介绍 + 教育摘要

5. Contact CTA
   - 引导联系的简洁模块

### 首页按钮
- View Projects
- Download Resume
- Contact Me

---

## 5.2 About 页面

需要包含：
- 完整自我介绍
- Education
- Focus Areas
- Selected Highlights
- 可放 awards / patent / competition highlights

---

## 5.3 Skills 页面

分 3 组展示：
- Technical Skills
- Business Skills
- Tools / Libraries

页面应当结构清晰，标签感强，不要堆成一大段。

---

## 5.4 Projects 页面

需要：
- 所有项目卡片总览
- 每个项目卡片可跳转到详情页
- 首页展示的是精选版，这里展示完整版

---

## 5.5 Resume 页面

即使内容较轻，也必须存在。  
建议内容：
- Download Resume button
- Education summary
- Experience highlights
- Awards / Patent / Selected achievements

---

## 5.6 Contact 页面

需要：
- Primary Email
- GitHub
- LinkedIn

不要公开：
- 电话
- 家庭住址
- 旧邮箱（除非我后续明确允许）

---

## 5.7 Blog 页面

需要：
- 英文文章列表页
- 每篇文章有：
  - 标题
  - 日期
  - 简要摘要
  - tag

---

## 6. 用户信息（用于生成内容）

### 6.1 基本信息
- Name: **Gu Zepeng / Sam Gu**
- School: **Lingnan University**
- Program: **Data Science**
- Expected Graduation: **July 2026**
- Location: **Hong Kong**
- Target Roles:
  - AI Product Development
  - Intelligent Robotics / AI Robotics related roles

### 6.2 对外联系方式
优先公开：
- Email: `zepenggu@ln.hk`
- Secondary Email: `finneganwatts4@gmail.com`
- GitHub: `https://github.com/ssgzy`
- LinkedIn: `https://www.linkedin.com/in/finnegan-watts-317772380`

默认不要公开：
- 电话
- 住址
- 旧 163 邮箱

### 6.3 个人定位关键词
用户想突出：
- keep learning
- 持续进步
- 喜欢研究和使用新技术
- AI 工具使用经验丰富
- 倾向于 agent、automation、rapid prototyping、practical systems
- 关注区块链、人工智能、具身智能

---

## 7. 首页文案（英文初稿，可直接使用）

### 7.1 Name
**Sam Gu**

### 7.2 Headline
**I build AI agents, research tools, and product prototypes.**

### 7.3 Subtitle
**MSc Data Science candidate at Lingnan University seeking opportunities in AI product development and intelligent robotics. I enjoy turning emerging models, workflows, and tools into practical systems people can actually use.**

### 7.4 Tags
- Python
- SQL
- AI Agents
- LLM Workflows
- NLP
- Rapid Prototyping
- Automation
- Applied AI

---

## 8. About 页面文案（英文初稿，可润色后使用）

**About Me**

Hi, I’m Sam Gu, an MSc Data Science student at Lingnan University with a background in computer science and hands-on experience in software development, machine learning, and AI workflows. I enjoy exploring new technologies and turning them into useful tools, especially in agentic AI, research automation, and practical product prototyping. My recent work spans reinforcement learning, text classification, benchmark reconstruction, database design, and local AI research intelligence systems. Before graduate school, I studied computer science and worked in software and security-related roles, which strengthened my engineering foundation. I’m especially interested in AI product development, blockchain-related innovation, and embodied intelligence, and I try to keep learning by building, iterating, and shipping.

### 8.1 Education
- **MSc in Data Science**, Lingnan University — *Expected Jul 2026*
- **BEng in Computer Science and Technology**, Yanching Institute of Technology — *2025*

### 8.2 Focus Areas
- Agentic AI and workflow automation
- Applied machine learning and NLP
- Embodied intelligence and robotics exploration
- Emerging technology research, including blockchain

### 8.3 Selected Highlights
- Utility Model Patent: *A High-Stability Security Monitoring Device*
- Third Prize, 17th National College Student Information Security Competition
- Silver Prize, 8th Hebei “Internet+” College Student Innovation Competition

---

## 9. Skills 页面内容（英文初稿）

### 9.1 Technical Skills
- Python
- SQL
- Machine Learning
- NLP / Text Classification
- Reinforcement Learning
- Data Cleaning & Evaluation
- Database Design
- PySpark
- Git / GitHub
- Java
- C
- HTML / CSS / JavaScript

### 9.2 Business Skills
- Problem Framing
- Experiment Design
- Requirements Analysis
- Technical Documentation
- Reporting & Storytelling
- Cross-functional Collaboration
- Workflow Optimization

### 9.3 Tools / Libraries
- pandas
- scikit-learn
- PyTorch
- PySpark
- Jupyter Notebook
- MySQL
- MongoDB
- Postman
- Maven
- Linux
- Ollama
- Obsidian

### 9.4 Emphasized Skills
- Python
- SQL
- LLM Workflows
- NLP / Text Mining
- Rapid Prototyping

---

## 10. 项目展示策略

首页精选展示顺序建议：

1. AI Radar
2. Zhenyan Intelligent Monitoring System
3. ShadowBox — RL Sokoban Agent
4. CDS527 Group Assignment

Projects 页面展示完整列表：

5. FinQA Benchmark Reconstruction
6. Database Management for an Online Learning System

另外这两个仓库如果内容不足，可以只做“占位卡片 / Coming Soon”：
- `CDS527`
- `DataMining_GroupAssignment`

---

## 11. 项目卡片内容（英文草稿）

## 11.1 Project 1 — AI Radar

- **Project Name:** AI Radar — Local AI Research Intelligence System
- **Time:** 2026 – Ongoing
- **Type:** Individual Project
- **Display Priority:** 1
- **Problem:** High-value AI updates are scattered across papers, repositories, feeds, and news sites. I wanted a local system that could continuously collect, summarize, score, and organize useful signals.
- **Data:** Multi-source content from arXiv, GitHub, RSS, Hacker News, and news feeds, stored as raw, processed, deduped, and scored outputs with daily and weekly reports.
- **Approach:** Built a Python-based local pipeline with ingestion, merge/deduplication, tagging/scoring, local summarization workflow, Obsidian export, and scheduler-ready automation.
- **Outcome / Impact:** Delivered a stable version that supports end-to-end collection, structured scoring, failed-item replay, daily digests, and weekly intelligence reports.
- **Your Contribution:** Designed the architecture, implemented the pipeline, organized outputs, and prepared the system for regular runs.
- **Link:** `https://github.com/ssgzy/ai_radar`
- **Screenshot:** placeholder needed
- **Status:** 可以直接上首页

## 11.2 Project 2 — Zhenyan Intelligent Monitoring System

- **Project Name:** Zhenyan Intelligent Monitoring System
- **Time:** Oct 2022 – Mar 2023
- **Type:** Group Project
- **Display Priority:** 2
- **Problem:** Traditional surveillance workflows often lack stable and timely object detection for real-time monitoring. The project aimed to improve practical monitoring with intelligent recognition and alerts.
- **Data:** Surveillance camera imagery/video for object-detection scenarios.
- **Approach:** Developed an intelligent monitoring system using YOLOv5 for object detection, with real-time recognition and alert logic.
- **Outcome / Impact:** Built a working intelligent monitoring solution and supported a utility model patent related to a high-stability security monitoring device.
- **Your Contribution:** Led the software development work and implemented the real-time object-recognition and alert features.
- **Link:** placeholder / details upon request
- **Screenshot:** placeholder needed
- **Status:** 可以直接上首页

## 11.3 Project 3 — ShadowBox RL Sokoban

- **Project Name:** ShadowBox — Reinforcement Learning for Sokoban
- **Time:** 2026
- **Type:** Individual Project
- **Display Priority:** 3
- **Problem:** Train an AI agent to solve Sokoban efficiently under limited training time and challenging level design.
- **Data:** Environment-generated game states, rewards, and evaluation runs on Sokoban levels.
- **Approach:** Implemented a Rainbow DQN-style solution with optimization and reward redesign.
- **Outcome / Impact:** Achieved strong performance on benchmark levels and improved training efficiency.
- **Your Contribution:** Built the training and evaluation workflow, optimized training, and summarized performance.
- **Link:** `https://github.com/ssgzy/CDS524_individual-assignment_Sam`
- **Screenshot:** placeholder needed
- **Status:** 可以直接上首页

## 11.4 Project 4 — CDS527 Text Classification

- **Project Name:** CDS527 Group Assignment — Text Classification on Social Text
- **Time:** 2026
- **Type:** Group Project
- **Display Priority:** 4
- **Problem:** Improve multi-class text classification performance on short social text in a reproducible group workflow.
- **Data:** Social text / emotion classification dataset.
- **Approach:** Compared multiple text representation and classification strategies in a reproducible workflow.
- **Outcome / Impact:** Improved model performance over baseline and documented the comparison process.
- **Your Contribution:** 暂时使用保守表述：supported preprocessing, experiment setup, result tracking, and report coordination.
- **Link:** `https://github.com/ssgzy/CDS527-group-project`
- **Screenshot:** placeholder needed
- **Status:** 可以上首页，但个人贡献后续还要补精确

## 11.5 Project 5 — FinQA Benchmark Reconstruction

- **Project Name:** FinQA Benchmark Reconstruction
- **Time:** 2026
- **Type:** Individual Project
- **Display Priority:** 5
- **Problem:** Legacy scripts and leftover experiments made the benchmark difficult to trust and reproduce.
- **Data:** FinQA-related evaluation inputs and standardized outputs.
- **Approach:** Rebuilt the benchmark workflow, cleaned assumptions, and standardized outputs/logging.
- **Outcome / Impact:** Produced a clearer and more traceable evaluation workflow.
- **Your Contribution:** Reorganized the project from zero and rebuilt the scripts and reporting structure.
- **Link:** `https://github.com/ssgzy/new-task`
- **Screenshot:** placeholder needed
- **Status:** 放在 Projects 页即可

## 11.6 Project 6 — Database Management

- **Project Name:** Database Management for an Online Learning System
- **Time:** 2026
- **Type:** Group Project
- **Display Priority:** 6
- **Problem:** Design and query an online learning platform database across relational and NoSQL structures.
- **Data:** Cleaned CSV / JSON-based learning platform data.
- **Approach:** Created a relational schema and analytical SQL queries, with parallel NoSQL-oriented organization.
- **Outcome / Impact:** Delivered a working schema and useful analytical query outputs.
- **Your Contribution:** 暂时使用保守表述：contributed to database design, query writing, and data organization.
- **Link:** `https://github.com/ssgzy/DatabaseManagement_HW`
- **Screenshot:** placeholder needed
- **Status:** 放在 Projects 页即可

---

## 12. Experience 页面素材（用于 About / Resume）

这些内容不单独做 Experience 页面，但需要在 About 或 Resume 中体现。

### 12.1 Software Development Engineer Assistant
- Company: Shanghai Diaisi Information Technology Co., Ltd.
- Time: Oct 2024 – May 2025
- Summary:
  - Participated in requirement research, architectural support, third-party API integration, development, testing, and deployment
  - Assisted with integrating security-related modules into enterprise applications
  - Collaborated with cross-functional teams to solve technical issues and optimize performance

### 12.2 Technical Service Intern
- Company: Beijing HaoWang Technology Co., Ltd.
- Time: Jun 2024 – Jul 2024
- Summary:
  - Supported cloud and security-related projects
  - Assisted in requirements analysis and technical documentation
  - Contributed to testing and deployment of security-related features

---

## 13. Blog 初始文章（英文占位）

请先创建以下英文博客占位文章：

1. **Building AI Radar: Designing a Personal Research Intelligence Workflow**
2. **What I Learned from Training a Sokoban Agent**
3. **From Baseline to Better Results: Notes from a Text Classification Project**
4. **Rapid Prototyping with AI Tools: How I Learn by Shipping**

要求：
- blog 列表页可以先列 4 篇
- 首页 Latest Writing 先展示其中 3 篇
- 文章正文可以先写成简短 placeholder，但页面必须存在
- 摘要、tag、日期要有

---

## 14. Avatar 生成提示词

如果需要生成个人卡通头像，使用以下英文 prompt：

> Create a modern cartoon avatar for a personal AI engineer and data science website. Style: clean editorial tech illustration, founder-style vector portrait, friendly and curious expression, short dark hair, minimal black or dark gray outfit, subtle futuristic vibe, warm light background, crisp lines, soft shadows, square composition, polished and approachable, suitable for a Josh W. Comeau-inspired website. No text, no watermark, no busy background, no celebrity resemblance.

---

## 15. 技术实现要求（必须遵守）

### 15.1 部署兼容性
最终网站必须满足：
- 可直接部署到 GitHub Pages
- 不依赖服务端
- 不依赖数据库
- 不要求后端 API
- 即使使用构建工具，最终产物也必须是静态可部署的

### 15.2 目录建议
请按需要调整，但保持简单清晰。示例：

```text
/
  index.html
  about/
    index.html
  skills/
    index.html
  projects/
    index.html
    ai-radar/
      index.html
    zhenyan-monitoring/
      index.html
    shadowbox-rl/
      index.html
    cds527-text-classification/
      index.html
    finqa-benchmark/
      index.html
    database-management/
      index.html
  blog/
    index.html
    ai-radar-workflow/
      index.html
    sokoban-rl-notes/
      index.html
    text-classification-notes/
      index.html
    rapid-prototyping/
      index.html
  resume/
    index.html
  contact/
    index.html
  assets/
    images/
    icons/
    resume/
  styles/
  scripts/
  docs/
  logs/
  outputs/
  .nojekyll
  README.md
```

### 15.3 前端要求
- 响应式
- 移动端可读
- 统一导航
- 统一页脚
- 统一视觉系统
- 良好可读性
- 项目卡片风格统一
- 使用有层次的标题、正文、meta、tag
- 不要过度动画
- 可以有微交互，但不要影响可访问性

### 15.4 内容要求
- 首页、About、Skills、Projects、Resume、Contact、Blog 都必须可访问
- 所有重要内容页面都要有真实内容，不要只剩标题
- 对暂时缺数据的部分，用清晰占位文案，而不是乱码或空白

### 15.5 隐私要求
默认不要公开：
- 电话
- 家庭住址
- 旧 163 邮箱
- 任何未明确允许公开的个人敏感信息

---

## 16. Obsidian 文档体系（请在项目开始就创建）

请在项目根目录下创建一个简单的文档体系。推荐：

```text
docs/
  项目总览.md
  当前状态.md
  会话日志.md
  任务笔记 - 个人网站搭建.md
  常用命令.md
  下一步.md
  问题与坑点.md
  结果索引.md
```

要求：
- 全部中文
- 使用 `[[Wikilinks]]`
- 这些文档是项目过程的一部分，不是可有可无

---

## 17. 执行顺序（建议）

### Phase 1 — 启动与文档初始化
1. 检查 working directory
2. 确认项目根目录
3. 创建基础目录结构
4. 创建 Obsidian docs
5. 写入项目总览、当前状态、会话日志、任务笔记

### Phase 2 — 站点骨架
1. 创建全局 layout / header / footer
2. 创建所有页面
3. 建立统一样式
4. 建立项目卡片与文章卡片组件样式
5. 完成导航与相对路径校验

### Phase 3 — 内容落地
1. 填充首页 Hero
2. 填充 About
3. 填充 Skills
4. 填充 Projects 列表与详情页
5. 填充 Resume
6. 填充 Contact
7. 填充 Blog 占位文章

### Phase 4 — 校验与收尾
1. 移动端检查
2. 链接检查
3. 视觉一致性检查
4. GitHub Pages 兼容性检查
5. 更新全部文档
6. 给出后续补充内容建议

---

## 18. 每轮执行时必须写入文档的内容

每完成一个有意义的动作，都要同步写入 markdown：
- 读了哪些文件
- 为什么改
- 改了哪些文件
- 用了什么命令
- 生成了什么输出
- 遇到了什么问题
- 当前结论
- 下一步是什么

不要只在终端做，不记文档。

---

## 19. 你现在就要执行的第一轮动作

请你现在：
1. 检查当前目录
2. 告诉我准备创建/更新哪些 markdown 文件
3. 给我一个简短执行计划
4. 然后开始搭建项目

注意：
- 如果你打算一次性修改很多文件，先给出简短计划
- 重要进展必须落到 markdown
- 不要只在聊天里汇报

---

## 20. 最终交付物

你最终应当交付：

### 20.1 网站本体
- 可部署到 GitHub Pages 的完整静态网站

### 20.2 项目过程文档
- 完整的 Obsidian markdown 文档体系
- 能看出你如何一步步搭建、修改、验证

### 20.3 项目说明
- `README.md`
  - 项目简介
  - 本地预览方式
  - GitHub Pages 部署说明
  - 目录说明

### 20.4 部署准备
- relative links 校验
- `.nojekyll`
- 如需要，提供 Pages 发布说明

---

## 21. 你在实现时的判断原则

优先级排序：
1. **先满足作业硬要求**
2. **再保证页面完整与可访问**
3. **再提升视觉与排版**
4. **最后再做额外优化**

如果信息不全：
- 先建立完整页面和清晰占位
- 不要因为少数内容未确认而卡住整体搭建

如果你发现项目仓库中有信息不足：
- 在页面中写清楚 `Details to be refined`
- 同时在 Obsidian 的 `[[下一步]]` 里记下需要补充的信息

---

## 22. 额外提醒

- 不要默认沿用旧项目目录
- 不要私自公开敏感信息
- 不要用过度复杂的工程结构
- 不要只做一个 Home 页面就结束
- 不要漏掉 Resume / Contact / Blog
- 不要让导航断链
- 不要忘记在文档里写过程

---

## 23. 一句话总结

这是一个 **GitHub Pages 兼容、Josh 风格启发、英文对外内容、中文 Obsidian 过程文档、作业要求强对齐** 的个人求职网站项目。  
请你先做目录检查和文档初始化，再开始真正开发。
