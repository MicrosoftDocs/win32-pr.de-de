---
description: Alphablending wird verwendet, um eine Alphabitmap anzuzeigen, bei der es sich um eine Bitmap mit transparenten oder halbtransparenten Pixeln handelt.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alphablending (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb59f6b628236124305e4564803fa826c279bfdc2353725a62029b293cb1e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470130"
---
# <a name="alpha-blending-windows-gdi"></a>Alphablending (Windows GDI)

*Alphablending* wird verwendet, um eine Alphabitmap anzuzeigen, bei der es sich um eine Bitmap mit transparenten oder halbtransparenten Pixeln handelt. Zusätzlich zu einem roten, grünen und blauen Farbkanal verfügt jedes Pixel in einer Alphabitmap über eine Transparenzkomponente, die als *Alphakanal* bezeichnet wird. Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal. Beispielsweise kann ein 8-Bit-Alphakanal 256 Transparenzebenen darstellen, von 0 (die gesamte Bitmap ist transparent) bis 255 (die gesamte Bitmap ist nicht transparent).

Alphamischungsmechanismen werden aufgerufen, indem [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)aufgerufen wird, das auf die [**BLENDFUNCTION-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) verweist.

Alphawerte pro Pixel werden nur für BI RGB mit 32 bpp \_ unterstützt. Diese Formel wird wie folgt definiert:


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



Dies wird im Arbeitsspeicher dargestellt, wie in der folgenden Tabelle gezeigt.

:::row:::
    :::column:::
        31:24
    :::column-end:::
    :::column:::
        23:16
    :::column-end:::
    :::column:::
        15:08
    :::column-end:::
    :::column:::
        07:00
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        Alpha
    :::column-end:::
    :::column:::
        Red
    :::column-end:::
    :::column:::
        Grün
    :::column-end:::
    :::column:::
        Blau
    :::column-end:::
:::row-end:::

Bitmaps können auch mit einem Transparenzfaktor angezeigt werden, der auf die gesamte Bitmap angewendet wird. Jedes Bitmapformat kann mit einem globalen konstanten Alphawert angezeigt werden, indem **SourceConstantAlpha** in der [**BLENDFUNCTION-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) festgelegt wird. Der alpha-Wert der globalen Konstante weist 256 Transparenzebenen auf, von 0 (die gesamte Bitmap ist vollständig transparent) bis 255 (die gesamte Bitmap ist vollständig deckend). Der globale konstante Alphawert wird mit dem Pro-Pixel-Alphawert kombiniert.

Ein Beispiel finden Sie unter [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).

 

 



