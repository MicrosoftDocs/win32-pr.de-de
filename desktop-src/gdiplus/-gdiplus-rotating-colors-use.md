---
description: Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Drehen von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862528"
---
# <a name="rotating-colors"></a>Drehen von Farben

Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren. Wir können das Visualisieren der Rotation vereinfachen, indem wir akzeptieren, dass eine der Farbkomponenten korrigiert wird. Angenommen, die Alpha Komponente muss bei 1 (vollständig nicht transparent) korrigiert bleiben. Anschließend können wir einen dreidimensionalen Farbraum mit roten, grünen und blauen Achsen visualisieren, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Perspektiven Ansicht eines dreidimensionalen Farbraum mit Achsen mit der Bezeichnung rot, grün und blau](images/recoloring03.png)

Eine Farbe kann sich als Punkt im 3D-Raum vorstellen. Der Punkt (1, 0, 0) im Raum stellt z. b. die Farbe rot dar, und der Punkt (0, 1, 0) im Raum stellt die Farbe grün dar.

In der folgenden Abbildung wird gezeigt, was es bedeutet, die Farbe (1, 0, 0) durch einen Winkel von 60 Grad in der Red-Green Ebene zu drehen. Die Drehung in einer Ebene parallel zur Red-Green Ebene kann als Drehung der blauen Achse betrachtet werden.

![Abbildung, die anzeigt, dass der Punkt (1, 0, 0) um 60 Grad gedreht wird (0,5, 0,866, 0)](images/recoloring04.png)

In der folgenden Abbildung wird gezeigt, wie eine Farbmatrix initialisiert wird, um Drehungen zu jeder der drei Koordinatenachsen (rot, grün, blau) auszuführen.

![Abbildung der Farb Matrizen, die Drehungen zu jeder der drei Koordinatenachsen ausführen](images/recoloring05.png)

Im folgenden Beispiel wird ein Bild, das alle eine Farbe (1, 0, 0,6) ist, und eine 60-Grad-Drehung der blauen Achse angewendet. Der Winkel der Drehung wird in einer Ebene durchlaufen, die parallel zum Red-Green Ebene ist.


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



Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das Farb gedrehte Bild auf der rechten Seite.

![Abbildung mit Rechtecke, die mit dem ursprünglichen Bild (violett rot) und einem Farb rotierten Bild (Meer grün) gefüllt sind](images/colortrans5.png)

Die im vorangehenden Codebeispiel ausgeführte Farb Drehung kann wie folgt visualisiert werden.

![die Abbildung zeigt einen 3D-Farbraum, und der Punkt (1, 0, 0,6) gedreht 60 Grad nach (0,5, 0,866, 0,6).](images/recoloring06.png)

 

 



