---
description: Pfade werden gebildet, indem Linien, Rechtecke und einfache Kurven kombiniert werden. Erinnern Sie sich aus der Übersicht über Vektorgrafiken, dass die folgenden grundlegenden Bausteine sich als besonders nützlich für das Zeichnen von Bildern erwiesen haben.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Pfade (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554529"
---
# <a name="paths-gdi"></a>Pfade (GDI+)

Pfade werden gebildet, indem Linien, Rechtecke und einfache Kurven kombiniert werden. Erinnern Sie sich aus der [Übersicht über Vektorgrafiken](-gdiplus-overview-of-vector-graphics-about.md) , dass die folgenden grundlegenden Bausteine sich als besonders nützlich für das Zeichnen von Bildern erwiesen haben.

-   Linien
-   Rechtecke
-   Ellipsen
-   Bögen
-   Polygone
-   Kardinale Splines
-   Bézier-Splines

In Windows GDI+ ermöglicht das [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt, eine Sequenz dieser Bausteine in einer einzelnen Einheit zu erfassen. Die gesamte Sequenz von Linien, Rechtecke, Polygonen und Kurven kann dann mit einem aufzurufenden [**:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse gezeichnet werden. Die folgende Abbildung zeigt einen Pfad, der durch das Kombinieren einer Linie, eines Bogens, eines Bézier-Spline und eines kardinaler Spline erstellt wurde.

![Abbildung eines Pfads, der eine Linie, einen Bogen, eine Bézier-Spline und einen kardinalspline kombiniert](images/aboutgdip02-art14.png)

Die [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Klasse stellt die folgenden Methoden zum Erstellen einer Sequenz von Elementen bereit, die gezeichnet werden sollen: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [addrechteck](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [addelta lipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (für Kardinal-Splines) und [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Jede dieser Methoden ist überladen. Das heißt, jede Methode kommt in verschiedene Variationen mit unterschiedlichen Parameterlisten. Beispielsweise empfängt eine Variation der AddLine-Methode vier ganze Zahlen, und eine andere Variation der AddLine-Methode empfängt zwei [**Punkt**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) Objekte.

Die Methoden zum Hinzufügen von Linien, Rechtecke und Bézier-Splines zu einem Pfad verfügen über Plural-Begleit Methoden, mit denen dem Pfad in einem einzelnen-Befehl mehrere Elemente hinzugefügt werden: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [addrechgles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))und [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)). Außerdem verfügt die [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) -Methode über eine Begleit Methode, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), die dem Pfad eine geschlossene Kurve hinzufügt.

Zum Zeichnen eines Pfads benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt und ein [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt. Das **Grafik** Objekt stellt die [**Grafik::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode bereit, und das **Stift** -Objekt speichert Attribute des Pfads, z. b. Linienstärke und Farbe. Das **GraphicsPath** -Objekt speichert die Sequenz von Linien, Rechtecke und Kurven, die den Pfad bilden. Die Adressen des **Stift** Objekts und des **GraphicsPath** -Objekts werden als Argumente an die **Grafik::D rawpath** -Methode übergeben. Im folgenden Beispiel wird ein Pfad gezeichnet, der aus einer Zeile, einer Ellipse und einem Bézier-Spline besteht.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



In der folgenden Abbildung ist der Pfad dargestellt.

![Abbildung eines Pfads, der aus einer Zeile, einer Ellipse und einer Bézier-Spline besteht](images/aboutgdip02-art15.png)

Zusätzlich zum Hinzufügen von Linien, Rechtecke und Kurven zu einem Pfad können Sie Pfade zu einem Pfad hinzufügen. Dies ermöglicht Ihnen das Kombinieren vorhandener Pfade, um große und komplexe Pfade zu bilden. Der folgende Code fügt " **graphicsPath1** " und " **graphicsPath2** " zu **myGraphicsPath** hinzu. Der zweite Parameter der [**GraphicsPath:: Addpath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) -Methode gibt an, ob der hinzugefügte Pfad mit dem vorhandenen Pfad verbunden ist.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



Es gibt zwei weitere Elemente, die Sie einem Pfad hinzufügen können: Strings und Pies. Ein Kreis ist ein Teil des Inneren einer Ellipse. Im folgenden Beispiel wird ein Pfad von einem Bogen, ein kardinaler Spline, eine Zeichenfolge und ein Kreis erstellt.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



In der folgenden Abbildung ist der Pfad dargestellt. Beachten Sie, dass für einen Pfad keine Verbindung hergestellt werden muss. der Bogen, der kardinalspline, die Zeichenfolge und der Kreis werden getrennt.

![Abbildung eines Pfads, der aus getrennten Zeilen besteht: einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis](images/aboutgdip02-art16.png)

 

 



