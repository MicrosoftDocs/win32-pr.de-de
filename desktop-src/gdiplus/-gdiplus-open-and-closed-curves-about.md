---
description: 'Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Geöffnete und geschlossene Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383f7c68909a73291c00c6e760d1cc6554b061d5749b33e6e90ba3a986c71906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885125"
---
# <a name="open-and-closed-curves"></a>Geöffnete und geschlossene Kurven

Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.

![Abbildung einer offenen Kurve (einer gekrümmten Linie) und einer geschlossenen Kurve (kontur einer Form)](images/aboutgdip02-art24.png)

Geschlossene Kurven verfügen über ein Innere und können daher mit einem Pinsel gefüllt werden. Die [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in Windows GDI+ stellt die folgenden Methoden zum Füllen geschlossener Abbildungen und Kurven bereit: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)und [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). Wenn Sie eine dieser Methoden aufrufen, müssen Sie die Adresse eines der spezifischen Pinseltypen ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)oder [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) als Argument übergeben.

Die [FillPie-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) ist eine Ergänzung zur [DrawArc-Methode.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) So wie die DrawArc-Methode einen Teil der Kontur einer Ellipse zeichnet, füllt die FillPie-Methode einen Teil des Inneren einer Ellipse aus. Das folgende Beispiel zeichnet einen Bogen und füllt den entsprechenden Teil des Inneren der Ellipse aus.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



Die folgende Abbildung zeigt den Bogen und den gefüllten Kreis.

![Abbildung eines Segments einer ausgefüllten Ellipse](images/aboutgdip02-art25.png)

Die [FillClosedCurve-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) ist eine Ergänzung zur [DrawClosedCurve-Methode.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) Beide Methoden schließen die Kurve automatisch, indem sie den Endpunkt mit dem Startpunkt verbinden. Das folgende Beispiel zeichnet eine Kurve, die durch (0, 0), (60, 20) und (40, 50) verläuft. Anschließend wird die Kurve automatisch durch Verbinden (40, 50) mit dem Startpunkt (0, 0) geschlossen, und das Innere wird mit einer Volltonfarbe gefüllt.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Ein Pfad kann aus mehreren Abbildungen (Unterpfaden) bestehen. Die [**Graphics::FillPath-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) füllt das Innere der einzelnen Abbildungen aus. Wenn eine Figur nicht geschlossen ist, füllt die **Graphics::FillPath-Methode** den Bereich aus, der eingeschlossen würde, wenn die Figur geschlossen wäre. Im folgenden Beispiel wird ein Pfad zeichnet und ausgefüllt, der aus einem Bogen, einem Kardinalspfeil, einer Zeichenfolge und einem Kreis besteht.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



Die folgende Abbildung zeigt den Pfad vor und nach dem Auffüllen mit einem Vollbildpinsel. Beachten Sie, dass der Text in der Zeichenfolge von der [**Graphics::D rawPath-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) umrissen, aber nicht ausgefüllt wird. Es ist die [**Graphics::FillPath-Methode,**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) die das Innere der Zeichen in der Zeichenfolge zeichnet.

![Abbildung, die zweimal Text und eine geöffnete und eine geschlossene Kurve zeigt; diese sind beim ersten Mal leer und werden zum zweiten Mal ausgefüllt.](images/aboutgdip02-art26.png)

 

 



