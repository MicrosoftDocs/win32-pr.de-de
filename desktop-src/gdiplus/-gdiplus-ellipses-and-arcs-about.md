---
description: Eine Ellipse wird durch das umgebundene Rechteck angegeben. Die folgende Abbildung zeigt eine Ellipse zusammen mit dem umgebundenen Rechteck.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Ellipsen und Bögen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadd0a34107681d2d155ead5d4f80b7208b8926603f21fa4541d502886edaf73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036748"
---
# <a name="ellipses-and-arcs"></a>Ellipsen und Bögen

Eine Ellipse wird durch das umgebundene Rechteck angegeben. Die folgende Abbildung zeigt eine Ellipse zusammen mit dem umgebundenen Rechteck.

![Abbildung einer Ellipse, die in einem umschließenden Rechteck eingeschlossen ist](images/aboutgdip02-art05.png)

Um eine Ellipse zu zeichnen, benötigen Sie ein [**Graphics-Objekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein [**Pen-Objekt.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Das **Graphics-Objekt** stellt die [DrawEllipse-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) zur Lage, und das **Pen-Objekt** speichert Attribute der Ellipse, z. B. Linienbreite und Farbe. Die Adresse des **Pen-Objekts** wird als eines der Argumente an die DrawEllipse-Methode übergeben. Die verbleibenden Argumente, die an die DrawEllipse-Methode übergeben werden, geben das umgebundene Rechteck für die Ellipse an. Im folgenden Beispiel wird eine Ellipse ge zeichnet. Das umgebundene Rechteck hat eine Breite von 160, eine Höhe von 80 und eine obere linke Ecke von (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawEllipse ist](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) eine überladene Methode der [**Graphics-Klasse,**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) daher gibt es mehrere Möglichkeiten, sie mit Argumenten zu versorgen. Beispielsweise können Sie ein [**Rect-Objekt**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) erstellen und einen Verweis auf das **Rect-Objekt** als Argument an die DrawEllipse-Methode übergeben.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Ein Bogen ist ein Teil einer Ellipse. Um einen Bogen zu zeichnen, rufen Sie die [DrawArc-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) auf. Die Parameter der DrawArc-Methode sind identisch mit den Parametern der [DrawEllipse-Methode,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) mit der Ausnahme, dass DrawArc einen Startwinkel und einen Sweepwinkel erfordert. Im folgenden Beispiel wird ein Bogen mit einem Anfangswinkel von 30 Grad und einem Sweepwinkel von 180 Grad ge zeichnet.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



Die folgende Abbildung zeigt den Bogen, die Ellipse und das umgebundene Rechteck.

![Abbildung einer Ellipse innerhalb eines umgebundenen Rechtecks; Die untere linke Hälfte der Ellipse wird rot gezeichnet.](images/aboutgdip02-art06.png)

 

 



