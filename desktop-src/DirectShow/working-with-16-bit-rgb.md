---
description: Arbeiten mit 16-Bit-RGB
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Arbeiten mit 16-Bit-RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660d5b0223bab6c19a89e4316f7dffce56ec0545f83c72f7316b9278dfa3e4c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071794"
---
# <a name="working-with-16-bit-rgb"></a>Arbeiten mit 16-Bit-RGB

Für unkomprimiertes RGB mit 16 Bit sind zwei Formate definiert:

-   MEDIASUBTYPE 555 verwendet jeweils fünf Bits für die roten, grünen und blauen \_ Komponenten in einem Pixel. Das wichtigste Bit in **WORD** wird ignoriert.
-   MEDIASUBTYPE 565 verwendet fünf Bits für die roten und blauen Komponenten und sechs Bits \_ für die grüne Komponente. Dieses Format spiegelt die Tatsache wider, dass das menschliche Sehen am empfindlichsten auf die grünen Teile des sichtbaren Spektrums reagieren kann.

**RGB 565**

Um die Farbkomponenten aus einem RGB 565-Bild  zu extrahieren, behandeln Sie jedes Pixel als WORD-Typ, und verwenden Sie die folgenden Bitmasken:


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Erhalten Sie die Farbkomponenten wie folgt aus einem Pixel:


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



Beachten Sie, dass der rote und der blaue Kanal 5 Bits und der grüne Kanal 6 Bits beträgt. Um diese Werte in 8-Bit-Komponenten (für 24-Bit- oder 32-Bit-RGB) zu konvertieren, müssen Sie die entsprechende Anzahl von Bits nach links verschieben:


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Kehren Sie diesen Vorgang um, um ein RGB-Pixel von 565 Pixeln zu erstellen. Angenommen, die Farbwerte wurden auf die richtige Anzahl von Bits abgeschnitten:


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

Die Arbeit mit RGB 555 ist im Wesentlichen identisch mit RGB 565, außer dass sich die Bitmasken und Bitverschiebungsvorgänge unterscheiden. Gehen Sie wie folgt vor, um die Farbkomponenten aus einem RGB-Pixel von 555 Pixeln zu erhalten:


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



Gehen Sie wie folgt vor, um die Farbwerte für Rot, Grün und Blau in ein RGB-Pixel von 555 Pixeln zu packen:


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht komprimierte RGB-Videountertypen](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



