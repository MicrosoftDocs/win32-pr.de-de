---
description: Durch das Scheren wird eine Farbkomponente um einen in einer anderen Farbkomponente proportionalen Betrag vergrößert oder verringert.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Scheren von Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131332"
---
# <a name="shearing-colors"></a>Scheren von Farben

Durch das Scheren wird eine Farbkomponente um einen in einer anderen Farbkomponente proportionalen Betrag vergrößert oder verringert. Nehmen Sie z. b. die Transformation, bei der die rote Komponente um einen halben Wert der blauen Komponente erweitert wird. Bei einer solchen Transformation würde die Farbe (0,2, 0,5, 1) zu (0,7, 0,5, 1) werden. Die neue rote Komponente ist 0,2 + (1/2) (1) = 0,7.

Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei ColorBars4.bmp erstellt. Anschließend wendet der Code die im vorherigen Absatz beschriebene Scheren Transformation auf jedes Pixel im Bild an.


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
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



Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das auf der rechten Seite gelauftene Bild.

![die Abbildung zeigt vierfarbige Balken, dann die gleichen Balken mit unterschiedlichen Farben.](images/colortrans6.png)

Die folgende Tabelle zeigt die Farb Vektoren für die vier Balken vor und nach der Transformation für das Scheren-Diagramm.



| Ursprünglich           | Zert            |
|--------------------|--------------------|
| (0, 0, 1, 1)       | (0.5, 0, 1, 1)     |
| (0.5, 1, 0.5, 1)   | (0.75, 1, 0.5, 1)  |
| (1, 1, 0, 1)       | (1, 1, 0, 1)       |
| (0.4, 0.4, 0.4, 1) | (0.6, 0.4, 0.4, 1) |



 

 

 



