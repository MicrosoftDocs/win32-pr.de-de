---
description: 'Windows GDI+ verwendet drei Koordinatenräume: Welt, Seite und Gerät.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Typen von Koordinatensystemen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120625"
---
# <a name="types-of-coordinate-systems"></a>Typen von Koordinatensystemen

Windows GDI+ verwendet drei Koordinatenräume: Welt, Seite und Gerät. Wenn Sie den Aufruf vornehmen, befinden sich `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` die Punkte, die Sie an die [**Graphics::D rawLine-Methode**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) übergeben – (0, 0) und (160, 80) – im Koordinatenraum der Welt. Bevor GDI+ die Linie auf dem Bildschirm zeichnen kann, durchlaufen die Koordinaten eine Sequenz von Transformationen. Eine Transformation konvertiert Weltkoordinaten in Seitenkoordinaten, und eine andere Transformation konvertiert Seitenkoordinaten in Gerätekoordinaten.

Angenommen, Sie möchten mit einem Koordinatensystem arbeiten, das seinen Ursprung im Textkörper des Clientbereichs anstelle der oberen linken Ecke hat. Angenommen, Sie möchten, dass der Ursprung 100 Pixel vom linken Rand des Clientbereichs und 50 Pixel vom oberen Rand des Clientbereichs entfernt ist. Die folgende Abbildung zeigt ein solches Koordinatensystem.

![Screenshot eines Fensters mit bezeichneten Koordinatenachsen](images/aboutgdip05-art01.png)

Wenn Sie den Aufruf `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` ausführen, erhalten Sie die in der folgenden Abbildung dargestellte Zeile.

![Screenshot des vorherigen Fensters, jedoch mit einer blauen Linie, die sich diagonal vom Ursprung erstreckt](images/aboutgdip05-art02.png)

Die Koordinaten der Endpunkte Ihrer Linie in den drei Koordinatenbereichen sind wie folgt:



| LeerZchn       |  Endpunktkoordinaten                       |
|--------|-------------------------|
| World  | (0, 0) bis (160, 80)     |
| Seite   | (100, 50) bis (260, 130) |
| Gerät | (100, 50) bis (260, 130) |



 

Beachten Sie, dass der Seitenkoordinatenraum seinen Ursprung in der oberen linken Ecke des Clientbereichs hat. Dies ist immer der Fall. Beachten Sie außerdem, dass die Gerätekoordinaten mit den Seitenkoordinaten identisch sind, da die Maßeinheit das Pixel ist. Wenn Sie die Maßeinheit auf einen anderen Als Pixel (z. B. Zoll) festlegen, unterscheiden sich die Gerätekoordinaten von den Seitenkoordinaten.

Die Transformation, die Weltkoordinaten Seitenkoordinaten zuordnt, wird als *Welttransformation* bezeichnet und von einem [**Graphics-Objekt**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwaltet. Im vorherigen Beispiel ist die Welttransformation eine Übersetzung von 100 Einheiten in x-Richtung und 50 Einheiten in y-Richtung. Im folgenden Beispiel wird die Welttransformation eines **Graphics-Objekts** festgelegt und dann dieses **Graphics-Objekt** verwendet, um die in der vorherigen Abbildung gezeigte Linie zu zeichnen.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



Die Transformation, die Seitenkoordinaten Gerätekoordinaten zuordnt, wird als *Seitentransformation* bezeichnet. Die [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) stellt vier Methoden zum Bearbeiten und Untersuchen der Seitentransformation bereit: [**Graphics::SetPageUnit,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) [**Graphics::GetPageUnit,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit) [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)und [**Graphics::GetPageScale.**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale) Die **Graphics-Klasse** stellt auch zwei Methoden bereit: [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) und [**Graphics::GetDpiY,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy)um die horizontalen und vertikalen Punkte pro Zoll des Anzeigegeräts zu untersuchen.

Sie können die [**Graphics::SetPageUnit-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) der [**Graphics-Klasse**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) verwenden, um eine Maßeinheit anzugeben. Das folgende Beispiel zeichnet eine Linie von (0, 0) bis (2, 1), wobei der Punkt (2, 1) 2 Zoll nach rechts und 1 Zoll vom Punkt (0, 0) nach unten liegt.


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Wenn Sie beim Erstellen des Stifts keine Stiftbreite angeben, wird im vorherigen Beispiel eine Linie gezeichnet, die einen Zoll breit ist. Sie können die Stiftbreite im zweiten Argument für den [**Stiftkonstruktor**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) angeben:
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Wenn angenommen wird, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung hat, weisen die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinatenbereichen auf:



| LeerZchn       | Endpunktkoordinaten                    |
|--------|---------------------|
| World  | (0, 0) bis (2, 1)    |
| Seite   | (0, 0) bis (2, 1)    |
| Gerät | (0, 0, bis (192, 96) |



 

Sie können die Welt- und Seitentransformationen kombinieren, um eine Vielzahl von Effekten zu erzielen. Angenommen, Sie möchten Zoll als Maßeinheit verwenden und möchten, dass der Ursprung Ihres Koordinatensystems 2 Zoll vom linken Rand des Clientbereichs und 1/2 Zoll vom oberen Rand des Clientbereichs entfernt ist. Im folgenden Beispiel werden die Welt- und Seitentransformationen eines [**Graphics-Objekts**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) festgelegt und dann eine Linie von (0, 0) bis (2, 1) zeichnet.


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



Die folgende Abbildung zeigt die Linie und das Koordinatensystem.

![Screenshot des vorherigen Fensters, aber breiter, wobei die Achsen links positioniert und anders bezeichnet sind](images/aboutgdip05-art03.png)

Wenn angenommen wird, dass das Anzeigegerät 96 Punkte pro Zoll in horizontaler Richtung und 96 Punkte pro Zoll in vertikaler Richtung hat, weisen die Endpunkte der Linie im vorherigen Beispiel die folgenden Koordinaten in den drei Koordinatenbereichen auf:



| LeerZchn       | Endpunktkoordinaten                        |
|--------|-------------------------|
| World  | (0, 0) bis (2, 1)        |
| Seite   | (2, 0,5) bis (4, 1,5)    |
| Gerät | (192, 48) bis (384, 144) |



 

 

 
