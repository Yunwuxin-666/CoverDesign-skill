# Prompt Patterns

Every positive image prompt should include these parts in natural Chinese prose:

1. cover type and platform:
   - "一张小红书单张封面，竖版 3:4..."
2. scene/background:
   - where it happens, light, texture, mood, realism level
3. subject:
   - person/object/product, pose, placement, expression, clothing, relationship to camera
4. title:
   - exact title text, position, size, font style, color, hierarchy
5. graphic composition:
   - where each element sits: top, bottom, left, right, foreground, background
6. decorations:
   - stickers, arrows, hand-drawn lines, cards, labels, dots, icons, screenshots
7. color and typography:
   - palette, font family style, contrast, text effects
8. platform/style:
   - 小红书, Vlog, 教程, 杂志拼贴, 旅行手账, 综艺封面, etc.

## Type-Specific Prompt Notes

### 教程干货类

Must include:
- clear tutorial title
- instructor/person or tool interface
- proof module: before/after, cases, steps, formula, screenshots
- high readability on phone
- strong benefit line

Avoid:
- pure poster with no human/proof
- tiny title
- unclear learning outcome

### 旅行攻略类

Must include:
- real travel scene
- one concrete pain-point object or location cue
- large hand-written title
- travel sticker, handwritten note, or location cue, but no fixed red capsule platform badge unless requested
- doodle arrows/labels

Avoid:
- generic tourist postcard
- overly commercial travel ad
- polished stock-photo feeling

### 生活方式类

Must include:
- real daily-life photo
- emotional title in hand-written style
- natural light, film grain or halftone accents
- personal, diary-like composition
- for food, coffee, baking, dessert, or table diary content: add hand-drawn illustration overlays such as cute face, arms, legs, blush, motion lines, speech bubbles, sound words, and small props

Avoid:
- corporate design
- hard-selling CTA
- standard printed title font

### 美食 PLOG 类

Must include:
- real close-up food photography or table still life
- one main food/drink subject with cute anthropomorphic doodle face, arms, legs, blush, or small props
- white handwritten notes, curved captions, arrows, speech bubbles, or playful sound words
- warm natural light, wood table, linen cloth, plate, cup, book, tray, or small home props
- cozy diary mood, appetizing food texture, clear phone-readable title

Avoid:
- restaurant menu poster style
- commercial food advertising
- over-clean product photography
- heavy platform badges
- doodles that cover the food texture

### 穿搭杂志类

Must include:
- fashion subject in outfit
- editorial collage, item cards, labels
- English headline or OOTD marker
- clean cutouts or magazine layout

Avoid:
- e-commerce product grid
- low-quality model image
- clutter that hides outfit details

### 直播上新类

Must include:
- premium product/fashion campaign feel
- live time and room info
- seasonal headline
- elegant serif title and hand-drawn motion lines

Avoid:
- cheap sale banner
- loud red-yellow promotion style
- unclear date/time

### 访谈综艺类

Must include:
- human face and expression
- giant keywords
- topic-conflict wording
- video/play or variety-show visual cues

Avoid:
- overly quiet/minimal layout
- weak headline
- hidden face

## Universal Negative Prompt

Use and adapt:

```text
不要九宫格，不要合集图，不要多张封面，不要纯插画风，不要动漫人物，不要欧美人物，除非用户指定，不要红色胶囊角标，不要左上角平台标签，不要固定小红书标签，不要标题太小，不要文字模糊，不要错别字，不要遮挡人物五官，不要人脸变形，不要手部畸形，不要低清晰度，不要廉价模板感，不要过度杂乱，不要与主题无关的装饰。
```
