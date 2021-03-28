---
description: 'Ein B&\# 233; Zier-Splinekurve ist eine Kurve, die von vier Punkten angegeben wird: zwei Endpunkte (P1 und P2) und zwei Kontrollpunkte (C1 und C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Bézier-Splines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131385"
---
# <a name="bezier-splines"></a>Bézier-Splines

Eine Bézier-Spline ist eine Kurve, die von vier Punkten angegeben wird: zwei Endpunkte (P1 und P2) und zwei Kontrollpunkte (C1 und C2). Die Kurve beginnt bei P1 und endet bei P2. Die Kurve übergibt nicht die Steuerungs Punkte, aber die Steuerungs Punkte fungieren als Magnete, ziehen die Kurve in bestimmte Richtungen und beeinflussen die Kurven Kurven. In der folgenden Abbildung wird eine Bézier-Kurve zusammen mit den zugehörigen Endpunkten und Steuerungs Punkten dargestellt.

![Abbildung, die eine Bézier-Spline mit zwei Endpunkten und zwei Kontrollpunkten zeigt](images/aboutgdip02-art11a.png)

Beachten Sie, dass die Kurve bei P1 beginnt und zum Kontrollpunkt C1 wechselt. Die Tangente an der Kurve bei P1 ist die Linie, die von P1 bis C1 gezeichnet wird. Beachten Sie außerdem, dass die tangential Linie am Endpunkt P2 die Linie ist, die von C2 zu P2 gezeichnet wird.

Um einen Bézier-Spline zu zeichnen, benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt. Das **Grafik** Objekt stellt die [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt speichert Attribute der Kurve, z. b. Linienstärke und Farbe. Die Adresse des **Stift** Objekts wird als eines der Argumente an die DrawBezier-Methode übermittelt. Die übrigen Argumente, die an die DrawBezier-Methode übermittelt werden, sind die Endpunkte und die Steuerungs Punkte. Im folgenden Beispiel wird eine Bézier-Spline mit Startpunkt (0,0), Kontrollpunkten (40, 20) und (80, 150) und Endpunkt (100, 10) gezeichnet.


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



In der folgenden Abbildung sind die Kurve, die Kontrollpunkte und zwei Tangenten Linien dargestellt.

![Abbildung, die eine Bézier-Spline mit zwei Endpunkten, zwei Kontrollpunkten und zwei Tangenten Linien anzeigt](images/aboutgdip02-art12.png)

Die Bézier-Splines wurden ursprünglich von Pierre Bézier zum Entwerfen in der Automobilindustrie entwickelt. Sie haben sich in vielen Arten von computergestütztem Design bewährt und werden auch verwendet, um die Umschriften von Schriftarten zu definieren. Die Bézier-Splines können eine Vielzahl von Formen ergeben, von denen einige in der folgenden Abbildung dargestellt sind.

![Abbildung mit drei Bézier-Splines](images/aboutgdip02-art13.png)

 

 



