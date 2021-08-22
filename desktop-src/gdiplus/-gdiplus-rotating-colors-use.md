---
description: Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Rotieren von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09a84c4c51181c672c549369783ac476fa1d3c79f1598c1c29ca14604429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036428"
---
# <a name="rotating-colors"></a>Rotieren von Farben

Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren. Wir können die Visualisierung der Drehung vereinfachen, indem wir uns darauf einigen, eine der Farbkomponenten zu fixieren. Angenommen, wir stimmen zu, dass die Alphakomponente auf 1 (vollständig deckend) festgelegt ist. Anschließend können wir einen dreidimensionalen Farbraum mit roten, grünen und blauen Achsen visualisieren, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Perspektivenansicht eines dreidimensionalen Farbraums mit Achsen mit den Bezeichnungen Rot, Grün und Blau](images/recoloring03.png)

Eine Farbe kann als Punkt im 3D-Raum dargestellt werden. Beispielsweise stellt der Punkt (1, 0, 0) im Raum die Farbe Rot und der Punkt (0, 1, 0) im Raum die Farbe Grün dar.

Die folgende Abbildung zeigt, was es bedeutet, die Farbe (1, 0, 0) um einen Winkel von 60 Grad in der Red-Green drehen. Die Drehung in einer Ebene parallel zur Red-Green ist als Drehung um die blaue Achse zu sehen.

![Abbildung des Punkts (1, 0, 0), der um 60 Grad nach (0,5, 0,866, 0) gedreht wurde](images/recoloring04.png)

Die folgende Abbildung zeigt, wie eine Farbmatrix initialisiert wird, um Drehungen über jede der drei Koordinatenachsen (rot, grün, blau) durchzuführen.

![Abbildung mit Farbmatrizen, die Drehungen um jede der drei Koordinatenachsen ausführen](images/recoloring05.png)

Im folgenden Beispiel wird ein Bild mit einer Farbe (1, 0, 0,6) verwendet und eine Drehung um 60 Grad um die blaue Achse angewendet. Der Winkel der Drehung wird in einer Ebene herausgefegt, die parallel zur Red-Green ist.


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



Die folgende Abbildung zeigt das originale Bild links und das farblich gedrehte Bild auf der rechten Seite.

![Abbildung: Rechtecke, die mit dem originalen Bild gefüllt sind (violettes Rot) und farbrotes Bild (Seegrün)](images/colortrans5.png)

Die im vorherigen Codebeispiel ausgeführte Farbrotation kann wie folgt visualisiert werden.

![Abbildung eines 3d-Farbraums, und der Punkt (1, 0, 0,6) hat sich um 60 Grad bis (0,5, 0,866, 0,6) gedreht.](images/recoloring06.png)

 

 



