---
name: ai-director-cinematography-standard
description: AI导演电影创作标准——镜头语言、灯光、色彩、构图、情绪组合的完整知识体系，用于为AI视频模型生成专业prompt
metadata: 
  node_type: memory
  type: reference
  source: e:\短视频\镜头.md（用户提供的基础文档）
  version: 2
  last_updated: 2026-07-01
  originSessionId: df487bb4-0e6c-4364-b64b-351739abfcd9
---

# AI导演电影创作标准 v2.0

> 基础文档来源：`e:\短视频\镜头.md` — 已有完整的焦距/景别/机位/运镜/情绪组合/五大模型体系

## 角色定位

作为「AI漫局导演」，我具备以下电影创作专业知识：
- 镜头选择（焦距、景别、机位、角度）
- 剪辑思路（平行/交叉/蒙太奇、转场设计）
- 拍摄角度（俯/仰/平/荷兰角/过肩/POV）
- 灯光设计（三点布光、光质、光向、光比）
- 色彩/调色（色温、色调、饱和度、色彩对比）
- 构图法则（三分法、负空间、引导线、画幅比）
- 运镜设计（推/拉/摇/移/升/降/甩/静止）
- 叙事结构（三幕式、节拍表、情绪曲线）

核心职责：**为其他AI模型（Sora/Runway/Kling/即梦/Midjourney等）撰写专业的创作提示词（prompt）**。

## 参考资源

完整基础文档位于：`e:\短视频\镜头.md`（包含十二个章节的完整镜头语言体系）

在每次创作时，应综合运用基础文档的全部知识 + 本文档补充的高级维度。

---

## 补充维度一：灯光设计体系

### 1.1 光的方向与情绪

| 光位 | 情绪效果 | 面部特征 | 中文提示词 | 英文提示词 |
|---|---|---|---|---|
| 正面光 | 平坦、坦诚、直面、无秘密 | 面部全亮，无阴影，立体感弱 | 正面光，面部均匀照亮，无阴影 | frontal lighting, flat even illumination, no shadows on face |
| 侧光（45°） | 立体、优雅、经典电影感 | 一侧亮一侧暗，鼻子投下经典阴影 | 45度侧光，经典伦勃朗光，面部立体分明 | 45-degree key light, Rembrandt lighting, sculpted facial shadows |
| 侧光（90°） | 分裂、对抗、双重人格、戏剧化 | 脸一半亮一半暗，明暗分割线 | 90度侧光，面部明暗分割，分裂感 | split lighting, half-lit half-shadow face, dramatic duality |
| 逆光 | 神秘、希望、剪影、神圣感 | 人物边缘发光，面部全暗或半暗 | 逆光，人物边缘光晕，剪影效果 | backlight, rim light halo, silhouette effect |
| 顶光 | 压迫、审判、疲惫、真相揭露 | 眼窝深陷，颧骨下方阴影 | 顶光，从头顶直射，眼窝深陷阴影 | top light, harsh overhead illumination, deep eye socket shadows |
| 底光 | 恐怖、邪恶、非人、超自然 | 面部下方照亮，阴影倒置（经典恐怖光） | 底光，从下方照射，面部阴影倒置 | under-lighting, light from below, inverted facial shadows, horror lighting |
| 蝴蝶光 | 美颜、迷人、经典好莱坞 | 鼻下蝴蝶形阴影，颧骨高光 | 蝴蝶光，正面高角度，鼻下蝴蝶形阴影 | butterfly lighting, high frontal key, butterfly shadow under nose |

### 1.2 光质（硬光 vs 柔光）

| 光质 | 情绪 | 提示词 |
|---|---|---|
| 硬光 | 紧张、真实、粗糙、阳刚、犯罪感 | hard light, sharp defined shadows, high contrast, harsh direct sunlight |
| 柔光 | 浪漫、温暖、安全、治愈、唯美 | soft diffused light, feathery shadows, low contrast, cloud-filtered daylight |

### 1.3 经典灯光组合配方

| 场景 | 灯光组合 | 提示词关键词 |
|---|---|---|
| 审讯/对峙 | 单顶光+硬光 | single overhead harsh light, deep shadows, interrogation room |
| 浪漫/约会 | 柔光+暖色侧光+浅景深 | soft warm side light, golden hour glow, romantic |
| 恐怖/惊悚 | 底光+硬光+荷兰角 | under-lighting, hard shadows, Dutch angle horror |
| 史诗/英雄 | 逆光+金色暖光+仰拍 | golden backlight rim, hero silhouette, low angle |
| 孤独/忧郁 | 单侧光+冷色+大量负空间 | single cold side light, large negative space, melancholic |

### 1.4 光比（key-to-fill ratio）

| 光比 | 情绪 | 提示词 |
|---|---|---|
| 低光比（1:1 ～ 2:1）| 柔和、安全、喜剧、日常 | low contrast ratio, soft fill light, even illumination |
| 中光比（3:1 ～ 4:1）| 经典电影感、戏剧化适中 | medium contrast ratio, classic cinematic modeling |
| 高光比（8:1+）| 紧张、悬疑、黑色电影、悲剧 | high contrast ratio, deep shadows, harsh noir lighting |

---

## 补充维度二：色彩/调色体系

### 2.1 色温的情绪语言

| 色温 | 情绪关键词 | 中文提示词 | 英文提示词 |
|---|---|---|---|
| 暖色调（3000K-4500K） | 温暖、回忆、安全、亲密、怀旧、浪漫 | 暖色调，金色光线，怀旧温暖的色彩基调 | warm color palette, golden tones, nostalgic warmth |
| 中性色调（5000K-5600K） | 客观、真实、纪录、当下 | 中性色调，自然日光色温，纪实感 | neutral color temperature, natural daylight, documentary realism |
| 冷色调（6000K-10000K） | 疏离、孤独、真相、科技、未来、恐惧 | 冷色调，青蓝色彩基调，冰冷疏离感 | cool color palette, cyan/blue tones, cold detachment |

### 2.2 经典色彩方案（Color Scheme）

| 方案 | 描述 | 情绪 | 提示词 |
|---|---|---|---|
| 青橙对比（Teal & Orange） | 好莱坞最经典配色 | 电影感、冲突、视觉冲击 | teal and orange color grade, cinematic color contrast |
| 单色调（Monochromatic） | 全片统一色调 | 压抑、梦幻、风格化 | monochromatic color palette, single hue throughout |
| 互补色（Complementary） | 色轮对立两色 | 冲突、张力、视觉冲击 | complementary color scheme, contrasting hues |
| 低饱和（Desaturated） | 接近黑白 | 冷酷、绝望、纪实、严肃 | desaturated muted colors, near-monochrome, bleak atmosphere |
| 高饱和（Saturated） | 色彩浓烈 | 青春、活力、超现实、梦幻 | highly saturated vivid colors, hyperreal color intensity |

### 2.3 色调的情绪配方

| 情绪 | 色彩配方 |
|---|---|
| 怀旧/回忆 | 暖金色调 + 轻微柔光 + 暗角 + 轻微胶片颗粒 → warm golden tones, soft glow, subtle vignette, light film grain |
| 孤独/忧郁 | 冷蓝/青色调 + 低饱和 + 大量阴影 → cool blue/cyan cast, desaturated, deep shadows |
| 恐惧/悬疑 | 绿/黄偏移 + 高对比 + 暗角 → green/yellow color shift, high contrast, heavy vignette |
| 浪漫/心动 | 粉/紫/暖金 + 柔光 + 浅景深 → pink/purple/warm gold, soft glow, shallow DOF |
| 史诗/宏大 | 高对比 + 青橙色调 + 深景深 → high contrast, teal-and-orange grade, deep DOF |

---

## 补充维度三：构图法则

### 3.1 核心构图规则

| 构图 | 描述 | 情绪 | 提示词 |
|---|---|---|---|
| 三分法 | 主体在画面1/3或2/3处 | 平衡、自然、经典 | rule of thirds composition, subject at intersection point |
| 中心构图 | 主体在画面正中央 | 庄重、对称、凝视、仪式感 | centered composition, subject dead center, symmetrical framing |
| 负空间 | 主体小，大量留白 | 孤独、思考、空间感 | negative space composition, small subject, vast empty surroundings |
| 引导线 | 线条引向主体 | 深度、命运、被牵引 | leading lines drawing eye to subject, deep perspective |
| 框架构图 | 通过门/窗/框看主体 | 窥视、隔离、被框住的命运 | frame within a frame, subject seen through doorway/window/mirror |
| 前景遮挡 | 前景虚化遮挡部分画面 | 偷窥、隐秘、层次感 | foreground occlusion, out-of-focus foreground element, voyeuristic |

### 3.2 画幅比（Aspect Ratio）

| 画幅比 | 情绪/质感 | 典型用途 | 提示词 |
|---|---|---|---|
| 2.35:1 / 2.39:1 | 宏大、史诗、电影感 | 电影大片、史诗叙事 | ultrawide cinematic aspect ratio 2.35:1, anamorphic widescreen |
| 1.85:1 | 经典电影、叙事 | 常规电影 | standard widescreen 1.85:1 |
| 16:9 (1.78:1) | 现代、日常、视频 | 短视频/现代视频 | standard 16:9 widescreen |
| 4:3 (1.33:1) | 复古、压抑、私密 | 旧时代、独立电影、压抑感 | 4:3 aspect ratio, vintage boxy framing, intimate constraint |
| 1:1 | 社媒、亲密、方正 | Instagram/品牌 | 1:1 square format, social media intimate framing |
| 9:16 | 竖屏、第一人称、手机感 | 竖屏短视频 | 9:16 vertical format, phone-screen native |

---

## 补充维度四：转场设计

> 转场分为两个层级：**基础转场**是剪辑的基本操作单元，是所有转场的底层实现；**视听语言转场**是在基础操作之上叠加情绪和风格的更高维度表达。

### 4.1 剪辑基础转场（5种基本操作）

> 硬切是主力——80%的场景用硬切。叠化、匹配剪辑是加分项，不是必选项。J-cut / L-cut 为后期配音阶段的剪辑指导。

| 转场 | 画面表现 | 导演意图 | 剧情匹配 |
|---|---|---|---|
| **硬切** (Hard Cut) | 直接切换，无过渡 | 干脆，节奏感强 | 快节奏剪辑、信息推进 |
| **叠化** (Dissolve) | 两画面交融溶解 | 时间流逝、回忆感 | 文艺片、情感戏 |
| **匹配剪辑** (Match Cut) | 形状/动作/色彩匹配连接 | 高级、隐喻、连贯 | 作者风格片、品牌片 |
| **J-cut** | 下一镜声音先进来（画面未切） | 自然引导、期待感 | 对话戏、场景切换 |
| **L-cut** | 上一镜声音继续留（画面已切） | 情绪延续、不舍感 | 离别戏、情感收束 |

**基础转场提示词：**

| 转场 | 中文提示词 | 英文提示词 |
|---|---|---|
| 硬切 | 硬切，无过渡，直接跳转 | abrupt hard cut, instant transition, no transition |
| 叠化 | 叠化过渡，两画面交融，时间流逝感 | dissolve transition, cross-dissolve, two shots blending |
| 匹配剪辑 | 匹配剪辑，形状/动作呼应连接 | match cut, visual echo between two unrelated scenes |
| J-cut | J-cut，声音先入，画面后切（配音阶段执行） | J-cut, audio preceding the visual cut (post-production) |
| L-cut | L-cut，画面已切，声音延续（配音阶段执行） | L-cut, audio lingering after the visual cut (post-production) |

### 4.1.1 转场选择速查表

| 场景 | 推荐转场 | 原因 |
|---|---|---|
| 快节奏MV / 动作片 | 硬切 + 甩镜 | 硬切保证节奏，甩镜制造视觉冲击 |
| 时间跳跃 / 回忆 | 叠化 | 画面交融暗示时间流逝 |
| 两段情绪相似 | 匹配剪辑 | 形状/动作呼应，强化情绪连贯 |
| 场景切换但情绪连续 | J-cut / L-cut | 声音与画面错位，情绪不中断 |
| AIGC 画面不连续 | 空镜过渡 + 声音桥接 | 用空镜遮掩生成画面的跳跃感 |
| 万能兜底 | 硬切 + 空镜 | 硬切最安全，空镜给情绪留白 |

### 4.1.2 转场禁忌事项（AI生成视频专项）

> AI生成的多个镜头之间容易出现不一致，以下是转场时必须规避的四条红线。

| 禁忌 | 说明 | 预防策略（提示词中强化） |
|---|---|---|
| ❌ 前后镜头人物长相不一致 | 同一角色在两个镜头里变成不同的人 | 在每段prompt中重复角色外貌描述，保持一致性关键词 |
| ❌ 前后镜头空间逻辑断裂 | 上一镜人在室内，下一镜突然在室外，无交代 | 用空镜/环境全景过渡，或明确标注"同一空间，角度切换" |
| ❌ 前后镜头光线/色调跳变 | 暖黄光突然变冷蓝光，破坏视觉连贯 | 统一标注全片色温基调，每镜重申灯光方向与色调 |
| ❌ 运动方向突然反转 | 人物上一镜向右走，下一镜突然向左 | 标注运动轴线，避免越轴（除非故意制造不安感） |

### 4.2 视听语言转场（情绪级）

> 以下转场是在基础操作之上叠加情绪冲击和风格表达的更高维度应用。

| 转场 | 情绪 | 提示词 |
|---|---|---|
| 淡入淡出（Fade） | 柔和、时间流逝、开始/结束 | slow fade to black/white, time passage |
| 甩镜转场（Whip Pan） | 速度、能量、节奏冲击 | whip pan transition, motion blur bridge between scenes |
| 越轴转场 | 打破规则、不安、冲突 | axis jump cut, disorienting transition |
| 相似形转场（Shape Match）| 精致、设计感 | shape-match transition, visual echo cut |

---

## 补充维度五：综合创作工作流

### 5.1 导演决策树（接到需求后的思考顺序）

```
1. 故事 → 三幕式结构分配时长
2. 角色 → 动机四件套（渴望/需要/障碍/转变）
3. 情绪 → 目标情绪词 → 查情绪组合配方表
4. 景别 → 叙事节奏公式（入场三段式/情绪收紧公式）
5. 运镜 → 选五大模型之一（聚焦/抽离/跟随/扫视/爆发）
6. 机位 → 角度决策（根据权力关系和代入感）
7. 焦段 → 镜头选择（根据空间感和情绪质感）
8. 灯光 → 光位+光质+光比（根据场景氛围）
9. 色彩 → 色温+色调方案（根据情绪基调）
10. 构图 → 构图规则+画幅比（根据平台和美学）
11. 转场 → 连接方式（根据节奏需求）
12. 输出 → 填写脚本模板 → 生成中英文prompt
```

### 5.2 不同平台的镜头策略

| 平台 | 特点 | 镜头策略 |
|---|---|---|
| 横屏电影感 | 16:9或更宽，故事驱动 | 深景深、大景别跨度、缓推拉为主 |
| 竖屏短视频 | 9:16，3秒定生死 | 大特写开局、强节奏运镜、钩子前置 |
| 品牌广告 | 产品+情绪并行 | 微距产品+情绪镜头交叉、灯光精致 |
| 剧情短片 | 叙事为核心 | 三幕式完整、角色动机驱动景别变化 |

---

## 版本记录

- v2.1 (2026-07-02)：重构转场设计维度——新增「剪辑基础转场」5种（硬切/叠化/匹配剪辑/J-cut/L-cut），配套「转场选择速查表」和「转场禁忌事项」；原有转场归入「视听语言转场（情绪级）」，形成两层级转场体系
- v2.0 (2026-07-01)：在基础文档（镜头.md）之上补充了灯光设计体系、色彩/调色体系、构图法则（含画幅比）、转场设计、综合创作工作流五个维度
- v1.0：基础文档十二章节，包含焦距/景别/机位/运镜/情绪组合/剪辑/三幕式/角色动机/五大模型/脚本模板
