---
description: Zum Zeichnen von Linien mit Windows GDI+ müssen Sie ein Grafikobjekt und ein Stiftobjekt erstellen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Stifte, Linien und Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ac54d1e98a617492aa6f5f1194767fc56a34ffcaaee71ba71753dda08f8bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359590"
---
# <a name="pens-lines-and-rectangles"></a>Stifte, Linien und Rechtecke

Zum Zeichnen von Linien mit Windows GDI+ müssen Sie ein [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein [**Stiftobjekt**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) erstellen. Das **Graphics-Objekt** stellt die Methoden zur eigentlichen Zeichnung zur Vervollst. Das **Pen-Objekt** speichert Attribute der Linie, z. B. Farbe, Breite und Stil. Das Zeichnen einer Linie ist einfach eine Frage des Aufrufs der [DrawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) des **Graphics-Objekts.** Die Adresse des **Pen-Objekts** wird als eines der Argumente an die DrawLine-Methode übergeben. Im folgenden Beispiel wird eine Linie vom Punkt (4, 2) bis zum Punkt (12, 6) ge zeichnet.


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) ist eine überladene Methode der [**Graphics-Klasse,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) daher gibt es mehrere Möglichkeiten, sie mit Argumenten zu versorgen. Beispielsweise können Sie zwei [**Point-Objekte**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) erstellen und Verweise auf die **Point-Objekte** als Argumente an die DrawLine-Methode übergeben.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



Sie können bestimmte Attribute angeben, wenn Sie ein [**Stiftobjekt**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) erstellen. Beispielsweise können Sie mit einem [Stiftkonstruktor](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) Farbe und Breite angeben. Im folgenden Beispiel wird eine blaue Linie der Breite 2 von (0, 0) bis (60, 30) ge zeichnet.


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



Das [**Pen-Objekt**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) verfügt auch über Attribute, z. B. das Bindestrichformat, mit denen Sie Features der Linie angeben können. Im folgenden Beispiel wird beispielsweise eine gestrichelte Linie von (100, 50) bis (300, 80) gestrichelt.


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



Sie können verschiedene Methoden des [**Pen-Objekts**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) verwenden, um viele weitere Attribute der Zeile zu setzen. Die [**Methoden Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) und [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) geben die Darstellung der Zeilenenden an. Die Enden können flach, quadratisch, abgerundet, dreieckig oder eine benutzerdefinierte Form sein. Mit [**der Pen::SetLineJoin-Methode**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) können Sie angeben, ob verbundene Linien geergt (mit spitzen Ecken verknüpft), abschrägt, gerundet oder abgeschnitten werden. Die folgende Abbildung zeigt Linien mit verschiedenen Stilen für Verschluss- und Joins.

![Abbildung einer zwei Linien, die abgerundete und kreisförmige Enden, abgerundete und miterbierte Ecken und zwei Pfeilstile veranschaulichen](images/aboutgdip02-art04.png)

Das Zeichnen von Rechtecke mit GDI+ ähnelt dem Zeichnen von Linien. Um ein Rechteck zu zeichnen, benötigen Sie ein [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein [**Stiftobjekt.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Das **Graphics-Objekt** bietet eine [DrawRectangle-Methode,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) und das **Pen-Objekt** speichert Attribute wie Linienbreite und Farbe. Die Adresse des **Pen-Objekts** wird als eines der Argumente an die DrawRectangle-Methode übergeben. Im folgenden Beispiel wird ein Rechteck mit seiner oberen linken Ecke bei (100, 50), einer Breite von 80 und einer Höhe von 40 ge zeichnet.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[DrawRectangle ist](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) eine überladene Methode der [**Graphics-Klasse,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) daher gibt es mehrere Möglichkeiten, sie mit Argumenten zu versorgen. Beispielsweise können Sie ein [**Rect-Objekt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) erstellen und einen Verweis auf das **Rect-Objekt** als Argument an die DrawRectangle-Methode übergeben.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Ein [**Rect-Objekt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) verfügt über Methoden zum Bearbeiten und Sammeln von Informationen über das Rechteck. Beispielsweise ändern die [Methoden Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) und [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) die Größe und Position des Rechtecks. Die [**Rect::IntersectsWith-Methode**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) teilt Ihnen mit, ob das Rechteck ein anderes bestimmtes Rechteck schneidet, und die [Contains-Methode](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) gibt an, ob sich ein angegebener Punkt innerhalb des Rechtecks befindet.

 

 
