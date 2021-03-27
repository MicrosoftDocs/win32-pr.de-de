---
description: Die Welt Transformation ist eine Eigenschaft der Grafikklasse.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Verwenden der globalen Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214566"
---
# <a name="using-the-world-transformation"></a>Verwenden der globalen Transformation

Die Welt Transformation ist eine Eigenschaft der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse. Die Zahlen, die die globale Transformation angeben, werden in einem [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt gespeichert, das eine 3 × 3-Matrix darstellt. Die **Matrix** -und **Grafik** Klassen verfügen über mehrere Methoden zum Festlegen der Zahlen in der Transformations Matrix der Welt. Die Beispiele in diesem Abschnitt manipulieren Rechtecke, da Rechtecke leicht gezeichnet werden können, und es ist leicht, die Auswirkungen von Transformationen auf Rechtecke anzuzeigen.

Wir beginnen mit dem Erstellen eines 50 nach 50-Rechtecks und der Suche am Ursprung (0,0). Der Ursprung befindet sich in der oberen linken Ecke des Client Bereichs.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



Der folgende Code wendet eine Skalierungs Transformation an, die das Rechteck um den Faktor 1,75 in der x-Richtung erweitert und das Rechteck um den Faktor 0,5 in der y-Richtung verkleinert:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



Das Ergebnis ist ein Rechteck, das in der x-Richtung länger und kürzer in der y-Richtung als die ursprüngliche ist.

Um das Rechteck zu drehen, anstatt es zu skalieren, verwenden Sie den folgenden Code anstelle des vorangehenden Codes:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



Verwenden Sie den folgenden Code, um das Rechteck zu übersetzen:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



