---
description: Um Linien und Rechtecke zu zeichnen, benötigen Sie ein Graphics-Objekt und ein Pen-Objekt. Das Graphics-Objekt stellt die DrawLine-Methode zur, und das Pen-Objekt speichert Features der Linie, z. B. Farbe und Breite.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Verwenden eines Stifts zum Zeichnen von Linien und Rechtecken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da700d61a5c8c1ce605678ea09aa540706d569361cebba8f5a93110ccdc304bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884860"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Verwenden eines Stifts zum Zeichnen von Linien und Rechtecken

Um Linien und Rechtecke zu zeichnen, benötigen Sie ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein [**Pen-Objekt.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Das **Graphics-Objekt** stellt die [DrawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) zur, und das **Pen-Objekt** speichert Features der Linie, z. B. Farbe und Breite.

Im folgenden Beispiel wird eine Linie von (20, 10) bis (300, 100) ge zeichnet. Angenommen, **Grafiken** sind ein vorhandenes [**Grafikobjekt.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



Die erste Code-Anweisung verwendet den [**Konstruktor der Pen-Klasse,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) um einen schwarzen Stift zu erstellen. Das einzige Argument, das an den **Stiftkonstruktor übergeben** wird, ist ein [**Color-Objekt.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Die Zum Erstellen des **Color-Objekts** verwendeten Werte (255, 0, 0, 0) entsprechen den Alpha-, Rot-, Grün- und Blaukomponenten der Farbe. Diese Werte definieren einen nicht transparenten schwarzen Stift.

Im folgenden Beispiel wird ein Rechteck mit seiner oberen linken Ecke bei (10, 10) ge zeichnet. Das Rechteck hat eine Breite von 100 und eine Höhe von 50. Das zweite Argument, das an den [**Stiftkonstruktor übergeben**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) wird, gibt an, dass die Stiftbreite 5 Pixel beträgt.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Wenn das Rechteck gezeichnet wird, wird der Stift auf der Begrenzung des Rechtecks zentriert. Da die Stiftbreite 5 beträgt, werden die Seiten des Rechtecks 5 Pixel breit gezeichnet, damit 1 Pixel an der Grenze selbst, 2 Pixel im Inneren und 2 Pixel außen gezeichnet werden. Weitere Informationen zur Stiftausrichtung finden Sie unter [Festlegen der Stiftbreite und Ausrichtung.](-gdiplus-setting-pen-width-and-alignment-use.md)

Die folgende Abbildung zeigt das resultierende Rechteck. Die gepunkteten Linien zeigen, wo das Rechteck gezeichnet worden wäre, wenn die Stiftbreite ein Pixel gewesen wäre. Die vergrößerte Ansicht der oberen linken Ecke des Rechtecks zeigt, dass die dichten schwarzen Linien auf diesen gepunkteten Linien zentriert sind.

![Abbildung eines Rechtecks, das mit einer dichten schwarzen Linie gezeichnet wird, die eine dünne, graue, gestrichelte Linie umgibt](images/pens1.png)

 

 



