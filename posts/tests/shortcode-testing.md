---
title: 样式预览 &nbsp;·&nbsp; 简码
date: 2025-06-24T13:29:14+08:00
categories: [tests]
tags: []
summary: 测试 Hugo 及 Blowfish 支持的预定义元素外观效果。包括响应式图片、按钮、图表、色板等。
draft: false
isCJKLanguage: true
---

站内简码是一套由 Hugo 提供，Blowfish 扩展的预定义模板元素，用以在文章中插入多样化的媒体。

## Article

{{< article link="/posts/tests/layout-testing/" >}}

## Alert

{{< alert icon="triangle-exclamation" iconColor="#f1faee" cardColor="#e63946" textColor="#f1faee" >}}
请不要轻易尝试 `rm -rf /*` ！
{{< /alert >}}

## Button

{{< button href="https://imwqqa.com/posts/tests/layout-testing/" >}}
Teleportation
{{< /button >}}

## Chart

{{< chart >}}
type: 'bubble',
data: {
    datasets: [{
        label: "Example",
        data: [
        {
            "x": 99,
            "y": 53,
            "r": 9
        },
        {
            "x": 18,
            "y": 70,
            "r": 6
        },
        {
            "x": 59,
            "y": 98,
            "r": 7
        },
        {
            "x": 76,
            "y": 55,
            "r": 4
        },
        {
            "x": 45,
            "y": 12,
            "r": 10
        },
        {
            "x": 23,
            "y": 67,
            "r": 8
        },
        {
            "x": 8,
            "y": 34,
            "r": 3
        },
        {
            "x": 64,
            "y": 29,
            "r": 5
        },
        {
            "x": 31,
            "y": 86,
            "r": 7
        },
        {
            "x": 55,
            "y": 41,
            "r": 6
        },
        {
            "x": 12,
            "y": 77,
            "r": 10
        },
        {
            "x": 90,
            "y": 20,
            "r": 4
        },
        {
            "x": 37,
            "y": 63,
            "r": 9
        },
        {
            "x": 81,
            "y": 48,
            "r": 5
        },
        {
            "x": 24,
            "y": 11,
            "r": 3
        },
        {
            "x": 68,
            "y": 92,
            "r": 7
        },
        {
            "x": 47,
            "y": 35,
            "r": 8
        },
        {
            "x": 3,
            "y": 57,
            "r": 6
        },
        {
            "x": 71,
            "y": 15,
            "r": 10
        },
        {
            "x": 29,
            "y": 84,
            "r": 4
        },
        {
            "x": 60,
            "y": 38,
            "r": 9
        },
        {
            "x": 14,
            "y": 68,
            "r": 5
        },
        {
            "x": 83,
            "y": 27,
            "r": 7
        },
        {
            "x": 38,
            "y": 71,
            "r": 3
        },
        {
            "x": 52,
            "y": 59,
            "r": 6
        },
        {
            "x": 20,
            "y": 45,
            "r": 8
        },
        {
            "x": 96,
            "y": 30,
            "r": 10
        },
        {
            "x": 6,
            "y": 82,
            "r": 4
        },
        {
            "x": 66,
            "y": 46,
            "r": 9
        },
        {
            "x": 27,
            "y": 53,
            "r": 7
        },
        {
            "x": 43,
            "y": 14,
            "r": 5
        },
        {
            "x": 78,
            "y": 91,
            "r": 3
        },
        {
            "x": 33,
            "y": 61,
            "r": 8
        },
        {
            "x": 57,
            "y": 49,
            "r": 6
        },
        {
            "x": 19,
            "y": 73,
            "r": 10
        },
        {
            "x": 70,
            "y": 22,
            "r": 4
        },
        {
            "x": 25,
            "y": 88,
            "r": 9
        },
        {
            "x": 41,
            "y": 36,
            "r": 5
        },
        {
            "x": 85,
            "y": 17,
            "r": 7
        },
        {
            "x": 30,
            "y": 65,
            "r": 3
        },
        {
            "x": 63,
            "y": 44,
            "r": 8
        },
        {
            "x": 17,
            "y": 79,
            "r": 6
        },
        {
            "x": 74,
            "y": 9,
            "r": 9
        },
        {
            "x": 10,
            "y": 7,
            "r": 5
        },
        {
            "x": 55,
            "y": 70,
            "r": 10
        }
        ],
    }]
}
{{< /chart >}}

## Code Importer

{{< codeimporter url="https://raw.githubusercontent.com/nunocoracao/blowfish/main/layouts/shortcodes/mdimporter.html" type="go" >}}

## Katex

{{< katex >}}

$$
    \int_{a}^{b} f(x)dx = F(b) - F(a)
$$

## Swatches

{{< swatches "#64748b" "#3b82f6" "#06b6d4">}}

## Mermaid

{{< mermaid >}}
    graph LR;
    A[Lemons]-->B[Lemonade];
    B-->C[Profit]
{{< /mermaid >}}


## TypeIt

{{< typeit lifeLike=true speed=50 >}}
Lorem ipsum dolor sit amet, 
consectetur adipiscing elit. 
{{< /typeit >}}

