---
title: "短代码"
weight: 6
draft: false
description: "Blowfish 主题支持的所有短代码。"
slug: "shortcodes"
tags: ["shortcodes", "mermaid", "icon", "lead", "文档"]
series: ["文档"]
series_order: 8
---

（这里保持其他短代码说明不变，只需修改 Carousel 部分）

## 轮播图

`carousel` 用于以交互方式展示多张图片。

<!-- prettier-ignore-start -->
| 参数         | 说明                                                                           |
| ------------ | ------------------------------------------------------------------------------ |
| `images`     | **必填** 图片路径的正则表达式或具体路径                                        |
| `aspectRatio`| **可选** 图片比例，可选 `16-9`（默认）、`21-9` 或 `32-9`                       |
| `interval`   | **可选** 自动切换间隔（毫秒），默认 2000                                       |
<!-- prettier-ignore-end -->

**示例 1：** 16:9 比例，手动指定图片
```md
{{</* carousel 
    images="https://cdn.pixabay.com/photo/2016/12/11/12/02/mountains-1899264_960_720.jpg,gallery/03.jpg,gallery/01.jpg,gallery/02.jpg,gallery/04.jpg"
    aspectRatio="16-9" 
*/>}}

{{</* carousel 
    images="gallery/.*" 
    aspectRatio="21-9" 
    interval="2500" 
*/>}}

---

#### 步骤 3：禁用意大利语文档
在项目根目录的 `config.toml` 中添加：
```toml
disableLanguages = ["it"]  # 禁用意大利语