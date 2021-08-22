---
description: Eine Skalierungstransformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl. Die Farbmatrixeinträge, die die Skalierung darstellen, sind in der folgenden Tabelle angegeben.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Skalieren von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7877db07ff1a11dcb985f8b0ca8ec3cc017f25fe45f00e989c9108891f8ff1ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036368"
---
# <a name="scaling-colors"></a>Skalieren von Farben

Eine Skalierungstransformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl. Die Farbmatrixeinträge, die die Skalierung darstellen, sind in der folgenden Tabelle angegeben.



| Zu skalierende Komponente | Matrixeintrag |
|------------------------|--------------|
| Red                    | \[0 \] \[ 0\]   |
| Grün                  | \[1 \] \[ 1\]   |
| Blau                   | \[2 \] \[ 2\]   |
| Alpha                  | \[3 \] \[ 3\]   |



 

Im folgenden Beispiel wird ein [**Image-Objekt aus**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) der Datei ColorBars2.bmp. Anschließend skaliert der Code die blaue Komponente jedes Pixels im Bild um den Faktor 2. Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



Die folgende Abbildung zeigt das ursprüngliche Bild links und das skalierte Bild auf der rechten Seite.

![Zeigt vier farbige Balken und dann die gleichen Balken mit unterschiedlichen Farben an.](images/colortrans3.png)

Die folgende Tabelle zeigt die Farbvektoren für die vier Balken vor und nach der blauen Skalierung. Beachten Sie, dass die blaue Komponente in der vierten Farbleiste von 0,8 auf 0,6 verstrichen ist. Das liegt daran GDI+ nur den Bruchteil des Ergebnisses beibebehalte. Beispiel: (2)(0,8) = 1,6, und der Bruchteil von 1,6 ist 0,6. Wenn nur der Bruchteil beibehalten wird, wird sichergestellt, dass das Ergebnis immer im \[ Intervall 0, 1 \] liegt.



| Ursprünglich           | Skaliert             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

Im folgenden Beispiel wird ein [**Image-Objekt aus**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) der Datei ColorBars2.bmp. Anschließend skaliert der Code die roten, grünen und blauen Komponenten der einzelnen Pixel im Bild. Die roten Komponenten werden um 25 Prozent herunterskaliert, die grünen Komponenten werden um 35 Prozent herunterskaliert, und die blauen Komponenten werden um 50 Prozent herunterskaliert.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



Die folgende Abbildung zeigt das ursprüngliche Bild links und das skalierte Bild auf der rechten Seite.

![Abbildung mit vier farbigen Balken und balken mit unterschiedlichen Farben](images/colortrans4.png)

Die folgende Tabelle zeigt die Farbvektoren für die vier Balken vor und nach der roten, grünen und blauen Skalierung.



| Ursprünglich           | Skaliert               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



