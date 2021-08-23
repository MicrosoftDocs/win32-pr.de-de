---
description: Eine Übersetzung fügt einer oder mehrere der vier Farbkomponenten einen Wert hinzu. Die Farbmatrixeinträge, die Übersetzungen darstellen, sind in der folgenden Tabelle angegeben.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Übersetzen von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608a0653423d854e6d77bd624949f24ec03cce6c4ed063d4c740dd142b1dfb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036338"
---
# <a name="translating-colors"></a>Übersetzen von Farben

Eine Übersetzung fügt einer oder mehrere der vier Farbkomponenten einen Wert hinzu. Die Farbmatrixeinträge, die Übersetzungen darstellen, sind in der folgenden Tabelle angegeben.



| Zu übersetzende Komponente | Matrixeintrag |
|----------------------------|--------------|
| Red                        | \[4 \] \[ 0\]   |
| Grün                      | \[4 \] \[ 1\]   |
| Blau                       | \[4 \] \[ 2\]   |
| Alpha                      | \[4 \] \[ 3\]   |



 

Im folgenden Beispiel wird ein [**Image-Objekt aus**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) der Datei ColorBars.bmp. Anschließend fügt der Code der roten Komponente jedes Pixels im Bild 0,75 hinzu. Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



Die folgende Abbildung zeigt das ursprüngliche Bild links und das transformierte Bild auf der rechten Seite.

![Abbildung mit vier farbigen Balken und denselben Balken mit unterschiedlichen Farben](images/colortrans2.png)

In der folgenden Tabelle sind die Farbvektoren für die vier Balken vor und nach der roten Übersetzung aufgeführt. Beachten Sie, dass sich die rote Komponente in der zweiten Zeile nicht ändert, da der Höchstwert für eine Farbkomponente 1 ist. (Entsprechend ist der Mindestwert für eine Farbkomponente 0.)



| Ursprünglich           | Übersetzt      |
|--------------------|-----------------|
| Schwarz (0, 0, 0, 1) | (0.75, 0, 0, 1) |
| Rot (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Grün (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Blau (0, 0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



