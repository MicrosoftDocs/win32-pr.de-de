---
description: Eine Ellipse wird durch das umgebende Rechteck angegeben. In der folgenden Abbildung wird eine Ellipse zusammen mit dem umgebenden Rechteck gezeigt.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Ellipsen und Bögen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131345"
---
# <a name="ellipses-and-arcs"></a>Ellipsen und Bögen

Eine Ellipse wird durch das umgebende Rechteck angegeben. In der folgenden Abbildung wird eine Ellipse zusammen mit dem umgebenden Rechteck gezeigt.

![Abbildung einer Ellipse in einem umschließenden Rechteck](images/aboutgdip02-art05.png)

Zum Zeichnen einer Ellipse benötigen Sie ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) -Objekt. Das **Grafik** Objekt stellt die [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) -Methode bereit, und das **Pen** -Objekt speichert Attribute der Ellipse, z. b. Linienstärke und Farbe. Die Adresse des **Stift** Objekts wird als eines der Argumente an die DrawEllipse-Methode übermittelt. Die übrigen Argumente, die an die DrawEllipse-Methode übergeben werden, geben das Begrenzungs Rechteck für die Ellipse an. Im folgenden Beispiel wird eine Ellipse gezeichnet. das umgebende Rechteck hat eine Breite von 160, eine Höhe von 80 und eine linke obere Ecke von (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) ist eine überladene Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse, sodass Sie Sie mit Argumenten bereitstellen können. Beispielsweise können Sie ein [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt erstellen und einen Verweis auf das **Rect** -Objekt als Argument der DrawEllipse-Methode übergeben.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Ein Bogen ist ein Teil einer Ellipse. Zum Zeichnen eines Bogens wird die [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse aufgerufen. Die Parameter der DrawArc-Methode sind identisch mit den Parametern der [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) -Methode, mit dem Unterschied, dass DrawArc einen Anfangs Winkel und einen Pfeil Winkel erfordert. Im folgenden Beispiel wird ein Bogen mit einem Anfangs Winkel von 30 Grad und einem Mittelpunktswinkel von 180 Grad gezeichnet.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



Die folgende Abbildung zeigt den Bogen, die Ellipse und das umgebende Rechteck.

![Abbildung einer Ellipse in einem umgebenden Rechteck die untere linke Hälfte der Ellipse wird rot gezeichnet.](images/aboutgdip02-art06.png)

 

 



