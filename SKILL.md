---
name: CoverDesign-skill
description: 用于小红书单张封面设计、封面参考图分析、视频文案到封面提示词转换、内容分类匹配封面模板、输出图形构成、设计规范、正向和负面生图提示词。覆盖教程、旅行、生活方式、美食 PLOG、穿搭、直播上新、访谈综艺等封面。触发于用户上传视频/文案/标题/口播稿/人物图/产品图/食物图/参考封面，并要求做封面设计、封面提示词、封面风格复刻、封面分类推荐、或提到“封面设计 Skill”。
metadata:
  short-description: 小红书封面分析与生图提示词
---

# 封面设计

## Core Rule

This skill is prompt-first. Do not generate images automatically.

Default output is a cover strategy and a reusable prompt. If image generation tools are available, ask whether the user wants to generate after the prompt is delivered. Only call image generation after explicit confirmation such as "生成", "直接做", "调用 image", or "帮我出图".

If image generation tools are unavailable, output only the prompt and say it can be copied into GPT-image, 即梦, Midjourney, or another image tool.

## Workflow

1. Parse the user's content:
   - topic, platform, audience, content type, emotional hook, practical value, click reason
   - available assets: person, product, scene, screenshot, reference cover, video frame, title
2. Classify the cover type using `references/cover-types.md`.
3. If a reference cover is provided, analyze it first:
   - composition, title hierarchy, font style, color system, person/object relationship, decorations, texture, platform signals
4. Select the best cover type and adapt it to the user's content.
5. Output a single-cover design:
   - content judgment
   - recommended cover type
   - matching reason
   - graphic composition
   - design specification
   - positive image prompt
   - negative prompt
   - optional image-generation guidance

Use `references/prompt-patterns.md` for prompt structure. Use `references/output-format.md` for response format.

## Classification Defaults

When multiple types fit, choose the one that best supports the user's primary click reason:

- teach a repeatable method -> 教程干货类
- solve a travel/location problem -> 旅行攻略类
- express mood, daily life, identity, MBTI, personal state -> 生活方式类
- show breakfast, baking, coffee, dessert, meals, cafe, food diary, or cute food doodles -> 美食 PLOG 类
- show outfits, style, products worn on body -> 穿搭杂志类
- announce live stream, product drop, activity time -> 直播上新类
- create topic conflict around people, workplace, interviews, social observation -> 访谈综艺类

If the user only provides a reference image and no content, analyze the reference and output a reusable template prompt. Ask for the actual topic only if the cover cannot be made useful without it.

## Writing Rules

- Write in Chinese by default.
- Focus on one single cover, not a collage, unless the user explicitly asks for a collection.
- Make prompts concrete enough for an image model: subject, scene, title text, layout, font style, colors, decorations, texture, and negative constraints.
- Do not add platform corner badges by default. Avoid red capsule labels, top-left app tags, and fixed "小红书/家居分享/PLOG 日常/旅行" badge elements unless the user explicitly requests them.
- Do not promise exact text rendering quality. Keep text short and specify that it should be clear, large, and placed as described.
- Do not copy a reference cover exactly. Extract its design language and adapt it to the user's topic.
- Preserve user-provided title words when they are usable. If the title is weak, propose 2-3 stronger title alternatives after the main prompt.

## Image Generation Guidance

At the end of the output:

- If imagegen is available: "当前环境支持生图。如果你需要，我可以基于上面的提示词直接生成一张封面。"
- If imagegen is not available: "当前环境无法直接生图，你可以复制上面的提示词到 GPT-image、即梦、Midjourney 或其他工具使用。"
