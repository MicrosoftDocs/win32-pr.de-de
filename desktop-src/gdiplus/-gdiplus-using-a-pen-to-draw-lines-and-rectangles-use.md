---
description: Zum Zeichnen von Linien und Rechtecke benötigen Sie ein Grafik Objekt und ein Pen-Objekt. Das Grafik Objekt stellt die DrawLine-Methode bereit, und das Pen-Objekt speichert Features der Linie, z. b. Farbe und Breite.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Verwenden eines Stifts zum Zeichnen von Linien und Rechtecken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959444"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Verwenden eines Stifts zum Zeichnen von Linien und Rechtecken

Zum Zeichnen von Linien und Rechtecke benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt. Das **Grafik** Objekt stellt die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt speichert Features der Linie, z. b. Farbe und Breite.

Im folgenden Beispiel wird eine Zeile von (20, 10) nach (300, 100) gezeichnet. Angenommen, **Grafik** ist ein vorhandenes [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt.


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



Die erste Code Anweisung verwendet den [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Klassenkonstruktor, um einen schwarzen Stift zu erstellen. Das einzige Argument, das an den **Stift** -Konstruktor übergeben wird, ist ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt. Die Werte, die verwendet werden, um das **Color** -Objekt – (255, 0, 0, 0) – zu erstellen, entsprechen den Alpha-, rot-, grün-und blauen Komponenten der Farbe. Diese Werte definieren einen nicht transparenten schwarzen Stift.

Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (10, 10) gezeichnet. Das Rechteck hat eine Breite von 100 und eine Höhe von 50. Das zweite Argument, das an den [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Konstruktor übergeben wird, gibt an, dass die Stift Breite 5 Pixel beträgt.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Wenn das Rechteck gezeichnet wird, wird der Stift auf die Begrenzung des Rechtecks zentriert. Da die Stift Breite 5 beträgt, werden die Seiten des Rechtecks 5 Pixel breit gezeichnet, sodass 1 Pixel an der Grenze selbst gezeichnet wird, 2 Pixel im inneren gezeichnet werden und 2 Pixel auf der Außenseite gezeichnet werden. Weitere Informationen zur Ausrichtung von Pen finden Sie unter [Festlegen der Stift Breite und-Ausrichtung](-gdiplus-setting-pen-width-and-alignment-use.md).

Die folgende Abbildung zeigt das resultierende Rechteck. Die gepunkteten Linien zeigen an, wo das Rechteck gezeichnet worden wäre, wenn die Stift Breite ein Pixel gewesen wäre. Die erweiterte Ansicht der oberen linken Ecke des Rechtecks zeigt, dass die dicken schwarzen Linien auf diese gepunkteten Linien zentriert sind.

![Abbildung eines Rechtecks, das mit einer dicken schwarzen Linie gezeichnet wird, die eine dünne, graue, gestrichelte Linie umgibt](images/pens1.png)

 

 



