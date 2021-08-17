---
description: Pfade werden durch Kombinieren von Linien, Rechtecke und einfachen Kurven gebildet. Erinnern Sie sich an die Übersicht über Vektorgrafiken, dass sich die folgenden grundlegenden Bausteine als am nützlichsten für das Zeichnen von Bildern erwiesen haben.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Pfade (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54dae290138314cac3dae8d259591939490764d371e9a2caf9423801e985ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695476"
---
# <a name="paths-gdi"></a>Pfade (GDI+)

Pfade werden durch Kombinieren von Linien, Rechtecke und einfachen Kurven gebildet. Erinnern Sie sich [an die Übersicht über Vektorgrafiken,](-gdiplus-overview-of-vector-graphics-about.md) dass sich die folgenden grundlegenden Bausteine als am nützlichsten für das Zeichnen von Bildern erwiesen haben.

-   Linien
-   Rechtecke
-   Ellipsen
-   Bögen
-   Polygone
-   Kardinalsplines
-   Bézier-Splines

In Windows GDI+ können Sie mit [**dem GraphicsPath-Objekt**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) eine Sequenz dieser Bausteine in einer einzelnen Einheit sammeln. Die gesamte Sequenz von Linien, Rechtecke, Polygonen und Kurven kann dann mit einem Aufruf der [**Graphics::D rawPath-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) der [**Graphics-Klasse gezeichnet**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) werden. Die folgende Abbildung zeigt einen Pfad, der durch Kombinieren einer Linie, eines Bogens, einer Bézier-Spline und einer Kardinalspline erstellt wurde.

![Abbildung eines Pfads, der eine Linie, einen Bogen, eine Bézier-Spline und eine Kardinal-Spline kombiniert](images/aboutgdip02-art14.png)

Die [**GraphicsPath-Klasse**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) bietet die folgenden Methoden zum Erstellen einer Sequenz von elementen, die gezeichnet werden sollen: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (für Kardinalsplines) und [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Jede dieser Methoden ist überladen. Das bedeutet, dass jede Methode in mehreren Variationen mit unterschiedlichen Parameterlisten enthalten ist. Beispielsweise empfängt eine Variante der AddLine-Methode vier ganze Zahlen, und eine andere Variante der AddLine-Methode empfängt zwei [**Point-Objekte.**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)

Die Methoden zum Hinzufügen von Linien, Rechtecke und Bézier-Splines zu einem Pfad verfügen über Plural-Begleitmethoden, die dem Pfad in einem einzigen Aufruf mehrere Elemente hinzufügen: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))und [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)). Darüber hinaus verfügt die [AddCurve-Methode](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) über die Begleitmethode [AddClosedCurve,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint))die dem Pfad eine geschlossene Kurve hinzufügt.

Um einen Pfad zu zeichnen, benötigen Sie ein [**Graphics-Objekt,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ein [**Pen-Objekt**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) und ein [**GraphicsPath-Objekt.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) Das **Graphics-Objekt** stellt die [**Graphics::D rawPath-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) zur, und das **Pen-Objekt** speichert Attribute des Pfads, z. B. Linienbreite und Farbe. Das **GraphicsPath-Objekt** speichert die Sequenz von Linien, Rechtecke und Kurven, die den Pfad bilden. Die Adressen des **Pen-Objekts** und des **GraphicsPath-Objekts** werden als Argumente an die **Graphics::D rawPath-Methode** übergeben. Im folgenden Beispiel wird ein Pfad ge zeichnet, der aus einer Linie, einer Ellipse und einer Bézier-Spline besteht.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Die folgende Abbildung zeigt den Pfad.

![Abbildung eines Pfads, der aus einer Linie, einer Ellipse und einer Bézierspline besteht](images/aboutgdip02-art15.png)

Zusätzlich zum Hinzufügen von Linien, Rechtecke und Kurven zu einem Pfad können Sie einem Pfad Pfade hinzufügen. Dadurch können Sie vorhandene Pfade zu großen, komplexen Pfaden kombinieren. Der folgende Code fügt **"graphicsPath1"** und **"graphicsPath2"** **zu "myGraphicsPath" hinzu.** Der zweite Parameter der [**GraphicsPath::AddPath-Methode**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) gibt an, ob der hinzugefügte Pfad mit dem vorhandenen Pfad verbunden ist.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



Es gibt zwei weitere Elemente, die Sie einem Pfad hinzufügen können: Zeichenfolgen und Kreis. Ein Kreis ist ein Teil des Inneren einer Ellipse. Im folgenden Beispiel wird ein Pfad aus einem Bogen, einer Kardinalspline, einer Zeichenfolge und einem Kreis erstellt.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Die folgende Abbildung zeigt den Pfad. Beachten Sie, dass ein Pfad nicht verbunden werden muss. Der Bogen, die Kardinalspline, die Zeichenfolge und der Kreis sind getrennt.

![Abbildung eines Pfads, der aus getrennten Linien besteht: einem Bogen, einer Kardinalspline, einer Zeichenfolge und einem Kreis](images/aboutgdip02-art16.png)

 

 



