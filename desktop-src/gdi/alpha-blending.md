---
description: Alpha Blending wird zum Anzeigen einer Alpha Bitmap verwendet, bei der es sich um eine Bitmap mit transparenten oder semitransparenten Pixeln handelt.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alpha Mischung (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978825"
---
# <a name="alpha-blending-windows-gdi"></a>Alpha Mischung (Windows GDI)

*Alpha Blending* wird zum Anzeigen einer Alpha Bitmap verwendet, bei der es sich um eine Bitmap mit transparenten oder semitransparenten Pixeln handelt. Zusätzlich zu einem roten, grünen und blauen Farbkanal weist jedes Pixel in einer Alpha Bitmap eine Transparenz Komponente auf, die als *Alphakanal* bezeichnet wird. Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal. Ein 8-Bit-Alphakanal kann z. b. 256 Ebenen der Transparenz darstellen, von 0 (die gesamte Bitmap ist transparent) bis 255 (die gesamte Bitmap ist nicht transparent).

Alpha Mischungs Mechanismen werden aufgerufen, indem [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)aufgerufen wird, das auf die [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) -Struktur verweist.

Alpha Werte pro Pixel werden nur für 32-bpp-BI-RGB unterstützt \_ . Diese Formel wird wie folgt definiert:


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



Dies wird im Arbeitsspeicher dargestellt, wie in der folgenden Tabelle dargestellt.



|       |       |       |       |
|-------|-------|-------|-------|
| 31:24 | 23:16 | 15:08 | 07:00 |
| Alpha | Red   | Grün | Blau  |



 

Bitmaps können auch mit einem auf die gesamte Bitmap angewendeten Transparenz Faktor angezeigt werden. Jedes Bitmap-Format kann mit einem globalen Konstanten Alpha Wert angezeigt werden, indem **SourceConstantAlpha** in der [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) -Struktur festgelegt wird. Der Wert der globalen Konstanten Alpha-Wert hat 256 Ebenen der Transparenz, von 0 (gesamte Bitmap ist vollständig transparent) bis 255 (gesamte Bitmap ist vollständig deckend). Der Wert der globalen Konstanten Alpha-Wert wird mit dem Alpha Wert pro Pixel kombiniert.

Ein Beispiel finden Sie unter [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).

 

 



