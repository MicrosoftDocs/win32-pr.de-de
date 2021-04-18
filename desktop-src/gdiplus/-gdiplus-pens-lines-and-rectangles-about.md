---
description: Zum Zeichnen von Linien mit Windows GDI+ müssen Sie ein Grafik Objekt und ein Pen-Objekt erstellen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Stifte, Linien und Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978960"
---
# <a name="pens-lines-and-rectangles"></a>Stifte, Linien und Rechtecke

Zum Zeichnen von Linien mit Windows GDI+ müssen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellen. Das **Grafik** Objekt stellt die Methoden bereit, die die Zeichnung tatsächlich durchführen, und das **Stift** -Objekt speichert Attribute der Zeile, z. b. Farbe, Breite und Stil. Das Zeichnen einer Linie ist einfach eine Frage des Aufrufs der [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode des **Grafik** Objekts. Die Adresse des **Stift** Objekts wird als eines der Argumente an die DrawLine-Methode übermittelt. Im folgenden Beispiel wird eine Linie vom Punkt (4, 2) bis zum Punkt (12, 6) gezeichnet.


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) ist eine überladene Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse, sodass Sie Sie mit Argumenten bereitstellen können. Beispielsweise können Sie zwei [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) -Objekte erstellen und Verweise auf die **Point** -Objekte als Argumente an die DrawLine-Methode übergeben.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



Sie können bestimmte Attribute angeben, wenn Sie ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellen. Beispielsweise können Sie mit einem [Stift](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) -Konstruktor Farbe und Breite angeben. Im folgenden Beispiel wird eine blaue Linie der Breite 2 von (0,0) bis (60, 30) gezeichnet.


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



Das [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt verfügt auch über Attribute, wie z. b. den Dash-Stil, mit denen Sie Features der Linie angeben können. Im folgenden Beispiel wird z. b. eine gestrichelte Linie von (100, 50) zu (300, 80) gezeichnet.


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



Sie können verschiedene Methoden des [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekts verwenden, um viele weitere Attribute der Zeile festzulegen. Die [**Pen:: setstartcap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) -Methode und die [**Pen:: setendcap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) -Methode geben die Darstellung der Zeilenenden an. die enden können flach, quadratisch, gerundet, dreieckig oder eine benutzerdefinierte Form sein. Mit der Methode [**Pen:: setlinejoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) können Sie angeben, ob verbundene Linien gezippt (mit spitzen Ecken verknüpft), geglättet, gerundet oder abgeschnitten werden. In der folgenden Abbildung werden Zeilen mit verschiedenen Obergrenzen und joinstilen dargestellt.

![Abbildung von zwei Zeilen, die gerundete und zirkuläre enden, gerundete und unterteilte Ecken und zwei Pfeil Stile demonstrieren](images/aboutgdip02-art04.png)

Zeichnungs Rechtecke mit GDI+ ähneln Zeichnungslinien. Zum Zeichnen eines Rechtecks benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt. Das **Grafik** Objekt stellt eine [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt speichert Attribute, z. b. Linienstärke und Farbe. Die Adresse des **Stift** Objekts wird als eines der Argumente an die drawrechteck-Methode übermittelt. Im folgenden Beispiel wird ein Rechteck mit der linken oberen Ecke bei (100, 50), einer Breite von 80 und einer Höhe von 40 gezeichnet.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[Drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) ist eine überladene Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen. Beispielsweise können Sie ein [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt erstellen und einen Verweis auf das **Rect** -Objekt als Argument an die drawrechteck-Methode übergeben.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Ein [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) -Objekt verfügt über Methoden zum Bearbeiten und Sammeln von Informationen über das Rechteck. Beispielsweise ändern die Methoden zum [aufblasen](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) und [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) die Größe und Position des Rechtecks. Die [**Rect:: IntersectWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) -Methode gibt Aufschluss darüber, ob das Rechteck ein anderes angegebenes Rechteck überschneidet, und die [enthält](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) -Methode gibt an, ob sich ein bestimmter Punkt innerhalb des Rechtecks befindet.

 

 
