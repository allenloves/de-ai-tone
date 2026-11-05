# de-ai-tone

去 AI 味：繁體中文寫作與翻譯的風格規範，做成 Claude Code skill。
A style guide for Traditional Chinese (Taiwan) writing and translation that strips the telltale habits of AI-generated prose, packaged as a Claude Code skill.

---

## 中文說明

### 這是什麼

AI 生成的中文有一組可辨識的統計慣性：假對比、破折號濫用、三項式排比、空轉的話語標記、每段收尾的微型總結。單獨看都不算錯，堆疊起來就是「AI 味」。另一種方向相反的慣性是過度壓縮：擬人動詞、名詞堆疊、自創詞組、省掉功能詞的電報體，讓讀者得自己把句子解開。本規範逐條列出這些慣性，禁用或限用，並附生成後的強制自檢清單。核心原則只有一條：每個修辭手段都必須賺回自己的位置。

裝進 Claude Code 之後，任何以繁體中文產出連續文字的任務（翻譯、撰稿、長篇回覆、Claude Code 的工作回報）會自動套用。

### 規範涵蓋

- **禁用與限用清單（第 1–11 條）**：「不是 X 而是 Y」假辯證、破折號、冒號（帽句、擂鼓式宣告）、三項式排比、空轉話語標記、貼標語彙（賦能、打造、旨在）、結構強迫症（濫用列點、加粗、小標題）、開場與收場公式、修辭性設問、贅詞「一個」、框式介詞。
- **壓縮型 AI 味（第 11 之二條）**：擬人動詞配無生命主詞、名詞堆疊、臨時名詞轉動詞、自創詞組、電報體；並給前面各條的刪除測試加上反向限制，刪到讀者要讀第二遍才懂就補回去。依據 Clark、Martin、Mahowald 2026 對英文前沿模型的量測（[arXiv 2610.29162](https://arxiv.org/abs/2610.29162)），中文對應為推論。
- **翻譯專用（第 12–13 條）**：歐化句式的還原——關係子句拆句、「被」字句改寫、代名詞刪減，以及慣用直譯句型的替代方案。忠實優先於流暢：原文刻意的修辭不在清理之列。
- **臺灣用語規範（第 14–16 條）**：支語過濾對照表，按資訊科技、互聯網黑話、音樂與音訊工程、數學科學、學術日常分組；表外詞彙的判斷原則；英文命名禁止無意義的拼音音譯。
- **標點規範（第 17–18 條）**：中文行文一律全形，唯英文與英文之間的標點用半形；引號只留提及、術語首現、引文、篇章名四種本職。
- **正向原則與自檢**：動詞驅動、短句節奏、具體優於抽象、信任讀者、有立場；產出前強制執行十二項逐條掃描，包括挑最擠的一句做平實改寫測試。

### 安裝

```bash
git clone https://github.com/allenloves/de-ai-tone.git ~/.claude/skills/de-ai-tone
```

Claude Code 讀取 `SKILL.md` 的 description 自動觸發；也可在對話中以 `/de-ai-tone` 手動載入。

### 背景

規範出自實際的翻譯與寫作工作，其中包括一部十六世紀音樂理論論著的英譯中全書專案。條目的演進方式是：發現一個實例，收一條規則，配一個可執行的判準（刪除測試、稻草人測試）。

---

## English

### What this is

AI-generated Chinese prose carries a recognizable set of statistical habits: fake dialectic contrasts, em-dash overuse, triadic parallelism, throat-clearing discourse markers, a miniature summary at the end of every paragraph. None of them is wrong in isolation; stacked, they read unmistakably as machine output. A second family runs the opposite way, toward over-compression: personified verbs on inanimate subjects, stacked nouns, coined phrases, telegraphic sentences with function words stripped out, all of which leave the reader to unpack the sentence. This guide enumerates those habits and bans or rations them, ending with a mandatory post-generation checklist. The whole thing rests on one principle: every rhetorical device must earn its place.

Installed as a Claude Code skill, it applies automatically to any task that produces running text in Traditional Chinese, including Claude Code's progress and completion reports.

### What it covers

- **Bans and rations (rules 1–11)**: fake "not X but Y" dialectics, em-dashes, colons (topic-label sentence openers, drumroll announcements), triadic parallelism, empty discourse markers, buzzword vocabulary, structural compulsions (bullet points, bold, headings), formulaic openings and closings, rhetorical self-questioning, article-calque "一個", frame prepositions calqued from English.
- **Compression-style AI tone (rule 11-2)**: personified verbs with inanimate subjects, stacked nouns, ad-hoc denominal verbs, coined phrases, telegraphic omission; plus a reverse check on every deletion test above, so that trimming stops before a sentence needs a second reading. Based on Clark, Martin & Mahowald 2026, who measured these features in English frontier-model output ([arXiv 2610.29162](https://arxiv.org/abs/2610.29162)); the Chinese counterparts are inferred.
- **Translation-specific (rules 12–13)**: undoing Europeanized syntax — splitting relative clauses, rewriting passive constructions, trimming pronouns — plus alternatives to stock calque patterns. Fidelity outranks fluency: deliberate rhetoric in the source is not cleaned up.
- **Taiwan usage (rules 14–16)**: a filter table of PRC vocabulary versus Taiwan equivalents, grouped by field (IT, internet-industry jargon, music and audio engineering, mathematics, academic and daily life); judgment principles for words outside the table; a ban on meaningless pinyin transliteration when naming things in English.
- **Punctuation (rules 17–18)**: full-width punctuation throughout Chinese text, half-width only between English and English; quotation marks restricted to their four real jobs — mention, first use of a term, direct quotation, titles.
- **Positive principles and self-check**: verb-driven sentences, short-sentence rhythm, concrete over abstract, trusting the reader, taking a stance; twelve mandatory scans before any text ships, including a plain-rewrite test on the densest sentence.

### Install

```bash
git clone https://github.com/allenloves/de-ai-tone.git ~/.claude/skills/de-ai-tone
```

Claude Code triggers the skill from the description in `SKILL.md`; you can also load it manually with `/de-ai-tone`.

### Background

The rules come from real translation and writing work, including a complete English-to-Chinese translation of a sixteenth-century music treatise. Each entry follows the same pattern: a habit observed in the wild, a rule against it, and an executable test (deletion test, straw-man test) to decide borderline cases.

The guide itself is written in Traditional Chinese — the ruleset is the content, and its own prose follows every rule it states.

---

© 2026 Allen（allenloves）。本作品以創用 CC 姓名標示—相同方式分享 4.0 國際（[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)）授權釋出。
Licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
