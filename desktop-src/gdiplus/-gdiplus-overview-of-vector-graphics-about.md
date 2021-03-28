---
description: Windows GDI+ zeichnet Linien, Rechtecke und andere Abbildungen in einem Koordinatensystem.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Übersicht über Vektorgrafiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9bfe98585ef8e073cf1c563c237436b7c982bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556169"
---
# <a name="overview-of-vector-graphics"></a>Übersicht über Vektorgrafiken

Windows GDI+ zeichnet Linien, Rechtecke und andere Abbildungen in einem Koordinatensystem. Sie können aus einer Vielzahl von Koordinatensystemen auswählen, aber das Standard Koordinatensystem hat den Ursprung in der oberen linken Ecke, wobei die x-Achse nach rechts und die y-Achse nach unten zeigt. Die Maßeinheit im Standard Koordinatensystem ist das Pixel.

![Abbildung eines Koordinatensystems, bei dem die x-Achse nach rechts und die y-Achse nach unten erweitert wird](images/aboutgdip02-art01.png)

Ein Computermonitor erstellt seine Anzeige auf einem rechteckigen Array von Punkten, die als Bildelemente oder Pixel bezeichnet werden. Die Anzahl der Pixel, die auf dem Bildschirm angezeigt werden, variiert von einem Monitor zum nächsten, und die Anzahl der Pixel, die auf einem einzelnen Monitor angezeigt werden, kann normalerweise in gewissem Umfang vom Benutzer konfiguriert werden.

![Abbildung eines rechteckigen Rasters mit drei Zellen in diesem Raster, die durch Ihre Koordinaten gekennzeichnet sind](images/aboutgdip02-art02.png)

Wenn Sie GDI+ zum Zeichnen einer Linie, eines Rechtecks oder einer Kurve verwenden, stellen Sie bestimmte Schlüsselinformationen über das zu zeichnende Element bereit. Sie können z. b. eine Zeile angeben, indem Sie zwei Punkte bereitstellen, und Sie können ein Rechteck angeben, indem Sie einen Punkt, eine Höhe und eine Breite angeben. GDI+ funktioniert in Verbindung mit der Anzeigetreiber Software, um zu bestimmen, welche Pixel eingeschaltet werden müssen, um die Linie, das Rechteck oder die Kurve anzuzeigen. Die folgende Abbildung zeigt die Pixel, die aktiviert werden, um eine Linie vom Punkt (4, 2) bis zum Punkt (12, 8) anzuzeigen.

![Abbildung mit einem rechteckigen Raster mit gefüllten Zellen, die eine Linie zwischen zwei Endpunkten anzeigen](images/aboutgdip02-art03.png)

Im Laufe der Zeit haben sich bestimmte grundlegende Bausteine als besonders hilfreich für das Erstellen zweidimensionaler Bilder bewährt. Diese Bausteine, die alle von GDI+ unterstützt werden, sind in der folgenden Liste aufgeführt:

-   Linien
-   Rechtecke
-   Ellipsen
-   Bögen
-   Polygone
-   Kardinale Splines
-   Bézier-Splines

Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse in GDI+ bietet die folgenden Methoden zum Zeichnen der Elemente in der vorherigen Liste: [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (für Kardinal-Splines) und [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Jede dieser Methoden ist überladen. Das heißt, jede Methode kommt in verschiedene Variationen mit unterschiedlichen Parameterlisten. Beispielsweise empfängt eine Variation der DrawLine-Methode die Adresse eines [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Objekts und vier ganze Zahlen, während eine andere Variation der DrawLine-Methode die Adresse eines **Stift** Objekts und zwei [**Punkt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) Objekt Verweise empfängt.

Die Methoden zum Zeichnen von Linien, Rechtecke und Bézier-Splines verfügen über Plural-Begleit Methoden, die mehrere Elemente in einem einzelnen-Befehl zeichnen: [DrawLines](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)), [drawrechgles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))und [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)). Außerdem verfügt die [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) -Methode über die Begleit Methode [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)), die eine Kurve schließt, indem der Endpunkt der Kurve mit dem Ausgangspunkt verbunden wird.

Alle Zeichnungs Methoden der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse funktionieren in Verbindung mit einem [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt. Daher müssen Sie zum Zeichnen von etwas mindestens zwei Objekte erstellen: ein **Grafik** Objekt und ein **Pen** -Objekt. Das **Pen** -Objekt speichert Attribute des zu Zeichenden Elements, z. b. Linienstärke und Farbe. Die Adresse des **Stift** Objekts wird als eines der Argumente an die Zeichnungs Methode übermittelt. Beispielsweise empfängt eine Variation der [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Methode die Adresse eines **Stift** Objekts und vier ganze Zahlen, wie im folgenden Code gezeigt, der ein Rechteck mit einer Breite von 100, eine Höhe von 50 und eine obere linke Ecke von (20, 10) zeichnet.


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



