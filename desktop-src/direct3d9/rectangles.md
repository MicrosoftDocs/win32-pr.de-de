---
description: Während der Direct3D-und Fenster Programmierung werden Objekte auf dem Bildschirm in Bezug auf Begrenzungs Rechtecke bezeichnet.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rechtecke (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123434"
---
# <a name="rectangles-direct3d-9"></a>Rechtecke (Direct3D 9)

Während der Direct3D-und Fenster Programmierung werden Objekte auf dem Bildschirm in Bezug auf Begrenzungs Rechtecke bezeichnet. Die Seiten eines umgebenden Rechtecks sind immer parallel zu den Seiten des Bildschirms. Daher kann das Rechteck durch zwei Punkte, die obere linke Ecke und die untere rechte Ecke beschrieben werden. Die meisten Anwendungen verwenden die [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, um Informationen zu einem umgebenden Rechteck zu übertragen, das beim blisten auf den Bildschirm oder beim Ausführen der Treffer Erkennung verwendet werden soll.

In C++ hat die [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur die folgende Definition.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



Im vorherigen Beispiel sind die linken und oberen Elemente die x-und y-Koordinaten der linken oberen Ecke eines umgebenden Rechtecks. Entsprechend bilden die Rechte und unteren Member die Koordinaten der unteren rechten Ecke. In der folgenden Abbildung wird gezeigt, wie diese Werte visualisiert werden können.

![Abbildung des Rechtecks, das durch die Werte Links, oben, rechts und unten begrenzt ist](images/rect.png)

Die Spalte mit Pixeln am rechten Rand und die Zeile der Pixel am unteren Rand sind nicht in der Rect enthalten. Wenn Sie z. b. ein Rect mit den Membern {10, 10, 138, 138} sperren, wird ein Objekt mit einer Breite und Höhe von 128 Pixel ausgegeben.

Im Interesse der Effizienz, Konsistenz und Benutzerfreundlichkeit können alle Direct3D Presentation-Funktionen mit Rechtecke verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
