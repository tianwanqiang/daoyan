# 镜头语言 → AI视频生成镜头控制提示词脚本

> 基于课件内容整理，可直接用于 Sora / Runway / Kling / 即梦 / Midjourney 视频等模型的 prompt 撰写

---

## 一、焦距与视角类镜头（lens / focal length）

| 镜头 | 情绪/质感 | 中文提示词 | 英文提示词 |
|---|---|---|---|
| 广角镜头 | 压迫、卷入、临场、宏大、不安 | 广角镜头，强透视压迫感，临场卷入感 | wide-angle lens, 16-24mm, strong perspective distortion, immersive, claustrophobic, epic scale |
| 标准镜头 | 真实、克制、平视、信任、日常 | 标准镜头，平视视角，真实自然，无夸张畸变 | standard lens, 35-50mm, eye-level, naturalistic, undistorted, documentary feel |
| 中长焦人像镜头 | 凝视、亲密、暧昧、精致、被审视 | 中长焦人像镜头，浅景深，背景柔和虚化，凝视感 | mid-telephoto portrait lens, 85mm, shallow depth of field, creamy bokeh, intimate gaze |
| 长焦/超长焦镜头 | 宿命、孤立、窥视、史诗、不可抗拒 | 超长焦镜头，压缩空间感，远距离窥视视角 | telephoto/super-telephoto lens, 200-600mm, compressed perspective, voyeuristic distant framing |
| 鱼眼镜头 | 迷幻、超现实、混乱、青春、极限 | 鱼眼镜头，强烈球面畸变，迷幻超现实视角 | fisheye lens, extreme barrel distortion, surreal psychedelic perspective |
| 微距镜头 | 精致、私密、被忽视的世界、超细节、感官放大 | 微距镜头，极致细节特写，质感纹理清晰可见 | macro lens, extreme close-up detail, hyper-textured surface, sensory amplification |
| 移轴镜头 | 玩具感、上帝视角、抽离、童趣、模型化现实 | 移轴镜头，上帝视角俯瞰，画面呈微缩模型质感 | tilt-shift lens, god's-eye overhead view, miniature diorama effect |

**典型应用场景速查：**
- 广角：狭窄走廊推进、近身打斗、史诗大场面、第一人称追逐、恐怖片密闭空间
- 标准：双人对话、生活流叙事、纪录片、家庭剧、文艺片日常戏
- 中长焦人像：人物特写、情感独白、暗恋戏、肖像广告、时尚MV
- 长焦：雪原孤行、狙击视角、追逐戏远观、史诗结尾、命运感场面
- 鱼眼：滑板/冲浪极限运动、迷幻药物体验、梦境、嘻哈MV、儿童视角
- 微距：化妆品广告、美食广告、自然纪录片、情绪空镜、产品特写
- 移轴：城市俯瞰、节日活动、品牌广告创意片头、节奏明快的MV

### 光圈与景深核心规律

- **光圈用 f 值表示**：f 值越小 → 光圈越大 → 进光量越多 → 画面越亮 → 景深越浅（背景虚化强）
- f 值越大 → 光圈越小 → 进光量越少 → 画面越暗 → 景深越深（前后景都清晰）
- **速记口诀**："小光圈大景深，大光圈小景深"（因为 f 值的数学本质是分母）
- **焦距规律**：焦距越长景深越浅；焦距越短景深越深
  - 经典质感公式：**长焦 + 大光圈 = 极致浅景深**（人像虚化）；**广角 + 小光圈 = 极致深景深**（风光全清晰）

---

## 二、景别——电影工业的6级框架（shot size）

> 景别是镜头决策的第一步：先决定"框多少"，再决定"从哪里框"。景别不是孤立选择的，是按**叙事节奏**组合使用的。

| 景别 | 英文 | 核心定义 | 情绪关键词 | 导演意图 | 中文提示词 | 英文提示词 |
|---|---|---|---|---|---|---|
| 远景 | Extreme Long Shot | 人物小到几乎看不见，画面90%是环境 | 史诗、孤立、宿命、宏大、世界感 | 不是讲一个人，是讲一个人和这个世界的关系 | 远景，人物渺小，环境占据画面绝大部分，宏大世界感 | extreme long shot (ELS), tiny figure in vast environment, epic scale, world-building |
| 全景 | Full Shot | 从头到脚完整呈现，环境与人物各占一半权重 | 平等、纪实、动作完整、关系展示 | 让观众认识"她是谁、她在哪里" | 全景，人物全身入画，环境与人物权重相当，清晰展示动作关系 | full shot (FS), full body visible head to toe, equal weight of subject and environment |
| 中景 | Medium Shot | 腰部以上，肢体语言可读，环境开始退后 | 对话、叙事、社交距离、信息适中 | 让观众感受到"她在做什么、她的状态" | 中景，腰部以上入画，肢体语言清晰，叙事推进镜头 | medium shot (MS), waist up, body language readable, narrative workhorse |
| 近景 | Medium Close-Up | 胸部以上，面部表情成为主角，环境大幅压缩 | 情绪、表演、个人空间、专注 | 观众的注意力被强制收紧到她的内心 | 近景，胸部以上，面部表情主导画面，情绪戏标配 | medium close-up (MCU), chest up, face becomes dominant, emotional intimacy |
| 特写 | Close-Up | 脸几乎填满整个画面，环境完全消失 | 爆发、揭示、心理放大、真相时刻 | 真相时刻，观众与她贴脸，呼吸可闻 | 特写，面部充满画面，环境消失，情感高潮瞬间 | close-up (CU), face fills the frame, environment vanishes, truth moment |
| 大特写 | Extreme Close-Up | 只有眼睛，连脸都裁掉了 | 超现实、压迫、感官放大、心理崩溃 | 观众进入了她的潜意识 | 大特写，仅眼睛/局部细节填满画面，心理崩溃或决定性瞬间 | extreme close-up (ECU), only eyes or single detail fills frame, entering the subconscious |

### 典型应用场景

| 景别 | 典型场景 |
|---|---|
| 远景 | 开场建立环境、人物走向远方、史诗大场面、命运感结尾 |
| 全景 | 人物动作戏（舞蹈/打斗/奔跑）、双人关系展示、纪录片人物全身 |
| 中景 | 双人对话、采访、剧情推进常规镜头（好莱坞标准对话戏的"过肩中景"） |
| 近景 | 演员情绪戏、独白、人物反应镜头 |
| 特写 | 决定性瞬间的反应、关键道具揭示、情感高潮 |
| 大特写 | 心理崩溃瞬间、关键细节揭示（指纹/字条/表情纹）、风格化作者电影 |

### 景别的叙事节奏公式

> **景别不是孤立选择的，是按"叙事节奏"组合使用的**

```
标准入场三段式：
远景（这是哪里）→ 中景（谁在这里）→ 特写（他在想什么）

情绪收紧公式：
全景 → 中景 → 近景 → 特写（逐级收窄，情绪逐步升温）

震撼对比公式：
大特写（极度私密） → 切远景（世界感）→ 制造空间上的情绪冲击
```

### 景别与情绪深度的关系

```
远景 ──── 世界    （观众是旁观者，感受宏大）
全景 ──── 行动    （观众看到完整的人，理解其处境）
中景 ──── 关系    （观众开始关心人物）
近景 ──── 情绪    （观众开始感受人物内心）
特写 ──── 真相    （观众与人物合一，无处遁形）
大特写 ── 潜意识  （观众进入人物的心理深处）
```

### 景深的情绪语言

| 景深类型 | 情绪关键词 | 中文提示词 | 英文提示词 |
|---|---|---|---|
| 浅景深 | "内心"，主体突出，私密、聚焦情绪 | 浅景深，大光圈（f/1.4-f/2.8），背景奶油般虚化，主体清晰突出 | shallow depth of field, wide aperture f/1.4-f/2.8, creamy bokeh background, subject in sharp focus |
| 中等景深 | "关系"，人物与环境兼顾 | 中等景深（f/4-f/8），主体与周边环境均保持可辨识清晰度 | medium depth of field, f/4-f/8, subject and surrounding environment both reasonably sharp |
| 深景深 | "世界"，史诗感、宏大、人与天地的关系 | 深景深，小光圈（f/11-f/22），前景中景远景全部清晰，史诗全景感 | deep depth of field, narrow aperture f/11-f/22, foreground midground and background all in sharp focus, epic panoramic clarity |

> 浅景深是"内心"，中等景深是"关系"，深景深是"世界"

---

## 三、机位与角度类镜头（camera angle）

| 镜头 | 情绪/质感 | 中文提示词 | 英文提示词 |
|---|---|---|---|
| 俯拍镜头 | 渺小、无助、被审视、上帝视角、宿命 | 俯拍镜头，从高处向下俯视，人物显得渺小无助 | high-angle shot, looking down, subject appears small and vulnerable |
| 仰拍镜头 | 威严、强大、英雄感、压迫、敬畏 | 仰拍镜头，从低处向上仰视，强调威严与英雄气概 | low-angle shot, looking up, emphasizing power and heroism |
| 荷兰角（倾斜镜头） | 失衡、混乱、精神错乱、危险临近、不安 | 荷兰角倾斜构图，画面失衡，制造紧张不安感 | Dutch angle, tilted frame, off-kilter composition, unease and tension |
| 平视镜头 | 平等、对话、客观、共情、真实 | 平视镜头，与人物视线齐平，客观平等的纪实视角 | eye-level shot, neutral and objective framing, documentary realism |
| 过肩镜头 | 对峙、对话、视角代入、关系张力 | 过肩镜头，越过前景人物肩膀拍摄对话对象 | over-the-shoulder shot, framing the other subject past a foreground shoulder |
| 第一人称 | 代入、临场、紧迫、私密、第一人称体验 | 第一人称视角，模拟角色双眼所见 | POV shot, first-person perspective, simulating the character's own eyes |

**典型应用场景速查：**
- 俯拍：人物在巨大空间里的孤独感、群体场面俯瞰、悬疑片受害者视角、品牌片宏观叙事
- 仰拍：英雄登场、反派威慑、建筑宏伟感、运动员胜利时刻、领导力品牌片
- 荷兰角：恐怖片心理崩溃、动作片打斗中的眩晕、悬疑片真相揭露、超现实MV、反派出场
- 平视：访谈、对话戏、纪录片、人物介绍、真诚向品牌片
- 过肩：双人对话戏、谈判戏、对峙戏、采访、约会场景
- 第一人称：恐怖片追逐、第一人称游戏化叙事、Vlog、品牌沉浸式体验片

---

## 四、运镜方式（camera movement）

> 运镜是时间维度上的情绪设计。镜头的运动方向和速度，决定观众的心理被"推向"还是"拉离"主体。

| 运镜名 | 定义 | 情绪编码 | 导演潜台词 | 中文提示词 | 英文提示词 |
|---|---|---|---|---|---|
| 推镜头 | 机位主动向主体逼近 | 揭示、聚焦、心理深入、悬念递进、情绪逼近 | "注意，重点来了，看清楚这个人/这个细节。" | 缓慢推进，镜头向主体逼近，画面逐渐收窄聚焦 | slow dolly in, camera pushing toward subject, frame tightening, emotional compression |
| 拉镜头 | 机位主动远离主体 | 抽离、揭示环境、孤立感、收尾感、命运全景 | "等等，你以为你看到的就是全部？我现在让你看更大的真相。" | 缓慢拉远，画面从局部扩展到整体环境，揭示宏观全景 | slow dolly out / pull back, frame expanding from detail to full environment, revealing wider world |
| 摇镜头 | 机位不动，镜头水平左右转动，模拟人转头观察 | 展示、引导、扫视、连接、信息扩展 | "别急，我带你看看这边发生了什么。" | 水平摇镜，机位固定，镜头缓慢横向扫视环境 | pan shot, static camera position, slow horizontal swivel, scanning the environment |
| 移镜头 | 机位本身平行移动（区别于摇：摇是转动，移是平移） | 沉浸、跟随、流动、节奏、并行陪伴 | "我和你一起走，你看到的世界就是我看到的世界。" | 横向移镜，机位平行移动跟随主体，营造流动陪伴感 | tracking shot / lateral dolly, camera moving parallel alongside subject, immersive accompaniment |
| 升镜头 | 机位垂直向上移动，视野从地面被托举到高处 | 释放、超越、希望、宏大、上帝视角浮现 | "故事到这里要变大了，我们要看到更高的维度。" | 升镜，机位垂直向上移动，视野逐渐升至高空，格局打开 | crane up / boom up, camera rising vertically, viewpoint ascending, God's-eye perspective emerging |
| 降镜头 | 机位垂直向下移动，视野从高处被压向地面或具体目标 | 坠落、压迫、聚焦、命运降临、揭示局部 | "我先让你看到全貌，然后我要把你的视线锁定到某一个点。" | 降镜，机位垂直向下移动，从全景俯视下沉聚焦至目标 | crane down / boom down, camera descending vertically, locking onto a specific target |

### 运镜速度与情绪的关系

| 速度 | 情绪效果 | 典型用法 |
|---|---|---|
| 极慢推/拉 | 悬念积累、冥想感、不可察觉的威胁 | 恐怖片、心理剧、顿悟场景 |
| 匀速中速 | 叙事流动、时间流逝、陈述感 | 人物介绍、环境展示、旁白段落 |
| 急推/甩 | 冲击、愤怒、突发事件 | 动作片打斗、惊吓时刻、情绪爆发 |
| 静止（zero movement） | 凝固、对峙、绝对的权重感 | 对话高潮、决定时刻、定格情绪 |

### 经典运镜组合公式

| 场景需求 | 运镜组合 | 提示词 |
|---|---|---|
| 情绪收紧（焦虑/悬疑） | 缓慢推镜 + 静止落幅 | slow push in, hold on close-up |
| 故事放大（史诗/升华） | 升镜 + 拉镜 | crane up combined with pull back, expanding world |
| 并行叙事（跟随人物） | 移镜 + 匀速跟拍 | lateral tracking shot, steady pace alongside character |
| 揭示真相（从全局到局部） | 降镜 + 推镜 | crane down into slow push, locking onto target |
| 时间流逝/场所扫视 | 摇镜 + 匀速横移 | slow pan across space, scanning environment |

## 视听语言核心：静与动的三种关系

> **运动决定情绪流动**——AI生成视频时，"动"与"静"的切换节奏比运动方向本身更能决定观众的情绪反应。

**关系一：静 → 动的爆发**

从绝对静止突然爆发为剧烈运动，制造戏剧冲击。

情绪效果：震惊、惊吓、能量释放、叙事转折点

典型场景：恐怖片惊吓瞬间、动作片打斗开场、悬疑片真相揭露

提示词：`static hold, then sudden explosive movement — crash zoom / whip pan / rapid handheld`

---

**关系二：动 → 静的收束**

从持续运动突然收束为静止，制造命运感与凝固感。

情绪效果：宿命、定格、情绪重量落地、无处可逃

典型场景：人物追逐后的最终定格、战斗结束后的废墟凝视、决定性瞬间的静止

提示词：`continuous motion then abrupt freeze — hard stop on close-up, stillness after chaos`

---

**关系三：静中有动 / 动中有静（最高级的运动设计）**

两种形态：

- **静态运动**：镜头本身静止，但画面内部有运动感——如长焦压缩下人物缓步前行，背景几乎不动，观众能感到"时间在流逝"

- **动态静止**：镜头在运动，但主体相对静止——如手持跟拍人物站在原地不动，但镜头微微抖动，制造"活的静止"

情绪效果：静态运动→时间感、宿命感、冥想；动态静止→真实感、脆弱、临场呼吸

提示词：
- 静态运动：`static camera, subject slowly moving through compressed telephoto space, time passing`
- 动态静止：`handheld subtle drift, subject stationary, camera breathing gently around them`

---

## 五、曝光与景深控制（aperture / depth of field）

### 实操经验
| 景深类型 | 静态图出彩度 | 视频出彩度 | 提示词策略 |
|---|---|---|---|
| 浅景深 | ★★★★★ 最容易出彩 | ★★★★ | 直接写 "浅景深/shallow depth of field" 即可，AI模型天然偏好 |
| 中等景深 | ★★★★ | ★★★★ | 写清楚主体与环境关系即可 |
| 深景深 | ★★★ AI模型偏好浅景深，需强调提示词 | ★★★ | 需要**反复强调**关键词，如重复 "deep depth of field, everything in focus, sharp foreground to background"，并加入小光圈数值（f/11、f/16、f/22）来强化效果 |

> 提示：因为训练数据中"电影感"图片（大光圈虚化）占比高，AI 模型默认倾向浅景深；如需深景深效果，建议在提示词中多次强调并明确给出小光圈数值。

---

## 六、速用对照速查表

| 想表达的情绪 | 推荐镜头组合 |
|---|---|
| 私密/内心 | 中长焦人像 + 浅景深 + 大光圈 + 平视/过肩 |
| 关系/对话 | 标准镜头 + 中等景深 + 平视/过肩 |
| 史诗/宏大/世界感 | 广角 + 深景深 + 小光圈 + 俯拍/仰拍 |
| 威严/英雄 | 仰拍 + 广角 |
| 渺小/被支配 | 俯拍 + 广角 |
| 失衡/恐惧 | 荷兰角 + 鱼眼/广角 |
| 临场/代入 | 第一人称(POV) + 广角 |
| 精致/产品细节 | 微距镜头 + 浅景深 |
| 抽离/玩具感 | 移轴镜头 + 俯拍 |

---

## 七、情绪组合配方——情绪不是单帧出来的，是组合出来的

> 核心思想：一个镜头只能呈现画面，多个镜头的组合才能制造情绪。

| 情绪 | 镜头组合公式 | 为什么这样组合 | 提示词关键词 |
|---|---|---|---|
| 暴躁 / 愤怒 | 急推特写 + 甩镜转场 + 低角度仰拍 | 急推制造逼近压迫，甩镜击穿节奏，仰拍放大威胁 | crash zoom, whip pan transition, low-angle shot, aggressive framing |
| 忧郁 / 孤独 | 长焦特写 + 大远景空镜 + 缓慢拉远 | 长焦把人物压扁孤立，远景揭示人渺小，拉远制造抽离感 | telephoto isolation, wide empty establishing shot, slow pull back |
| 舒缓 / 治愈 | 平视中景 + 自然横移 + 柔光全景 | 平视让观众放松，横移制造时间流逝感，全景给情绪留白 | eye-level medium shot, natural dolly side, soft diffused lighting, wide panoramic |
| 紧张 / 悬疑 | 长焦窥视 + 缓慢推进 + 反应特写 | 长焦制造"被看"的窥视感，缓推让悬念递增，反应特写引爆心理 | telephoto voyeur shot, slow creeping push, reaction close-up |
| 史诗 / 震撼 | 极广角仰拍 + 缓慢升镜 + 大远景 | 仰拍制造威严，升镜打开格局，远景展示宏大世界 | extreme wide-angle low angle, slow crane up, epic wide establishing |
| 暧昧 / 亲密 | 浅景深特写 + 过肩近景 + 慢动作横移 | 浅景深孤立两人世界，过肩制造对视张力，慢动作放大每一个眼神 | shallow DOF close-up, over-the-shoulder, slow motion lateral dolly |
| 梦幻 / 超现实 | 鱼眼广角 + 升降摇 + 慢动作特写 | 鱼眼制造空间扭曲，升降摇打破地心引力，慢动作让现实失真 | fisheye distortion, vertical boom pan, slow motion surreal close-up |
| 荒凉 / 绝望 | 大远景空镜 + 静止长镜头 + 顶光俯拍 | 远景显出世界的空，静止让时间凝固，俯拍把人压成一个点 | vast empty wide shot, static long take, overhead top-down shot, harsh top light |

---

## 八、三大剪辑叙事逻辑（镜头组合的结构方式）

| 组合逻辑 | 一句话定义 | 情绪效果 | 经典AIGC应用 | 提示词写法 |
|---|---|---|---|---|
| 平行剪辑 | 两条线同时进行、互不相交 | 对比、并行、关系隐喻 | 男女主同时起床准备约会 / 品牌产品在不同人手中的使用 | 分别描述两个场景，用"同时/meanwhile"连接 |
| 交叉剪辑 | 两条线交替推进、终将相遇 | 紧张、悬念、终极冲突 | 追凶 / 救援 / 倒计时品牌广告 | 描述两场景交替切换，明确"即将相遇"的临界感 |
| 蒙太奇 | 多个不连续画面快速串联 | 时间压缩、情绪堆叠、概念表达 | 主角成长历程 / 品牌产品诞生过程 / MV情绪段落 | 列出多个强意象画面，用快切节奏串联 |

> 记忆口诀：平行 = "与此同时"；交叉 = "两边马上要撞上了"；蒙太奇 = "让你瞬间明白这段时间发生了什么"

---

## 九、三幕式故事结构——一切故事的元结构

> 任何AI视频需求，先套三幕式结构，再填镜头

| 幕 | 时长占比 | 叙事任务 | 情绪基调 |
|---|---|---|---|
| 第一幕 — 建立 | 25% | 这是谁？在哪里？发生了什么？ | 让观众关心 |
| 第二幕 — 对抗 | 50% | 主角遭遇障碍并努力 | 让观众紧张 |
| 第三幕 — 解决 | 25% | 决战与回响 | 让观众释放 |

### 不同时长的三幕式压缩公式

| 时长 | 结构分配 |
|---|---|
| 15秒短视频 | 3秒钩子 + 9秒展开 + 3秒落点 |
| 60秒短片 | 15秒建立 + 30秒对抗 + 15秒收束 |
| 3分钟品牌片 | 45秒痛点 + 90秒介入 + 45秒升华 |

### 3秒钩子四件套（开场前3秒抓住观众）

| 类型 | 示例 |
|---|---|
| 悬念型 | "为什么她每天凌晨3点准时醒来？" |
| 反差型 | 豪宅大门打开，里面只有一张折叠床 |
| 情绪型 | 一只手颤抖着按下电话拨号键 |
| 声明型 | "这是我离婚的第367天" |

---

## 十、角色动机四件套——情绪曲线四段式

> 动机直接决定镜头选择。写AI视频前，先明确角色的四件套：
> - **渴望**：他想要什么（表面目标）
> - **需要**：他真正需要什么（深层成长）
> - **障碍**：什么挡着他（外部/内部）
> - **转变**：故事结束时他变成了谁

### 动机 → 镜头配方对应表

| 角色处境 | 镜头配方 | 情绪目的 |
|---|---|---|
| 追求渴望时 | 中景跟拍 + 急推 + 强光（清晰果断） | 传递目标感与行动力 |
| 遭遇障碍时 | 长焦特写 + 低角度仰拍 + 阴影压顶（压迫孤立） | 放大压力与困境 |
| 顿悟需要时 | 缓慢拉远 + 升镜 + 自然光（抽离揭示） | 制造内省与觉醒感 |
| 完成转变时 | 极浅景深特写 + 静止 + 柔光（心跳凝固） | 凝固情绪最高点 |

---

## 十一、综合运用——五大情绪展示模型

> 掌握基础镜头知识后，真正的导演思维是把景别、运镜、角度、景深整合成一个**完整的情绪运动方案**。这五种模型是最经典的综合运用范式，每种都有明确的情绪目标、运动逻辑和可直接使用的提示词脚本。

---

### 模型一：聚焦式（Focusing）—— 从外到内的情绪收紧

**核心逻辑：** 像一只无形的手按着脖子，把观众推进一个真相。

| 维度 | 内容 |
|---|---|
| 运动模式 | 缓慢推进 / 缓慢变焦 / 持续向主体逼近 |
| 情绪流动 | 观众注意力从环境一步步被引导到主体核心 |
| 典型场景 | 悬念揭示前、情绪高潮前、品牌Slogan出现前的铺垫、人物心理转变临界点 |

**完整提示词脚本（15秒律师做决定）：**
```
镜头：50mm标准镜头，匀速直线缓慢推进
起幅：中年男性坐在昏暗律师事务所皮椅的中景，双手交握放在膝上，神情凝重
中段：镜头匀速缓向他面部推进，背景书架与窗外暮光逐渐被推出画框
落幅：他眼睛的特写，瞳孔反射最后一缕暮光，眼神从沉默转为决绝
节奏：前2秒起幅静止 → 中段11秒匀速推进 → 后2秒特写定格

slow steady dolly push in, 50mm lens, medium shot to extreme close-up on eyes,
background gradually excluded, emotional compression throughout 15 seconds
```

---

### 模型二：抽离式（Pulling Away）—— 从内到外的命运浮现

**核心逻辑：** 像从一个梦里被慢慢拽出来，才看清自己所处的世界有多大。

| 维度 | 内容 |
|---|---|
| 运动模式 | 缓慢后拉 / 缓慢升起 / 持续远离主体 |
| 情绪流动 | 观众视野从主体内心被拉开，逐渐看到主体所处的宏大世界 |
| 典型场景 | 电影结尾的抽离感、史诗片命运感总结、孤独感极致呈现、品牌片格局打开 |

**完整提示词脚本（15秒孤独女孩）：**
```
镜头：35mm镜头，垂直缓慢升起并后拉的复合运动
起幅：女孩独自坐在巨大空旷宴会厅地板正中央近景，低头怀抱一束枯萎玫瑰
中段：镜头同时垂直升起与水平后拉，依次揭示空荡舞池、水晶吊灯与镜面墙、整个空无一人的宴会厅
落幅：高空大远景，女孩成为画面中央的白色小点，被巨大空旷完全包围
节奏：前2秒近景情绪建立 → 中段11秒匀速升拉 → 后2秒高空俯拍落幅

35mm lens, simultaneous crane up and pull back, near to extreme long shot,
revealing vast empty ballroom around lone figure, fate and isolation emerging
```

---

### 模型三：跟随式（Following）—— 与主体共呼吸

**核心逻辑：** 像被牵着手一起走过这段时空，观众成为同行者而非旁观者。

| 维度 | 内容 |
|---|---|
| 运动模式 | 横移跟拍 / 手持跟拍 / 第一人称POV / 持续与主体保持平行 |
| 情绪流动 | 观众与主体共享视点，产生真实陪伴感 |
| 典型场景 | 人物行走戏、长镜头叙事、追逐戏、沉浸式纪录片、品牌片"陪伴感"段落 |

**完整提示词脚本（15秒雨中男孩）：**
```
镜头：35mm镜头，与主体平行同步横移跟拍，机位距主体约2米
起幅：穿黄色雨衣的小男孩在雨后湿漉漉的老式胡同入口入画，踩着水洼前进
中段：镜头与男孩保持完全平行速度横移，男孩始终位于画面右三分线，
     背景青砖墙、晾衣绳、老旧电线杆持续向左流动
落幅：男孩走到胡同尽头一扇敞开的木门前停下，回头望向镜头方向露出微笑
节奏：前1秒主体入画 → 中段13秒持续平行跟随 → 后1秒主体停下回望

35mm lens, lateral tracking shot parallel to subject at 2m distance,
subject held at rule-of-thirds right, background flowing left, companionship throughout
```

---

### 模型四：扫视式（Scanning）—— 信息的横向铺陈

**核心逻辑：** 像在阅读一行流动的文字，信息密度极高，观众被引导依次接收。

| 维度 | 内容 |
|---|---|
| 运动模式 | 横摇 / 升降摇 / 弧形环绕 |
| 情绪流动 | 观众视线被引导扫过一片信息海洋，信息密度极高 |
| 典型场景 | 环境介绍、群像展示、产品阵列呈现、复杂场面的依次叙事 |

**完整提示词脚本（15秒中医药铺群像）：**
```
镜头：35mm镜头，固定机位水平向右匀速摇动
起幅：老式中医药铺内景全景，白发老中医正在称药
中段：镜头从老中医开始匀速向右水平摇动，依次扫过抓药的伙计、咳嗽的等候老妇人、
     "悬壶济世"牌匾、煎药炉旁打盹的小学徒，共5个信息节点
落幅：最右侧店门口望向街上的小女孩背影，她站在门槛上望向画外的繁华街市
节奏：前2秒起幅 → 中段11秒匀速横摇依次展示5个信息点 → 后2秒落幅

35mm lens, fixed position slow pan right, scanning across multiple subjects in sequence,
high information density, each figure revealed one by one, ending on lone figure at threshold
```

---

### 模型五：爆发式（Explosive）—— 节奏的瞬间击穿

**核心逻辑：** 像被人拍了一下肩膀猛然回头，运动的冲击瞬间击穿观众的注意力。

| 维度 | 内容 |
|---|---|
| 运动模式 | 甩镜 / 急推急拉 / 急速变焦（Crash Zoom）/ 急速旋转 |
| 情绪流动 | 观众被运动瞬间冲击击穿，节奏感与冲击力极强 |
| 典型场景 | 转场、动作戏冲击点、喜剧反应镜头、音乐节奏点视觉爆发、风格化作者电影 |

**完整提示词脚本（15秒人物转变爆发）：**
```
镜头：35mm镜头，前段固定机位，中段极速横向甩动，后段固定机位
起幅：穿白T恤的年轻男性站在白色简约背景前中景，正面对镜头露出微笑（静止5秒）
中段：镜头突然向右极速甩动，产生强烈横向运动模糊形成彩色色块流动效果（1.5秒）
落幅：同一男性，已变身黑色西装站在城市霓虹夜景天台前，神情冷峻凝视远方（8.5秒）
节奏：前5秒起幅静止建立人物 → 中段1.5秒爆发甩镜击穿 → 后8.5秒落幅停留新场景
      爆发式不对称节奏——长静止蓄力，极短爆发，长落幅余震

35mm lens, 5s static hold → 1.5s explosive whip pan with motion blur → 8.5s new scene hold,
asymmetric rhythm: long buildup, instant explosive transition, long aftermath
```

---

### 五大模型对比速查

| 模型 | 情绪方向 | 核心运动 | 最适用场景 | 节奏特征 |
|---|---|---|---|---|
| 聚焦式 | 外→内收紧 | 缓慢推进 | 悬念揭示、心理转变 | 匀速渐进，结尾定格 |
| 抽离式 | 内→外扩展 | 后拉+升镜 | 结尾命运感、孤独极致 | 匀速渐远，落幅宏大 |
| 跟随式 | 并行陪伴 | 横移同步 | 行走叙事、沉浸纪录 | 匀速持续，始终保持距离 |
| 扫视式 | 横向铺陈 | 横摇扫描 | 群像介绍、信息展示 | 匀速流动，多信息节点 |
| 爆发式 | 瞬间击穿 | 甩镜/急推 | 转场、冲击点、节奏爆发 | 长静止+极短爆发+长余震 |

---

## 十二、完整脚本填写模板（综合所有维度）

> 每次接到AI视频需求，先填这张表，再写提示词

```
【故事结构】
- 幕：第一幕建立 / 第二幕对抗 / 第三幕解决
- 时长分配：___秒建立 + ___秒对抗 + ___秒解决
- 开场钩子类型：悬念型 / 反差型 / 情绪型 / 声明型

【角色动机四件套】
- 渴望（表面目标）：___
- 需要（深层成长）：___
- 障碍（外部/内部）：___
- 转变（结束时变成了谁）：___

【当前场景处于第几阶段】
- □ 追求渴望 → 中景跟拍+急推+强光
- □ 遭遇障碍 → 长焦特写+仰拍+阴影
- □ 顿悟需要 → 缓拉+升镜+自然光
- □ 完成转变 → 浅景深特写+静止+柔光

【镜头规格】
- 焦段：广角 / 标准 / 中长焦人像 / 长焦 / 鱼眼 / 微距 / 移轴
- 机位：俯拍 / 仰拍 / 平视 / 荷兰角 / 过肩 / 第一人称(POV)
- 景深：浅（f/1.4-2.8）/ 中（f/4-8）/ 深（f/11-22）

【运镜方式】
- 推进 / 拉远 / 横移 / 跟拍 / 升镜 / 甩镜 / 静止长镜

【情绪组合目标】
- 目标情绪：暴躁/忧郁/舒缓/紧张/史诗/暧昧/梦幻/荒凉
- 对应公式：___（参照第六章）

【剪辑逻辑】
- 平行剪辑 / 交叉剪辑 / 蒙太奇

【提示词输出】
中文：___
English：___
```

---

## 十三、综合示例脚本

### 示例：律师做决定（15秒情绪短片）

**场景描述：** 一位中年男性律师，在昏暗的事务所里做出某个决定的瞬间。

**动机分析：**
- 渴望：赢得这场官司（表面目标）
- 需要：找回内心的良知（深层成长）
- 障碍：利益与道德的撕裂
- 处境：顿悟需要 → 完成转变

**完整提示词脚本：**
```
镜头规格：50mm标准镜头，匀速直线缓慢推进。
起幅画面：一位中年男性坐在昏暗律师事务所的皮椅里的中景，
         他双手交握放在膝上，神情凝重。
中段运动：镜头从中景开始匀速缓向他面部推进，
         整个推进过程平滑无晃动，背景的书架与窗外暮光逐渐被推出画框。
落幅画面：画面停止于他眼睛的特写，瞳孔反射着室内最后一缕暮光，
         眼神从沉默缓慢转为决绝。
节奏曲线：15秒分配为"前2秒起幅静止 → 中段11秒匀速推进 → 后2秒特写定格"，
         全程聚焦式情绪收紧。
```

**英文提示词：**
```
Camera: 50mm standard lens, slow steady dolly push forward.
Opening: Medium shot of a middle-aged man sitting in a leather chair
         in a dimly lit law office, hands clasped on his knees, expression grave.
Movement: Camera slowly and smoothly pushes in toward his face,
         bookshelves and window light gradually exiting frame.
Closing: Frame settles on extreme close-up of his eyes,
         pupils reflecting the last glimmer of evening light,
         gaze shifting from stillness to quiet resolve.
Rhythm: 15 seconds — 2s static open → 11s slow push → 2s freeze on close-up,
         continuous emotional compression throughout.
```