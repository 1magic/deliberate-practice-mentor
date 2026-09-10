# 会话末总结图模板（三图骨架）

**何时读本文档**：仅在会话末「汇报」步要出总结图前加载——平时不进上下文（token 优化 · 反全量扫描）。
**怎么用**：选图 → 取对应骨架 → 填本次会话数据 → 出图。填数代替从零设计，保证跨会话格式稳定。

## 选图规则（三选一）

| 本场产出 | 用图 |
|---------|------|
| 验证/搞懂了一个机制、一条链路 | **机制链路图**（横向流） |
| 常规练习收尾（默认） | **战报总览图**（三块式） |
| 阶段/月度回顾，看长期进度 | **里程碑进度图**（进度条） |

## 通用制图规范（防翻车 · 每次出图前过一遍）

1. **一图一主题**：信息超过一屏就拆两图，不硬塞。
2. **数据溯源**：图里每个数字/状态必须来自本次会话的蒸馏产物（goal-brief DoD / 热力图更新 / error-log / session-brief）——**禁止编造或美化**。无数据就写「本场无新坑」「待验证」，不画空壳。
3. **颜色语义**：绿=掌握/成果 ｜ 琥珀=待巩固/警告 ｜ 红=错误 ｜ 灰=中性。单图 ≤2 色系 + 灰。
4. **文字溢出自检**：中文字号 ≈ 每字宽 = font-size（12px 字 = 12px 宽）。标签长度按「可用宽 ÷ 字号」估，放不下就拆行或缩句。SVG 不自动换行。
5. **主题适配**：浅色主题 = 浅底深字（示例配色直接用）；深色主题整体反转（底 #0d1117、卡 #161b22、字 #e6edf3，语义色换浅调：绿 #3fb950 / 琥珀 #d29922 / 红 #f85149）。
6. **字号 ≥11**；卡片圆角 rx=8-12；图内不出现 emoji（渲染不稳，用色块/文字代替）。
7. 图讲结构，出完图 ≤5 行文字讲结论。

---

## 模板一：战报总览图（三块式）

回答「这场练得怎么样」。三块并排：掌握热力图变化 + DoD 达成 + 错误入账，底部状态条。

**填写对照**：header=课号/主题/场次·日期 ｜ 卡1 每行=知识点（前圆=练前状态色，后圆=练后）+ 底部总结 ｜ 卡2 每行=DoD 编号+验证证据 ｜ 卡3=本场错误编号+一句话 ｜ footer=状态变量 + 下一步。

```svg
<svg viewBox="0 0 680 360" width="100%" role="img" xmlns="http://www.w3.org/2000/svg">
<title>战报 · L-001 主题</title>
<text x="40" y="46" font-size="15" font-weight="500" fill="#1F2328">战报 · L-001 ｜ 主题名</text>
<text x="640" y="46" font-size="12" fill="#57606A" text-anchor="end">场 1/1 · 2026-09-09</text>

<rect x="40" y="76" width="192" height="196" rx="12" fill="#FFFFFF" stroke="#D0D7DE" stroke-width="1"/>
<text x="56" y="106" font-size="13" font-weight="500" fill="#24292F">掌握热力图变化</text>
<line x1="54" y1="124" x2="218" y2="124" stroke="#D0D7DE" stroke-width="0.5"/>
<circle cx="64" cy="150" r="5" fill="#CF222E"/>
<line x1="72" y1="150" x2="96" y2="150" stroke="#8C959F" stroke-width="1.5"/>
<circle cx="104" cy="150" r="5" fill="#1A7F37"/>
<text x="114" y="150" font-size="12" fill="#1F2328" dominant-baseline="central">数据清洗</text>
<circle cx="64" cy="178" r="5" fill="#9A6700"/>
<line x1="72" y1="178" x2="96" y2="178" stroke="#8C959F" stroke-width="1.5"/>
<circle cx="104" cy="178" r="5" fill="#1A7F37"/>
<text x="114" y="178" font-size="12" fill="#1F2328" dominant-baseline="central">窗口函数</text>
<text x="56" y="214" font-size="12" fill="#57606A">2 项升级 · 换场景验证通过</text>
<text x="56" y="238" font-size="12" font-weight="500" fill="#9A6700">next_review +3d / +7d</text>

<rect x="244" y="76" width="192" height="196" rx="12" fill="#FFFFFF" stroke="#D0D7DE" stroke-width="1"/>
<text x="260" y="106" font-size="13" font-weight="500" fill="#24292F">DoD 达成</text>
<line x1="258" y1="124" x2="422" y2="124" stroke="#D0D7DE" stroke-width="0.5"/>
<circle cx="269" cy="150" r="9" fill="#1A7F37"/>
<text x="269" y="150" font-size="11" fill="#FFFFFF" text-anchor="middle" dominant-baseline="central">1</text>
<text x="288" y="150" font-size="12" fill="#1F2328" dominant-baseline="central">换场景题 5/5</text>
<circle cx="269" cy="178" r="9" fill="#1A7F37"/>
<text x="269" y="178" font-size="11" fill="#FFFFFF" text-anchor="middle" dominant-baseline="central">2</text>
<text x="288" y="178" font-size="12" fill="#1F2328" dominant-baseline="central">链路重述通过</text>
<text x="260" y="214" font-size="12" font-weight="500" fill="#1A7F37">2/2 DoD 达标</text>
<text x="260" y="238" font-size="12" fill="#57606A">允许闭环 → 拆下一目标</text>

<rect x="448" y="76" width="192" height="196" rx="12" fill="#FFFFFF" stroke="#D0D7DE" stroke-width="1"/>
<text x="464" y="106" font-size="13" font-weight="500" fill="#24292F">错误入账</text>
<line x1="462" y1="124" x2="626" y2="124" stroke="#D0D7DE" stroke-width="0.5"/>
<rect x="464" y="139" width="84" height="22" rx="11" fill="#FFEBE9" stroke="#CF222E" stroke-width="0.5"/>
<text x="506" y="150" font-size="11" fill="#CF222E" text-anchor="middle" dominant-baseline="central">E-CON-003</text>
<text x="464" y="178" font-size="12" fill="#1F2328" dominant-baseline="central">同名两表引用歧义</text>
<text x="464" y="214" font-size="12" fill="#57606A">四段式已入账 · 已修正</text>
<text x="464" y="238" font-size="12" fill="#57606A">再犯 ≥2 次 → 升规则区</text>

<rect x="40" y="292" width="600" height="54" rx="10" fill="#F6F8FA" stroke="#D0D7DE" stroke-width="1"/>
<text x="56" y="314" font-size="12" fill="#1F2328" dominant-baseline="central">质量 8/10 ｜ 能量 7/10 ｜ 分心 低 ｜ 挑战 3/5 → 难度保持</text>
<text x="56" y="332" font-size="12" fill="#57606A" dominant-baseline="central">下一步：拆 L-002（DoD 全达标 + 体感刚好）</text>
</svg>
```

**无错误场次**：卡3 内容换一行「本场无新坑」，删掉规则区提示行。
**有超出项**：header 后加一行琥珀小字「✅+ 超出预期：xxx」→ 图标按 15 号字重排（本示例无超出行）。

---

## 模板二：机制链路图（横向箭头流）

回答「这次学会/验证了什么机制」。节点 3-5 个横排（主标=环节，副题=关键证据/产物），底部=实证输出。

**填写对照**：header=机制名 ｜ 每节点主标 ≤8 字、副题 ≤10 字 ｜ 箭头=传导方向 ｜ 底部条=本场实证输出一句（走通/验证结果）。副题必须是证据（如「audit 0 失败」），不是口号。

```svg
<svg viewBox="0 0 680 224" width="100%" role="img" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
<path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
</marker>
</defs>
<title>机制链路 · 变更校验执行链</title>
<text x="40" y="46" font-size="15" font-weight="500" fill="#1F2328">机制链路 · 变更校验执行链</text>

<rect x="40" y="84" width="132" height="64" rx="10" fill="#F6F8FA" stroke="#D0D7DE" stroke-width="1"/>
<text x="106" y="104" font-size="13" font-weight="500" fill="#1F2328" text-anchor="middle" dominant-baseline="central">变更触发</text>
<text x="106" y="124" font-size="11" fill="#57606A" text-anchor="middle" dominant-baseline="central">输入：改一列 schema</text>
<line x1="174" y1="116" x2="194" y2="116" stroke="#8C959F" stroke-width="1.5" marker-end="url(#arrow)"/>

<rect x="196" y="84" width="132" height="64" rx="10" fill="#F6F8FA" stroke="#D0D7DE" stroke-width="1"/>
<text x="262" y="104" font-size="13" font-weight="500" fill="#1F2328" text-anchor="middle" dominant-baseline="central">解析计划</text>
<text x="262" y="124" font-size="11" fill="#57606A" text-anchor="middle" dominant-baseline="central">增量：只算受影响</text>
<line x1="330" y1="116" x2="350" y2="116" stroke="#8C959F" stroke-width="1.5" marker-end="url(#arrow)"/>

<rect x="352" y="84" width="132" height="64" rx="10" fill="#F6F8FA" stroke="#D0D7DE" stroke-width="1"/>
<text x="418" y="104" font-size="13" font-weight="500" fill="#1F2328" text-anchor="middle" dominant-baseline="central">校验门禁</text>
<text x="418" y="124" font-size="11" fill="#57606A" text-anchor="middle" dominant-baseline="central">audit 0 失败</text>
<line x1="486" y1="116" x2="506" y2="116" stroke="#8C959F" stroke-width="1.5" marker-end="url(#arrow)"/>

<rect x="508" y="84" width="132" height="64" rx="10" fill="#DAFBE1" stroke="#1A7F37" stroke-width="1"/>
<text x="574" y="104" font-size="13" font-weight="500" fill="#1F2328" text-anchor="middle" dominant-baseline="central">apply 执行</text>
<text x="574" y="124" font-size="11" fill="#1A7F37" text-anchor="middle" dominant-baseline="central">终点：跑通</text>

<rect x="40" y="168" width="600" height="40" rx="10" fill="#DAFBE1" stroke="#1A7F37" stroke-width="1"/>
<text x="56" y="188" font-size="12" fill="#1A7F37" dominant-baseline="central">实证输出：变更后仅受影响分区重建，下游视图自动更新 · 全链路走通</text>
</svg>
```

**3 节点版**：节点宽 (600-2×24)÷3 = 184，坐标按 x=40、248、456 排，其余照抄。
**5 节点版**：节点宽 (600-4×24)÷5 ≈ 100，主标 ≤6 字、副题 ≤8 字，或拆两行。
**链路末节点** = 终点（成果态，绿底）；中间环节一律中性灰底，不抢终点语义。

---

## 模板三：里程碑进度图（阶段进度条）

回答「长期计划走到哪」。每阶段一行：名称 + 完成比例条 + 状态，底部=当前焦点。

**填写对照**：行=阶段名（≤8 字）｜ 条=已闭环绿 / 进行中蓝 / 待开始灰底 ｜ 右侧=「n/m 状态」｜ footer=当前里程碑 + 下一站。只画阶段级（课/场次不进此图，那是热力图的事）。

```svg
<svg viewBox="0 0 680 260" width="100%" role="img" xmlns="http://www.w3.org/2000/svg">
<title>里程碑进度 · 主题名</title>
<text x="40" y="46" font-size="15" font-weight="500" fill="#1F2328">里程碑进度 · 主题名</text>
<text x="640" y="46" font-size="12" fill="#57606A" text-anchor="end">月度回顾 · 2026-09</text>

<text x="40" y="84" font-size="13" fill="#24292F" dominant-baseline="central">阶段一 · 筑基</text>
<rect x="180" y="77" width="340" height="14" rx="7" fill="#EFF1F3"/>
<rect x="180" y="77" width="340" height="14" rx="7" fill="#1A7F37"/>
<text x="560" y="84" font-size="12" font-weight="500" fill="#1A7F37" dominant-baseline="central">3/3 已闭环</text>

<text x="40" y="118" font-size="13" fill="#24292F" dominant-baseline="central">阶段二 · 核心</text>
<rect x="180" y="111" width="340" height="14" rx="7" fill="#EFF1F3"/>
<rect x="180" y="111" width="112" height="14" rx="7" fill="#0969DA"/>
<text x="560" y="118" font-size="12" font-weight="500" fill="#0969DA" dominant-baseline="central">1/3 进行中</text>

<text x="40" y="152" font-size="13" fill="#24292F" dominant-baseline="central">阶段三 · 进阶</text>
<rect x="180" y="145" width="340" height="14" rx="7" fill="#EFF1F3"/>
<text x="560" y="152" font-size="12" fill="#57606A" dominant-baseline="central">0/3 待开始</text>

<rect x="40" y="198" width="600" height="44" rx="10" fill="#DDF4FF" stroke="#0969DA" stroke-width="1"/>
<text x="56" y="220" font-size="12" fill="#0969DA" dominant-baseline="central">当前：阶段二 · 里程碑 M2 —— apply 走通 + 增量执行 ｜ 下一站：M3 状态同步</text>
</svg>
```

**比例换算**：完成段宽 = 340 × (已完成数 ÷ 本阶段目标数)，取整（如 1/3 → 112）。进行中一律蓝（不是绿——没闭环不标成果）。
