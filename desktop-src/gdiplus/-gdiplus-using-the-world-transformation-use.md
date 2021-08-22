---
description: Die Welttransformation ist eine Eigenschaft der Graphics-Klasse.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Verwenden der globalen Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6288b5640e330a827e96b632541dac44e9463b87c566c16a94797810c4c92c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977240"
---
# <a name="using-the-world-transformation"></a>Verwenden der globalen Transformation

Die Welttransformation ist eine Eigenschaft der [**Graphics-Klasse.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Die Zahlen, die die Welttransformation angeben, werden in einem [**Matrix-Objekt**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) gespeichert, das eine 3-×3-Matrix darstellt. Die **Klassen Matrix** und **Graphics** verfügen über mehrere Methoden zum Festlegen der Zahlen in der Welttransformationsmatrix. In den Beispielen in diesem Abschnitt werden Rechtecke bearbeitet, da Rechtecke einfach zu zeichnen sind und die Auswirkungen von Transformationen auf Rechtecke leicht zu erkennen sind.

Wir beginnen mit dem Erstellen eines Rechtecks von 50 durch 50 und dem Suchen am Ursprung (0, 0). Der Ursprung befindet sich in der oberen linken Ecke des Clientbereichs.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



Der folgende Code wendet eine Skalierungstransformation an, die das Rechteck um den Faktor 1,75 in x-Richtung erweitert und das Rechteck um den Faktor 0,5 in y-Richtung verkleinert:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



Das Ergebnis ist ein Rechteck, das länger in x-Richtung und kürzer in y-Richtung als das Original ist.

Verwenden Sie anstelle des vorangehenden Codes den folgenden Code, um das Rechteck zu drehen, anstatt es zu skalieren:


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



 

 



