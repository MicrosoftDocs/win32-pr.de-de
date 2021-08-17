---
description: Windows GDI+ zeichnet Linien, Rechtecke und andere Abbildungen auf einem Koordinatensystem.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Übersicht über Vektorgrafiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33566b5d1d683c87ea1f6858abcc6ae375ce09b71e0ac74711118e92bca656c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695658"
---
# <a name="overview-of-vector-graphics"></a>Übersicht über Vektorgrafiken

Windows GDI+ zeichnet Linien, Rechtecke und andere Abbildungen auf einem Koordinatensystem. Sie können aus einer Vielzahl von Koordinatensystemen wählen, aber das Standardkoordinatensystem hat den Ursprung in der oberen linken Ecke, wobei die x-Achse auf die rechte Seite und die y-Achse nach unten zeigen. Die Maßeinheit im Standardkoordinatensystem ist das Pixel.

![Abbildung eines Koordinatensystems mit der x-Achse, die sich nach rechts und der y-Achse nach unten erstreckt](images/aboutgdip02-art01.png)

Ein Computermonitor erstellt seine Anzeige auf einem rechteckigen Array von Punkten, die als Bildelemente oder Pixel bezeichnet werden. Die Anzahl der auf dem Bildschirm angezeigten Pixel variiert von Monitor zu Monitor, und die Anzahl der Pixel, die auf einem einzelnen Monitor angezeigt werden, kann vom Benutzer in der Regel in gewissem Umfang konfiguriert werden.

![Abbildung eines rechteckigen Rasters mit drei Zellen in diesem Raster, die durch ihre Koordinaten gekennzeichnet sind](images/aboutgdip02-art02.png)

Wenn Sie GDI+ verwenden, um eine Linie, ein Rechteck oder eine Kurve zu zeichnen, geben Sie bestimmte Schlüsselinformationen zum zu zeichnenden Element an. Beispielsweise können Sie eine Linie angeben, indem Sie zwei Punkte angeben, und Sie können ein Rechteck angeben, indem Sie einen Punkt, eine Höhe und eine Breite angeben. GDI+ arbeitet mit der Anzeigetreibersoftware zusammen, um zu bestimmen, welche Pixel aktiviert werden müssen, um die Linie, das Rechteck oder die Kurve anzuzeigen. Die folgende Abbildung zeigt die Pixel, die aktiviert sind, um eine Linie vom Punkt (4, 2) bis zum Punkt (12, 8) anzuzeigen.

![Abbildung eines rechteckigen Rasters mit gefüllten Zellen, um eine Linie zwischen zwei Endpunkten anzugeben](images/aboutgdip02-art03.png)

Im Laufe der Zeit haben sich bestimmte grundlegende Bausteine als besonders nützlich für die Erstellung von zweidimensionalen Bildern erwiesen. Diese Bausteine, die alle von GDI+ unterstützt werden, sind in der folgenden Liste aufgeführt:

-   Linien
-   Rechtecke
-   Ellipsen
-   Bögen
-   Polygone
-   Kardinale Splines
-   Bézier-Splines

Die [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in GDI+ stellt die folgenden Methoden zum Zeichnen der Elemente in der vorherigen Liste bereit: [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (für Kardinalsplines) und [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Jede dieser Methoden ist überladen. Das heißt, jede Methode weist mehrere Variationen mit unterschiedlichen Parameterlisten auf. Beispielsweise empfängt eine Variation der DrawLine-Methode die Adresse eines [**Pen-Objekts**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) und vier ganze Zahlen, während eine andere Variation der DrawLine-Methode die Adresse eines **Stiftobjekts** und zwei [**Point-Objektverweise**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) empfängt.

Die Methoden zum Zeichnen von Linien, Rechtecke und Béziersplines verfügen über Plural-Begleitmethoden, die mehrere Elemente in einem einzigen Aufruf zeichnen: [DrawLines](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)), [DrawRectangles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))und [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)). Außerdem verfügt die [DrawCurve-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) über die Begleitmethode [DrawClosedCurve,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint))die eine Kurve schließt, indem der Endpunkt der Kurve mit dem Startpunkt verbunden wird.

Alle Zeichnungsmethoden der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) funktionieren in Verbindung mit einem [**Stiftobjekt.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Daher müssen Sie mindestens zwei Objekte erstellen, um etwas zu zeichnen: ein **Graphics-Objekt** und ein **Pen-Objekt.** Das **Stiftobjekt** speichert Attribute des zu zeichnenden Elements, z. B. Linienbreite und Farbe. Die Adresse des **Stiftobjekts** wird als eines der Argumente an die Zeichnungsmethode übergeben. Beispielsweise empfängt eine Variation der [DrawRectangle-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) die Adresse eines **Stiftobjekts** und vier ganze Zahlen, wie im folgenden Code gezeigt, der ein Rechteck mit einer Breite von 100, einer Höhe von 50 und einer oberen linken Ecke von (20, 10) zeichnet.


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



