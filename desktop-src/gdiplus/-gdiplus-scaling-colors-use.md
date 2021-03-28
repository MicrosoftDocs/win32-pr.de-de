---
description: Eine Skalierungs Transformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl. Die Farbmatrix Einträge, die die Skalierung darstellen, werden in der folgenden Tabelle angegeben.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Skalieren von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218912"
---
# <a name="scaling-colors"></a>Skalieren von Farben

Eine Skalierungs Transformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl. Die Farbmatrix Einträge, die die Skalierung darstellen, werden in der folgenden Tabelle angegeben.



| Zu skalierbare Komponente | Matrix Eintrag |
|------------------------|--------------|
| Red                    | \[0 \] \[ 0\]   |
| Grün                  | \[1 \] \[ 1\]   |
| Blau                   | \[2 \] \[ 2\]   |
| Alpha                  | \[3 \] \[ 3\]   |



 

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars2.bmp erstellt. Anschließend skaliert der Code die blaue Komponente jedes Pixels im Bild um den Faktor 2. Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.


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



Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite.

![Zeigt vierfarbige Balken und dann die gleichen Balken mit unterschiedlichen Farben an.](images/colortrans3.png)

In der folgenden Tabelle werden die Farb Vektoren für die vier Balken vor und nach der blauen Skalierung angezeigt. Beachten Sie, dass die blaue Komponente in der vierten Farbleiste von 0,8 zu 0,6 gewechselt ist. Dies liegt daran, dass GDI+ nur den Bruch Teil des Ergebnisses beibehält. Beispiel: (2) (0,8) = 1,6 und der Bruchteil von 1,6 ist 0,6. Wenn nur der Bruchteil beibehalten wird, wird sichergestellt, dass das Ergebnis immer im Intervall \[ 0, 1 liegt \] .



| Ursprünglich           | Läufig             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars2.bmp erstellt. Anschließend werden im Code die roten, grünen und blauen Komponenten der einzelnen Pixel im Bild skaliert. Die roten Komponenten werden auf 25% herunterskaliert, die grünen Komponenten werden um 35% herunterskaliert, und die blauen Komponenten werden um 50% herunterskaliert.


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



Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite.

![Abbildung, die vierfarbige Balken anzeigt, dann diese Balken mit unterschiedlichen Farben](images/colortrans4.png)

In der folgenden Tabelle werden die Farb Vektoren für die vier Balken vor und nach der roten, grünen und blauen Skalierung angezeigt.



| Ursprünglich           | Läufig               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



