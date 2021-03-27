---
description: Wenn Sie Windows GDI+ zum Zeichnen einer Linie verwenden, geben Sie den Ausgangspunkt und den Endpunkt der Linie an, aber Sie müssen keine Informationen über die einzelnen Pixel in der Zeile angeben.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Antialiasing bei Linien und Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755776"
---
# <a name="antialiasing-with-lines-and-curves"></a>Antialiasing bei Linien und Kurven

Wenn Sie Windows GDI+ zum Zeichnen einer Linie verwenden, geben Sie den Ausgangspunkt und den Endpunkt der Linie an, aber Sie müssen keine Informationen über die einzelnen Pixel in der Zeile angeben. GDI+ funktioniert in Verbindung mit der Anzeigetreiber Software, um zu bestimmen, welche Pixel eingeschaltet werden, um die Zeile auf einem bestimmten Anzeigegerät anzuzeigen.

Angenommen, eine gerade rote Linie wechselt vom Punkt (4, 2) bis zum Punkt (16, 10). Angenommen, das Koordinatensystem hat seinen Ursprung in der oberen linken Ecke, und die Maßeinheit ist das Pixel. Nehmen Sie auch an, dass die x-Achse nach rechts und die y-Achse nach unten zeigt. Die folgende Abbildung zeigt eine vergrößerte Ansicht der roten Linie, die auf einem mehrfarbigen Hintergrund gezeichnet wird.

![Darstellung der in einem mehrfarbigen Hintergrund ausgeführten roten Pixel](images/aboutgdip02-art33.png)

Beachten Sie, dass die zum Rendering der Zeile verwendeten roten Pixel nicht transparent sind. Es gibt keine teilweise transparenten Pixel, die an der Anzeige der Zeile beteiligt sind. Diese Art von Zeilen Rendering gibt der Linie eine verzweigte Darstellung, und die Linie sieht etwas wie eine Treppe aus. Diese Methode zum Darstellen einer Linie mit einer Treppe wird als Aliasing bezeichnet. die Treppe ist ein Alias für die theoretische Zeile.

Ein anspruchsvolleres Verfahren zum Rendern einer Linie besteht darin, teilweise transparente Pixel zusammen mit reinen roten Pixeln zu verwenden. Pixel werden auf "rein rot" oder auf eine Mischung aus rot und die Hintergrundfarbe festgelegt, je nachdem, wie nah Sie auf die Linie sind. Diese Art des Renderings wird als Antialiasing bezeichnet und führt zu einer Zeile, die das menschliche Auge als nahtloser ansieht. In der folgenden Abbildung wird gezeigt, wie bestimmte Pixel mit dem Hintergrund kombiniert werden, um eine Zeile mit einem-oder-Alias zu bilden.

![Abbildung, die Pixel zeigt, die im gleichen Hintergrund Schattierungen von rot sind](images/aboutgdip02-art34.png)

Antialiasing (Glättung) kann auch auf Kurven angewendet werden. Die folgende Abbildung zeigt eine vergrößerte Ansicht einer gegläten Ellipse.

![Abbildung einer Ellipse, die aus unterschiedlichen Schattierungen von blauen Pixeln in einem weißen Hintergrund besteht](images/aboutgdip02-art35.png)

In der folgenden Abbildung wird die gleiche Ellipse in der tatsächlichen Größe angezeigt, einmal ohne Antialiasing und einmal mit Antialiasing.

![Screenshot von zwei Ellipsen: der eine mit Antialiasing wird benachrichtigt.](images/aboutgdip02-art36.png)

Zum Zeichnen von Linien und Kurven, die Antialiasing verwenden, erstellen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und übergeben Sie " *SmoothingModeAntiAlias* " an die zugehörige [**Grafik:: sezmuothingmode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) -Methode. Anschließend wird eine der Zeichnungs Methoden desselben **Grafik** Objekts aufgerufen.


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



" **SmoothingModeAntiAlias** " ist ein Element der " [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) "-Enumeration.

 

 



