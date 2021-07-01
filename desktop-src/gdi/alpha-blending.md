---
description: Alphablending wird verwendet, um eine Alphabitmap anzuzeigen, bei der es sich um eine Bitmap mit transparenten oder halbtransparenten Pixeln handelt.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alphablending (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4add2aca8ac4e2d7e1b24988eb5d40f80bac259c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120285"
---
# <a name="alpha-blending-windows-gdi"></a>Alphablending (Windows GDI)

*Alphablending* wird verwendet, um eine Alphabitmap anzuzeigen, bei der es sich um eine Bitmap mit transparenten oder halbtransparenten Pixeln handelt. Zusätzlich zu einem roten, grünen und blauen Farbkanal verfügt jedes Pixel in einer Alphabitmap über eine Transparenzkomponente, die als *Alphakanal bezeichnet wird.* Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal. Beispielsweise kann ein 8-Bit-Alphakanal 256 Transparenzebenen darstellen, von 0 (die gesamte Bitmap ist transparent) bis 255 (die gesamte Bitmap ist nicht transparent).

Alphablendingmechanismen werden durch Aufrufen von [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)aufgerufen, das auf die [**BLENDFUNCTION-Struktur**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) verweist.

Alphawerte pro Pixel werden nur für 32-bpp BI \_ RGB unterstützt. Diese Formel ist definiert als:


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

Bitmaps können auch mit einem Transparenzfaktor angezeigt werden, der auf die gesamte Bitmap angewendet wird. Jedes Bitmapformat kann mit einem globalen konstanten Alphawert angezeigt werden, indem **SourceConstantAlpha** in der [**BLENDFUNCTION-Struktur festlegen.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) Der globale konstante Alphawert hat 256 Transparenzebenen, von 0 (gesamte Bitmap ist vollständig transparent) bis 255 (die gesamte Bitmap ist vollständig deckend). Der globale konstante Alphawert wird mit dem Alphawert pro Pixel kombiniert.

Ein Beispiel finden Sie unter [AlphaBlending a Bitmap (Alphablending einer Bitmap).](alpha-blending-a-bitmap.md)

 

 



