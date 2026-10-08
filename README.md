# 终极无敌文生图反推提示词｜参考图反推与图片复刻

**Ultimate Text-to-Image Reverse Prompt · Image-to-Prompt · Reference Image Replication**

由 **ChatGPT 6 Astra（Ultra）** 生成的「**终极无敌文生图反推提示词**」。上传一张或多张参考图，让 AI 将可观察的构图、主体、空间关系、色彩、光影、材质与文字，整理成可直接使用的**文生图 Prompt**和**图生图 / 参考图 Prompt**。

适合搜索和使用：**文生图提示词、文生图 prompt、图片反推提示词、参考图反推、图片复刻、图像复刻、图生图提示词、提示词逆向工程**。

A reusable **text-to-image prompt reverse-engineering template**, generated with **ChatGPT 6 Astra (Ultra)**, for **image-to-prompt analysis, reference image reconstruction, visual replication, and image-to-image prompting**. Chinese instructions, English generation prompts by default, and original-language text preservation.

[中文使用指南](#中文使用指南) · [English guide](#english-guide) · [打开完整提示词](./%E6%96%87%E7%94%9F%E5%9B%BEprompt.txt) · [下载原始 TXT](https://raw.githubusercontent.com/MrDouZheng/text-to-image-prompt-reverse-engineering-replication/main/%E6%96%87%E7%94%9F%E5%9B%BEprompt.txt)

## 项目信息 / Project information

| 项目 | 内容 |
| --- | --- |
| 中文名称 | 终极无敌文生图反推提示词：参考图反推与图片复刻 |
| English name | Ultimate Text-to-Image Prompt Reverse Engineering & Reference Image Replication |
| 生成来源 / Generation source | ChatGPT 6 Astra · Ultra（由发布者提供的来源说明 / attribution supplied by the publisher） |
| 原始文件 / Original file | [`文生图prompt.txt`](./%E6%96%87%E7%94%9F%E5%9B%BEprompt.txt)，完整保留原文 |
| 输入 / Input | 一张或多张参考图片 / One or more reference images |
| 输出 / Output | 复刻规格、文生图 Prompt、图生图 Prompt、负向约束与设置、对照验收点 |
| 默认语言 / Default language | 中文说明、英文生成提示词；画面内文字保留原语言 |

## 中文使用指南

### 这份提示词能做什么

- **从参考图反推提示词**：把可见视觉信息转换为明确、可执行的生成指令。
- **文生图复刻**：完整描述画面，使生成模型在看不到参考图时也能使用提示词。
- **图生图 / 参考图复刻**：写清输入图片的顺序、分工、需要保留的特征和允许修改的内容。
- **多图处理**：区分逐图独立复刻、主图与辅助图、指定属性融合，避免擅自合成。
- **抓住决定相似度的细节**：按 P0、P1、P2 排序，优先保住构图、轮廓、姿态、关键色块和文字。
- **保留原图观感**：包括不对称、颗粒、模糊、偏色、磨损、边缘裁切等真实特征。
- **对照结果迭代**：提供原图和生成结果后，按可见差异修改，并重新交付完整 Prompt。

它根据参考图中的视觉证据编写复刻提示词，不猜测原始随机种子、原始模型、隐藏参数或无法辨认的文字。

### 三步开始

1. 打开 [`文生图prompt.txt`](./%E6%96%87%E7%94%9F%E5%9B%BEprompt.txt)，复制**完整内容**。
2. 将完整提示词粘贴到能读取图片的 AI 对话中，并在同一条消息附上参考图。
3. 获取文生图或图生图提示词，按目标生成模型的实际能力使用；随后可提交生成结果继续对照迭代。

文件末尾会要求立即开始分析参考图，因此首次提交时就附上图片。目标模型、版本或平台已知时，可以一并说明；没有填写设置时，按原文默认规则执行。

### 常用请求示例

以下是与**完整原始提示词和参考图片**一起提交的补充要求：

**完整交付：**

```text
请分析我附上的参考图，尽可能忠实复刻整张可见画面。
同时交付文生图与图生图两种使用路径，保留原图比例。
```

**只要英文文生图 Prompt：**

```text
生成方式：仅文生图。
提示词语言：英文。
只要 Prompt。
```

**使用中文 Prompt：**

```text
生成方式：仅文生图。
提示词语言：中文。
只要 Prompt。
```

**多张独立参考图：**

```text
这些图片是不同画面，请按上传顺序逐图独立复刻。
每张图都交付完整可用的提示词。
```

**主图与辅助图：**

```text
Image 1 是主图，控制构图、视角、姿态、光影与裁切。
Image 2 只补充服装细节，其他内容以 Image 1 为准。
仅交付图生图 / 参考图 Prompt。
```

**比较生成结果并修正：**

```text
Image 1 是原参考图，Image 2 是生成结果。
请优先比较 P0 与 P1 差异，说明对应修改，并交付修改后的完整 Prompt。
```

### 默认交付与完整结构

默认按每个复刻目标交付：

| 交付部分 | 内容 |
| --- | --- |
| A. 复刻规格 | 图片分工、画幅、P0/P1 特征、位置与空间关系、不确定项 |
| B. 文生图主 Prompt | 可以独立提交给文生图模型的完整提示词 |
| C. 图生图 / 参考图主 Prompt | 图片绑定说明与完整提示词 |
| D. 负向约束与生成设置 | 与当前图片有关的限制及必要设置 |
| E. 对照验收点 | 主体、构图、光色、文字和新增元素的具体检查点 |

B、C 是两种独立使用路径，可按需求选用。说“只要 Prompt”可启用原文中的精简输出规则。

原始模板包含十二部分：可选设置、观察与证据规则、多图输入规则、建立复刻规格、筛选相似度特征、编写可执行 Prompt、区分文生图与图生图、负向约束与参数、默认交付格式、提交前检查、后续迭代、精简输出开关。

### 使用边界

复刻效果取决于参考图清晰度、视觉分析模型、目标生成模型及其参考图和结构控制能力。精确文字、复杂几何或被遮挡信息可能需要额外工具或补充素材；原始模板会区分可见事实、近似估计与无法确定的信息。

本项目发布的是完整提示词模板；尚未附上固定测试集、生成结果对照或相似度评分。

## English guide

### What is this prompt?

**Ultimate Text-to-Image Reverse Prompt** is a reusable template for turning reference images into detailed generation prompts. It was generated with **ChatGPT 6 Astra (Ultra)**, according to the publisher's attribution, and is published here in its original Chinese form.

The template focuses on observable visual evidence: composition, subject identity and appearance, object relationships, perspective, lighting, color, material, typography, and visible imperfections. It produces English generation prompts by default, with Chinese explanations, and preserves text inside images in its original language.

### How to use

1. Open the [complete prompt file](./%E6%96%87%E7%94%9F%E5%9B%BEprompt.txt) or [download the original TXT](https://raw.githubusercontent.com/MrDouZheng/text-to-image-prompt-reverse-engineering-replication/main/%E6%96%87%E7%94%9F%E5%9B%BEprompt.txt).
2. Copy the entire template into an image-capable AI chat and attach your reference images in the same message.
3. Specify a target generation model and desired output language if needed. Use either the text-to-image prompt or the image-to-image / reference-image prompt that is returned.
4. To refine a result, attach both the original reference and the generated image, identify each image, and request a revised complete prompt.

The template's default response includes reproduction specifications, one text-to-image prompt per target, a reference-image prompt with image-role mapping, relevant negative constraints and settings, and concrete comparison checkpoints.

### Example additions to the complete template

**English text-to-image prompt only:**

```text
Generation method: text-to-image only.
Prompt language: English.
Only the prompt.
Preserve the reference image's aspect ratio and visible composition.
```

**Multiple independent images:**

```text
Treat these as separate reference images, in upload order.
Produce a complete, independent reproduction prompt for each image.
```

**Reference-image prompting:**

```text
Image 1 controls composition, viewpoint, pose, lighting, and crop.
Image 2 contributes clothing details only.
Return the image-to-image / reference-image prompt only.
```

### Core principles

- Use visible evidence and label uncertainty.
- Prioritize composition and structural similarity before secondary details.
- Preserve the reference's imperfections and crop.
- Bind each attribute to the correct subject or object.
- Keep text-to-image prompts self-contained.
- Specify image roles when working with multiple references.
- Use model-specific parameters only when support is confirmed.
- Compare generated results against concrete visual checkpoints.

This is a prompt template for visual reverse engineering and image reconstruction. It does not recover the original hidden prompt or random seed. Results depend on the reference quality and the capabilities of the analysis and generation models. No benchmark results or similarity scores are included in this initial release.

## 搜索词 / Search terms

**中文：** 文生图 prompt · 文生图提示词 · 文生图反推 · 图片反推提示词 · 参考图反推 · 图片转提示词 · 图片复刻 · 图像复刻 · 参考图复刻 · 图生图提示词 · 提示词逆向工程 · ChatGPT 6 Astra Ultra · 终极无敌文生图反推提示词。

**English:** text-to-image prompt · image-to-prompt · reverse image prompt · prompt reverse engineering · reference image replication · image reconstruction · visual reproduction · image-to-image prompt · bilingual image prompt · ChatGPT 6 Astra Ultra.

