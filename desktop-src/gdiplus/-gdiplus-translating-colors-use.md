---
description: Eine Übersetzung Fügt einer oder mehreren der vier Farbkomponenten einen Wert hinzu. Die Farbmatrix Einträge, die Übersetzungen darstellen, werden in der folgenden Tabelle angegeben.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Übersetzen von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567896"
---
# <a name="translating-colors"></a>Übersetzen von Farben

Eine Übersetzung Fügt einer oder mehreren der vier Farbkomponenten einen Wert hinzu. Die Farbmatrix Einträge, die Übersetzungen darstellen, werden in der folgenden Tabelle angegeben.



| Zu über setzende Komponente | Matrix Eintrag |
|----------------------------|--------------|
| Red                        | \[4 \] \[ 0\]   |
| Grün                      | \[4 \] \[ 1\]   |
| Blau                       | \[4 \] \[ 2\]   |
| Alpha                      | \[4 \] \[ 3\]   |



 

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars.bmp erstellt. Anschließend fügt der Code der roten Komponente jedes Pixels im Bild 0,75 hinzu. Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.


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



Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite.

![die Abbildung zeigt vierfarbige Balken, dann die gleichen Balken mit unterschiedlichen Farben.](images/colortrans2.png)

In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der roten Übersetzung aufgelistet. Beachten Sie, dass die rote Komponente in der zweiten Zeile nicht geändert wird, da der Höchstwert für eine Farbkomponente 1 ist. (Auf ähnliche Weise ist der minimale Wert für eine Farbkomponente 0.)



| Ursprünglich           | Übersetzt      |
|--------------------|-----------------|
| Schwarz (0,0 (0, 0, 1) | (0.75, 0, 0, 1) |
| Rot (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Grün (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Blau (0,0 (0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



