---
description: Arbeiten mit 16-Bit-RGB
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Arbeiten mit 16-Bit-RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347418"
---
# <a name="working-with-16-bit-rgb"></a>Arbeiten mit 16-Bit-RGB

Zwei Formate sind für 16-Bit-unkomprimierte RGB definiert:

-   Mediasubtype \_ 555 verwendet jeweils fünf Bits für die roten, grünen und blauen Komponenten in einem Pixel. Das signifikanteste Bit im **Wort** wird ignoriert.
-   Mediasubtype \_ 565 verwendet fünf Bits für die roten und blauen Komponenten und sechs Bits für die grüne Komponente. Dieses Format spiegelt die Tatsache wider, dass die menschliche Vision für die grünen Teile des sichtbaren Spektrums am empfindlichsten ist.

**RGB 565**

Wenn Sie die Farbkomponenten aus einem RGB-565-Image extrahieren möchten, behandeln Sie jedes Pixel als **Worttyp** , und verwenden Sie die folgenden Bitmasken:


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Nehmen Sie die Farbkomponenten aus einem Pixel wie folgt:


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



Beachten Sie, dass die roten und blauen Kanäle 5 Bits und der grüne Kanal 6 Bits sind. Um diese Werte in 8-Bit-Komponenten (24-Bit-oder 32-Bit-RGB) zu konvertieren, müssen Sie die entsprechende Anzahl von Bits nach links verschieben:


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Umkehren Sie diesen Prozess, um ein RGB-565-Pixel zu erstellen. Angenommen, die Farbwerte wurden auf die richtige Anzahl von Bits gekürzt:


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

Das Arbeiten mit RGB 555 ist im Wesentlichen mit RGB 565 identisch, mit der Ausnahme, dass Bitmasken und Bitverschiebungs Vorgänge unterschiedlich sind. Gehen Sie folgendermaßen vor, um die Farbkomponenten aus einem RGB-555-Pixel zu erhalten:


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



Gehen Sie folgendermaßen vor, um die roten, grünen und blauen Farbwerte in ein RGB-555-Pixel zu packen:


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unkomprimierte RGB-Video Untertypen](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



