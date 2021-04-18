---
description: Die Grafikklasse ist das Herzstück von Windows GDI+. Um etwas zu zeichnen, erstellen Sie ein Grafik Objekt, legen seine Eigenschaften fest und rufen seine Methoden auf (DrawLine, DrawImage, DrawString und like).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Status eines Grafikobjekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555247"
---
# <a name="the-state-of-a-graphics-object"></a>Status eines Grafikobjekts

Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse ist das Herzstück von Windows GDI+. Um etwas zu zeichnen, erstellen Sie ein **Grafik** Objekt, legen seine Eigenschaften fest und rufen seine Methoden auf ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))und like).

Im folgenden Beispiel werden ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt erstellt und dann die [**Grafik::D rawrechteck**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Methode des **Grafik** Objekts aufgerufen:


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



Im vorangehenden Code gibt die [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) -Methode ein Handle für einen Gerätekontext zurück, und dieses Handle wird an den [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) -Konstruktor übergeben. Ein Gerätekontext ist eine (von Windows betreute) Struktur, die Informationen über das jeweilige angeverwendete Anzeigegerät enthält.

## <a name="graphics-state"></a>Grafikzustand

Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt bietet mehr als Zeichnungs Methoden, z. b. [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) und [drawrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)). Ein **Grafik** Objekt verwaltet auch den Grafik Zustand, der in die folgenden Kategorien unterteilt werden kann:

-   Ein Link zu einem Gerätekontext.
-   Qualitätseinstellungen
-   Transformationen
-   Ein Clippingbereich

### <a name="device-context"></a>Gerätekontext

Als Anwendungsprogrammierer müssen Sie sich keine Gedanken über die Interaktion zwischen einem [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und seinem Gerätekontext machen. Diese Interaktion wird von GDI+ im Hintergrund behandelt.

### <a name="quality-settings"></a>Qualitätseinstellungen

Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verfügt über mehrere Eigenschaften, die die Qualität der Elemente beeinflussen, die auf dem Bildschirm gezeichnet werden. Sie können diese Eigenschaften anzeigen und bearbeiten, indem Sie Get-und Set-Methoden aufrufen. Beispielsweise können Sie die [**Graphics:: settextrenderinghint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) -Methode aufrufen, um den Typ des Antialiasing (sofern vorhanden) anzugeben, der auf Text angewendet wird. Andere Set-Methoden, die die Qualität beeinflussen, sind [**Grafiken:: sezmuothingmode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: setcompositingmode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: setcompositingquality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)und [**Graphics:: setinterpolationmode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

Im folgenden Beispiel werden zwei Ellipsen gezeichnet, wobei der Glättungs Modus auf [* * * * SmoothingModeAntiAlias * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) und einen mit dem Glättungs Modus * * * [* smoothingmodehighspeed * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)festgelegt ist:


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Transformationen

Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verwaltet zwei Transformationen (Welt und Seite), die auf alle Elemente angewendet werden, die von diesem **Grafik** Objekt gezeichnet werden. Jede affine Transformation kann in der Welt Transformation gespeichert werden. Affine Transformationen umfassen Skalierung, Rotation, Spiegelung, Neigung und Übersetzung. Die Seiten Transformation kann für die Skalierung und für das Ändern von Einheiten (z. b. Pixel in Zoll) verwendet werden. Weitere Informationen zu Transformationen finden Sie unter [Koordinatensysteme und Transformationen](-gdiplus-coordinate-systems-and-transformations-about.md).

Im folgenden Beispiel werden die Welt-und Seiten Transformationen eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts festgelegt. Die Welt Transformation ist auf eine 30-Grad-Drehung festgelegt. Die Seiten Transformation wird so festgelegt, dass die an die zweite Grafik über gebenden Koordinaten [**:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) als Millimeter anstelle von Pixel behandelt werden. Der Code führt zwei identische Aufrufe der **Grafik aus::D rawellipse** -Methode. Die globale Transformation wird auf die ersten **Grafiken angewendet::D rawellipse** -Aufrufe, und beide Transformationen (Welt und Seite) werden auf die zweite **Grafik angewendet::D rawellipse** -Aufruf.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



Die folgende Abbildung zeigt die beiden Ellipsen. Beachten Sie, dass die 30-Grad-Drehung über den Ursprung des Koordinatensystems (obere linke Ecke des Client Bereichs) und nicht über die Mittelpunkte der Ellipsen liegt. Beachten Sie außerdem, dass die Stift Breite 1 für die erste Ellipse 1 Pixel und für die zweite Ellipse 1 Millimeter bedeutet.

![Screenshot eines Fensters mit einer kleinen, dünnen Ellipse und einer großen, dickeren Ellipse](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Clippingbereich

Ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt verwaltet einen Clippingbereich, der für alle Elemente gilt, die von diesem **Grafik** Objekt gezeichnet werden. Sie können den Clippingbereich festlegen, indem Sie die [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) -Methode aufrufen.

Im folgenden Beispiel wird ein Plus förmiger Bereich erstellt, indem die Union von zwei Rechtecke gebildet wird. Diese Region wird als Clippingbereich eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts bezeichnet. Anschließend zeichnet der Code zwei Zeilen, die auf das Innere des Clippingbereichs beschränkt sind.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



In der folgenden Abbildung sind die ausgeschnittenen Zeilen dargestellt.

![Abbildung einer farbigen Form, die von zwei diagonalen roten Linien überschritten wird](images/graphicsascon2.png)

 

 
