# 语言学期刊 CSL 样式库

本目录覆盖 CSSCI（2025—2026）语言学来源期刊与扩展版期刊中，本地期刊论文库具有可核验 PDF 样例的 35 种中文期刊；每刊均有 `original` 与 `direct` 两版。另含 Glottometrics 校订样式。

适用版本：2026-10-04；各刊样例年份和缺样例清单见 `COVERAGE.md`；Glottometrics 样式依据第 60 卷（2026）校订。

所有本项目编写的 CSL 均在 `<info>` 中使用以下作者信息：`Tsy Yih <yihtsy@outlook.com>`。

## 中文期刊双版本约定

- `V1 Original 字段版`：英文或罗马化信息保存在普通字段，中文原文保存在 Extra 的 `original-*` 字段。
- `V2 普通字段直出版`：只读取 `author`、`title`、`container-title`、`publisher` 等普通字段，不读取 `original-*`。
- 后续每个中文期刊均同时交付 V1、V2，并在 CSL `<summary>` 和本文件中记录格式证据年份与适用范围。

## Original 字段写法

Zotero 普通字段保存英文或罗马化信息；中文原文放在 `Extra`：

```text
Original Author: 范 || 璐
Original Author: 蒋 || 跃
Original Title: 翻译语言特征新假设“折中假设”——基于依存语法的计量研究
Original Container Title: 外语教学与研究
Original Publisher: 商务印书馆
Original Publisher Place: 北京
```

如果普通字段保存英文译名或罗马化信息，`Language` 建议填写 `en-US` 或 `en-GB`；原文是中文并不改变这一点。Original 版直接检查 `original-*`，不依赖 `Language`。

普通字段直出版中，凡样式需要区分中外文，中文条目应将 `Language` 设为 `zh-CN`，外文条目设为 `en-US`、`en-GB` 等相应外语代码；样式据此选择中文或外文著录格式。尤其是《中国语文》《世界汉语教学》，不要让外文条目的 `Language` 留空。

## 样式行为

- `外语教学与研究-original.csl`：主著录使用英文/罗马化普通字段，中文作者、题名和刊名读取 `original-*` 并追加对照。
- `外语教学与研究-direct.csl`：全部内容直接读取普通字段，不追加 `original-*` 对照。
- `中国语文-original.csl`：中文来源优先使用 `original-*`；外文文献和缺失原文字段的条目回退普通字段。
- `中国语文-direct.csl`：全部内容直接读取普通字段，并根据 `Language` 区分中文、外文格式。
- `当代语言学-original.csl`：英文或罗马化信息作主著录；中文作者置于圆括号，中文题名、刊名等置于条目末尾的方括号。
- `当代语言学-direct.csl`：只用普通字段生成《当代语言学》作者—年份格式，不生成中文对照块。
- `现代外语-original.csl`：英文或罗马化信息作主著录，并从 `original-*` 追加中文作者与方括号中文对照。
- `现代外语-direct.csl`：只用普通字段生成《现代外语》作者—年份格式，不生成中文对照块。
- `世界汉语教学-original.csl`：有 `original-*` 的条目按中文文献著录并排在外文文献之前；外文条目使用普通字段。
- `世界汉语教学-direct.csl`：根据 `Language` 区分中文、外文条目，并将中文文献排在外文文献之前。
- `外国语-original.csl`：有 `original-*` 的来源按中文字段著录，其他来源按外文字段著录；正文和文后表均采用顺序编码制，保留 `[J]`、`[M]`、`[C]`、`[D]` 等类型标识。
- `外国语-direct.csl`：只用普通字段，并根据 `Language` 控制中外文题名的斜体行为；采用顺序编码制。
- `glottometrics.csl`：按第 60 卷实例处理期刊论文、专著、章节、会议论文、学位论文、网页、报告和数据集；正文同一第一作者同年文献使用扩展作者姓名消歧。

其余期刊依据各自 PDF 参考文献页分别采用传统作者—年份制、顺序编码制、正文作者—年份但文后编号制、中英并列制等模板，并非把同一份样式简单改名。每份 CSL 的 `<summary>` 都写明证据年份。

## 格式证据与适用年份

| 期刊 | 版本文件 | 格式证据 | 当前适用范围 |
|---|---|---|---|
| 外语教学与研究 | `外语教学与研究-original.csl` / `外语教学与研究-direct.csl` | 2024年第4期、2026年第3期 | 已核验的2024—2026年版式；跨年度使用宜复核 |
| 中国语文 | `中国语文-original.csl` / `中国语文-direct.csl` | 2023年第2期多篇文章 | 已核验的2023年版式；其他年份使用宜复核 |
| 当代语言学 | `当代语言学-original.csl` / `当代语言学-direct.csl` | 2022年第3期多篇文章 | 已核验的2022年版式；其他年份使用宜复核 |
| 世界汉语教学 | `世界汉语教学-original.csl` / `世界汉语教学-direct.csl` | 2020年第2期多篇文章 | 已核验的2020年版式；其他年份使用宜复核 |
| 现代外语 | `现代外语-original.csl` / `现代外语-direct.csl` | 2024年第4期、2025年样刊 | 已核验的2024—2025年版式；跨年度使用宜复核 |
| 外国语 | `外国语-original.csl` / `外国语-direct.csl` | 2025年、2026年样刊 | 已核验的2025—2026年版式；跨年度使用宜复核 |
| Glottometrics | `glottometrics.csl` | 第60卷（2026）全部5篇文章，视觉核对其中3篇参考文献页 | 2026年第60卷版式 |

完整 42 刊覆盖状态、35 刊样例年份以及 7 种缺样例期刊见 `COVERAGE.md`。

`test-items.json` 是直接供 CSL 处理器使用的测试数据，字段结构对应 Zotero 解析 Extra 后形成的 CSL 数据。

## Zotero 与 BibTeX

- 在 Zotero 的 Word/LibreOffice 插件、快速复制和 CSL JSON 导出中，以上 Extra 行会被解析为 CSL 变量，样式可直接读取。
- 普通 BibTeX 没有统一、可移植的 `original-author`、`original-title` 等字段约定。若先导出 `.bib` 再交给其他处理器，不能默认这些信息仍会保留；应逐条验证导出结果。
- 以英文元数据为主、同时需要中文刊物格式时，推荐使用 Original 字段版，并把中文原文信息放入上述 Extra 字段；在 Zotero 内直接使用 CSL，或导出 CSL JSON。

## 验证

71 份现行样式已于 2026-10-04 使用 citeproc-js 2.4.63 完成实际渲染。70 份中文期刊样式使用同一组中外文测试条目分别验证 Original 与普通字段通道；Glottometrics 另以 10 个测试条目覆盖 8 类文献及同年同作者消歧。全部文件也通过 XML 解析，并核验作者元数据完整。
