---
description: GDI+ bietet horizontale, vertikale und diagonale lineare Farbverläufe. Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig. Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe nicht einheitlich ändert.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Erstellen eines linearen Farbverlaufs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922c4f1fc805aae25f53ed206d1b3e9112afbd3fa51ba544e121a70839d79d0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015196"
---
# <a name="creating-a-linear-gradient"></a>Erstellen eines linearen Farbverlaufs

GDI+ bietet horizontale, vertikale und diagonale lineare Farbverläufe. Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig. Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe nicht einheitlich ändert.

-   [Horizontale lineare Farbverläufe](#horizontal-linear-gradients)
-   [Anpassen linearer Farbverläufe](#customizing-linear-gradients)
-   [Diagonale lineare Farbverläufe](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a>Horizontale lineare Farbverläufe

Im folgenden Beispiel wird ein horizontaler linearer Farbverlaufspinsel verwendet, um eine Linie, eine Ellipse und ein Rechteck auszufüllen:


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



Der [**LinearGradientBrush-Konstruktor**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) empfängt vier Argumente: zwei Punkte und zwei Farben. Der erste Punkt (0, 10) ist der ersten Farbe (rot) zugeordnet, und der zweite Punkt (200, 10) ist der zweiten Farbe (blau) zugeordnet. Wie Sie erwarten würden, ändert sich die Linie, die von (0, 10) bis (200, 10) gezeichnet wird, allmählich von Rot in Blau.

Die 10er-Punkte in den Punkten (50, 10) und (200, 10) sind nicht wichtig. Wichtig ist, dass die beiden Punkte dieselbe zweite Koordinate aufweisen– die Linie, die sie verbindet, ist horizontal. Die Ellipse und das Rechteck ändern sich ebenfalls schrittweise von Rot in Blau, wenn die horizontale Koordinate von 0 bis 200 reicht.

Die folgende Abbildung zeigt die Linie, die Ellipse und das Rechteck. Beachten Sie, dass sich der Farbverlauf wiederholt, wenn die horizontale Koordinate über 200 hinausgeht.

![Abbildung eines horizontalen Farbverlaufs, der eine Linie und eine Ellipse füllt, sowie ein Rechteck, das länger als die Ellipse ist](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>Anpassen linearer Farbverläufe

Im vorherigen Beispiel ändern sich die Farbkomponenten linear, wenn Sie von einer horizontalen Koordinate von 0 zu einer horizontalen Koordinate von 200 wechseln. Beispielsweise hat ein Punkt, dessen erste Koordinate halbwegs zwischen 0 und 200 liegt, eine blaue Komponente, die zwischen 0 und 255 liegt.

GDI+ können Sie anpassen, wie eine Farbe von einem Rand eines Farbverlaufs zum anderen variiert. Angenommen, Sie möchten einen Farbverlaufspinsel erstellen, der sich gemäß der folgenden Tabelle von Schwarz in Rot ändert.



| Horizontale Koordinate | RGB-Komponenten |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

Beachten Sie, dass die rote Komponente eine halbe Intensität aufwies, wenn die horizontale Koordinate nur 20 Prozent des Wegs von 0 bis 200 beträgt.

Das folgende Beispiel ruft die [**LinearGradientBrush::SetBlend-Methode**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) eines [**LinearGradientBrush-Objekts**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) auf, um drei relative Intensitäten mit drei relativen Positionen zuzuordnen. Wie in der obigen Tabelle wird eine relative Intensität von 0,5 einer relativen Position von 0,2 zugeordnet. Der Code füllt eine Ellipse und ein Rechteck mit dem Farbverlaufspinsel aus.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



Die folgende Abbildung zeigt die resultierende Ellipse und das Rechteck.

![Abbildung eines horizontalen Farbverlaufs, der eine Ellipse und ein Rechteck füllt, das länger als die Ellipse ist](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>Diagonale lineare Farbverläufe

Die Farbverläufe in den vorherigen Beispielen waren horizontal. Das heißt, die Farbe ändert sich nach und nach, wenn Sie sich entlang einer horizontalen Linie bewegen. Sie können auch vertikale Farbverläufe und diagonale Farbverläufe definieren. Der folgende Code übergibt die Punkte (0, 0) und (200, 100) an einen [**LinearGradientBrush-Konstruktor.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) Die Farbe Blau ist (0, 0) zugeordnet, und die Farbe Grün ist (200, 100) zugeordnet. Eine Linie (mit Stiftbreite 10) und eine Ellipse werden mit dem linearen Farbverlaufspinsel gefüllt.


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



Die folgende Abbildung zeigt die Linie und die Ellipse. Beachten Sie, dass sich die Farbe in der Ellipse schrittweise ändert, wenn Sie sich entlang einer Zeile bewegen, die parallel zur Linie verläuft, die durch (0, 0) und (200, 100) verläuft.

![Abbildung eines diagonalen Farbverlaufs, der eine Ellipse und eine diagonale Linie füllt](images/lineargradient3.png)

 

 



