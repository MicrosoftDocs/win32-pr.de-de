---
description: 'Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Geöffnete und geschlossene Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571421"
---
# <a name="open-and-closed-curves"></a>Geöffnete und geschlossene Kurven

Die folgende Abbildung zeigt zwei Kurven: eine geöffnete und eine geschlossene.

![Abbildung einer geöffneten Kurve (eine gekrümmte Linie) und einer geschlossenen Kurve (der Umriss einer Form)](images/aboutgdip02-art24.png)

Geschlossene Kurven verfügen über ein inneres und können daher mit einem Pinsel gefüllt werden. Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse in Windows GDI+ bietet die folgenden Methoden zum Auffüllen geschlossener Abbildungen und Kurven: [fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)und [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion). Jedes Mal, wenn Sie eine dieser Methoden aufrufen, müssen Sie die Adresse eines der spezifischen Pinseltypen ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)oder [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) als Argument übergeben.

Die [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) -Methode ist ein begleitende der [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) -Methode. Ebenso wie die DrawArc-Methode einen Teil der Gliederung einer Ellipse zeichnet, füllt die FillPie-Methode einen Teil des Inneren einer Ellipse aus. Im folgenden Beispiel wird ein Bogen gezeichnet und der entsprechende Teil des Inneren der Ellipse ausgefüllt.


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



Die folgende Abbildung zeigt den Bogen und den gefüllten Kreis.

![Abbildung, die ein Segment einer ausgefüllten Ellipse anzeigt](images/aboutgdip02-art25.png)

Die [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) -Methode ist ein begleitende der [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) -Methode. Beide Methoden schließen die Kurve automatisch, indem Sie den Endpunkt mit dem Ausgangspunkt verbinden. Im folgenden Beispiel wird eine Kurve gezeichnet, die durchläuft (0,0), (60, 20) und (40, 50). Anschließend wird die Kurve automatisch geschlossen, indem (40, 50) mit dem Anfangspunkt (0,0) verbunden wird, und das innere wird mit einer voll Tonfarbe gefüllt.


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



Ein Pfad kann aus mehreren Abbildungen (unter Pfaden) bestehen. Die [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode füllt das innere jeder Abbildung aus. Wenn eine Abbildung nicht geschlossen wird, füllt die **Graphics:: FillPath** -Methode den Bereich, der eingeschlossen werden würde, wenn die Abbildung geschlossen würde. Im folgenden Beispiel wird ein Pfad gezeichnet und gefüllt, der aus einem Bogen, einem kardinalspline, einer Zeichenfolge und einem Kreis besteht.


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



In der folgenden Abbildung wird der Pfad vor und nach dem Auffüllen mit einem Pinsel dargestellt. Beachten Sie, dass der Text in der Zeichenfolge von der [**Grafik::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode beschrieben, aber nicht ausgefüllt ist. Dabei handelt es sich um die [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode, die das Innere der Zeichen in der Zeichenfolge zeichnet.

![die Abbildung zeigt, dass zweimal Text und eine offene und eine geschlossene Kurve angezeigt werden. Diese sind beim ersten Mal leer und wurden beim zweiten Mal ausgefüllt.](images/aboutgdip02-art26.png)

 

 



