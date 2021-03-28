---
description: Sie können ein Bild drehen, reflektieren und verzerren, indem Sie Zielpunkte für die obere linke, obere Rechte und untere linke Ecke des ursprünglichen Bilds angeben.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Rotation, Spiegelung und Neigung von Bildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959446"
---
# <a name="rotating-reflecting-and-skewing-images"></a>Rotation, Spiegelung und Neigung von Bildern

Sie können ein Bild drehen, reflektieren und verzerren, indem Sie Zielpunkte für die obere linke, obere Rechte und untere linke Ecke des ursprünglichen Bilds angeben. Die drei Zielpunkte bestimmen eine affine Transformation, die das ursprüngliche rechteckige Bild einem Parallelogram zuordnet. (Die untere rechte Ecke des ursprünglichen Bilds wird der vierten Ecke des parallelograms zugeordnet, das aus den drei angegebenen Zielpunkten berechnet wird.)

Angenommen, das ursprüngliche Bild ist ein Rechteck mit der oberen linken Ecke bei (0,0), der oberen rechten Ecke bei (100, 0) und der unteren linken Ecke bei (0, 50). Nehmen wir nun an, dass die drei Punkte den Zielpunkten folgendermaßen zugeordnet werden.



| Ursprünglicher Punkt       | Zielpunkt |
|----------------------|-------------------|
| Oben links (0,0)    | (200, 20)         |
| Upper-Right (100, 0) | (110, 100)        |
| Unten links (0, 50)   | (250, 30)         |



 

Die folgende Abbildung zeigt das ursprüngliche Bild und das dem Parallelogram zugeordnete Bild. Das ursprüngliche Bild wurde verzerrt, reflektiert, gedreht und übersetzt. Die x-Achse entlang des oberen Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (110, 100). Die y-Achse entlang des linken Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (250, 30).

![die Abbildung zeigt farbige Streifen am Ursprung der Koordinatenachsen und die gleichen Streifen an einer anderen Position, Drehung und Größe.](images/stripes1.png)

Im folgenden Beispiel werden die in der obigen Abbildung gezeigten Bilder erzeugt.


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



Die folgende Abbildung zeigt eine ähnliche Transformation, die auf ein Foto Bild angewendet wird.

![Darstellung des gleichen Fotos zweimal die zweite ist umgekehrt, verzerrt und hat unterschiedliche Größe, Drehung und Position.](images/transformedclimber.png)

Die folgende Abbildung zeigt eine ähnliche Transformation, die auf eine Metadatei angewendet wird.

![Darstellung von Formen und Text, dann erneut, aber umgekehrt, verzerrt und mit unterschiedlichen Standorten, Drehung und Größe](images/transformedmetafile.png)

 

 



