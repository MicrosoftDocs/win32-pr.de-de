---
description: Die Graphics-Klasse steht im Mittelpunkt Windows GDI+. Um alles zu zeichnen, erstellen Sie ein Graphics-Objekt, legen dessen Eigenschaften fest und rufen dessen Methoden auf ( DrawLine, DrawImage, DrawString und ähnliches).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Status eines Grafikobjekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f68a2ba754aadc1f7d2572dcbc2ac40d08d7fe95d382ce60511cd72d441bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977330"
---
# <a name="the-state-of-a-graphics-object"></a>Status eines Grafikobjekts

Die [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) steht im Mittelpunkt Windows GDI+. Um alles zu zeichnen, erstellen Sie ein **Graphics-Objekt,** legen dessen Eigenschaften fest und rufen dessen Methoden auf ( [DrawLine,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) [DrawImage,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))und ähnliches).

Das folgende Beispiel erstellt ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und ein [**Pen-Objekt**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) und ruft dann die [**Graphics::D rawRectangle-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) des **Graphics-Objekts** auf:


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



Im vorangehenden Code gibt die [BeginPaint-Methode](/windows/win32/api/winuser/nf-winuser-beginpaint) ein Handle an einen Gerätekontext zurück, und dieses Handle wird an den [**Grafikkonstruktor**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) übergeben. Ein Gerätekontext ist eine Struktur (die von Windows verwaltet wird), die Informationen zum verwendeten Anzeigegerät enthält.

## <a name="graphics-state"></a>Grafikzustand

Ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) stellt mehr als Zeichnungsmethoden bereit, z. [B. DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) und [DrawRectangle.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) Ein **Graphics-Objekt** verwaltet auch den Grafikzustand, der in die folgenden Kategorien unterteilt werden kann:

-   Ein Link zu einem Gerätekontext
-   Qualitätseinstellungen
-   Transformationen
-   Ein Ausschneidebereich

### <a name="device-context"></a>Gerätekontext

Als Anwendungsprogrammierer müssen Sie sich keine Gedanken über die Interaktion zwischen einem [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und dessen Gerätekontext machen. Diese Interaktion wird von GDI+ im Hintergrund verarbeitet.

### <a name="quality-settings"></a>Quality Einstellungen

Ein [**Grafikobjekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verfügt über mehrere Eigenschaften, die die Qualität der Elemente beeinflussen, die auf dem Bildschirm gezeichnet werden. Sie können diese Eigenschaften anzeigen und bearbeiten, indem Sie get- und set-Methoden aufrufen. Beispielsweise können Sie die [**Graphics::SetTextRenderingHint-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) aufrufen, um den Typ des Antialiasings (falls vorhanden) anzugeben, das auf Text angewendet wird. Andere Set-Methoden, die die Qualität beeinflussen, sind [**Graphics::SetSmoothingMode,**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) [**Graphics::SetCompositingMode,**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode) [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)und [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

Das folgende Beispiel zeichnet zwei Ausellipsen: eine mit dem [Glättungsmodus "smoothingModeAntiAlias"](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) und eine mit dem Glättungsmodus ["SmoothingModeHighSpeed":](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Transformationen

Ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwaltet zwei Transformationen (Welt und Seite), die auf alle elemente angewendet werden, die von diesem **Graphics-Objekt** gezeichnet werden. Jede affine Transformation kann in der weltweiten Transformation gespeichert werden. Affine Transformationen umfassen Skalierung, Drehung, Reflektion, Skewing und Übersetzung. Die Seitentransformation kann für die Skalierung und zum Ändern von Einheiten (z. B. Pixel in Zoll) verwendet werden. Weitere Informationen zu Transformationen finden Sie unter [Koordinatensysteme und Transformationen.](-gdiplus-coordinate-systems-and-transformations-about.md)

Im folgenden Beispiel werden die Welt- und Seitentransformationen eines [**Graphics-Objekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) festgelegt. Die Welttransformation ist auf eine 30-Grad-Drehung festgelegt. Die Seitentransformation wird so festgelegt, dass die an die zweite [**Graphics::D rawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) übergebenen Koordinaten als Millimeter anstelle von Pixeln behandelt werden. Der Code ruft die **Graphics::D rawEllipse-Methode** auf zwei identische Weise auf. Die World-Transformation wird auf den ersten **Graphics::D rawEllipse-Aufruf** angewendet, und beide Transformationen (world und page) werden auf den zweiten **Graphics::D rawEllipse-Aufruf** angewendet.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



Die folgende Abbildung zeigt die beiden Ausellipsen. Beachten Sie, dass die 30-Grad-Drehung den Ursprung des Koordinatensystems (obere linke Ecke des Clientbereichs) und nicht die Mittelpunkte der Ellipsen betrifft. Beachten Sie auch, dass die Stiftbreite von 1 1 Pixel für die erste Ellipse und 1 Millimeter für die zweite Ellipse bedeutet.

![Screenshot eines Fensters mit einer kleinen, schlanken Ellipse und einer großen, breiteren Ellipse](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Beschneidungsregion

Ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwaltet einen Clippingbereich, der für alle von diesem **Graphics-Objekt** gezeichneten Elemente gilt. Sie können den Clippingbereich festlegen, indem Sie die [SetClip-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) aufrufen.

Im folgenden Beispiel wird ein plusförmiger Bereich erstellt, indem die Union von zwei Rechtecke gebildet wird. Dieser Bereich wird als Ausschneidebereich eines [**Graphics-Objekts**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) festgelegt. Anschließend zeichnet der Code zwei Linien, die auf das Innere des Ausschneidebereichs beschränkt sind.


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



Die folgende Abbildung zeigt die abgeschnittenen Zeilen.

![Abbildung einer farbigen Form, die durch zwei diagonale rote Linien gekreuzt wird](images/graphicsascon2.png)

 

 
