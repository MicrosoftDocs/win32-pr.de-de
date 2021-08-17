---
description: Während der Direct3D- und Fensterprogrammierung wird auf Objekte auf dem Bildschirm als umrandende Rechtecke verwiesen.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rechtecke (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02dda6e8a4f10128ab11ffeb8b390e79be7cc0f698ed1625ca3f2c5df995d67e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119368874"
---
# <a name="rectangles-direct3d-9"></a>Rechtecke (Direct3D 9)

Während der Direct3D- und Fensterprogrammierung wird auf Objekte auf dem Bildschirm als umrandende Rechtecke verwiesen. Die Seiten eines umrandenden Rechtecks sind immer parallel zu den Seiten des Bildschirms, sodass das Rechteck durch zwei Punkte beschrieben werden kann: die obere linke Ecke und die untere rechte Ecke. Die meisten Anwendungen verwenden die [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) um Informationen zu einem umrandenden Rechteck zu enthalten, das beim Blitting auf dem Bildschirm oder beim Ausführen der Treffererkennung verwendet werden soll.

In C++ hat die [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) die folgende Definition.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



Im vorherigen Beispiel sind der linke und der obere Member die x- und y-Koordinaten der oberen linken Ecke eines umgebundenen Rechtecks. Analog dazu stellen die rechten und unteren Elemente die Koordinaten der unteren rechten Ecke zusammen. Die folgende Abbildung zeigt, wie Sie diese Werte visualisieren können.

![Abbildung des Rechtecks, das durch den linken, oberen, rechten und unteren Wert gebunden ist](images/rect.png)

Die Pixelspalte am rechten Rand und die Pixelzeile am unteren Rand sind nicht im RECT enthalten. Beispielsweise führt das Sperren eines RECT mit den Membern {10, 10, 138, 138} zu einem Objekt mit einer Breite und Höhe von 128 Pixeln.

Im Interesse der Effizienz, Konsistenz und Benutzerfreundlichkeit funktionieren alle Direct3D-Präsentationsfunktionen mit Rechtecke.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
