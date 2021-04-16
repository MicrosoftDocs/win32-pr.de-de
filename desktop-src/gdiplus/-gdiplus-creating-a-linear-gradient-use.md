---
description: GDI+ stellt horizontale, vertikale und diagonale lineare Farbverläufe bereit. Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig. Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe auf nicht einheitliche Weise ändert.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Erstellen eines linearen Farbverlaufs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566146"
---
# <a name="creating-a-linear-gradient"></a>Erstellen eines linearen Farbverlaufs

GDI+ stellt horizontale, vertikale und diagonale lineare Farbverläufe bereit. Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig. Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe auf nicht einheitliche Weise ändert.

-   [Horizontale lineare Farbverläufe](#horizontal-linear-gradients)
-   [Anpassen von linearen Farbverläufen](#customizing-linear-gradients)
-   [Diagonale lineare Farbverläufe](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a>Horizontale lineare Farbverläufe

Im folgenden Beispiel wird ein horizontaler linearer Farbverlaufs Pinsel verwendet, um eine Linie, eine Ellipse und ein Rechteck auszufüllen:


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



Der [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) -Konstruktor erhält vier Argumente: zwei Punkte und zwei Farben. Der erste Punkt (0, 10) ist mit der ersten Farbe (rot) verknüpft, und der zweite Punkt (200, 10) wird der zweiten Farbe (blau) zugeordnet. Erwartungsgemäß wird die von (0, 10) zu (200, 10) gezogene Linie allmählich von rot in blau geändert.

Die 10S in den Punkten (50, 10) und (200, 10) sind nicht wichtig. Wichtig ist, dass die beiden Punkte dieselbe zweite Koordinate aufweisen – die Linie, die Sie verbindet, ist horizontal. Die Ellipse und das Rechteck ändern sich auch allmählich von rot in blau, wenn die horizontale Koordinate von 0 bis 200 wechselt.

Die folgende Abbildung zeigt die Zeile, die Ellipse und das Rechteck. Beachten Sie, dass der Farbverlauf selbst wiederholt wird, wenn sich die horizontale Koordinate über 200 erhöht.

![die Abbildung zeigt einen horizontalen Farbverlauf, der eine Linie und eine Ellipse füllt, und ein Rechteck, das länger als die Ellipse ist.](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>Anpassen von linearen Farbverläufen

Im vorherigen Beispiel ändern sich die Farbkomponenten linear, wenn Sie von einer horizontalen Koordinate von 0 zu einer horizontalen Koordinate von 200 wechseln. Beispielsweise weist ein Punkt, dessen erste Koordinate die Hälfte zwischen 0 und 200 ist, eine blaue Komponente auf, die sich in der Mitte zwischen 0 und 255 befindet.

Mit GDI+ können Sie die Art und Weise anpassen, in der eine Farbe von einem Rand eines Farbverlaufs zum anderen abweicht. Angenommen, Sie möchten einen Farbverlaufs Pinsel erstellen, der gemäß der folgenden Tabelle von schwarz in rot geändert wird.



| Horizontale Koordinate | RGB-Komponenten |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

Beachten Sie, dass die rote Komponente die halbe Intensität hat, wenn die horizontale Koordinate nur 20 Prozent der Art von 0 bis 200 ist.

Im folgenden Beispiel wird die [**LinearGradientBrush:: setblend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) -Methode eines [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) -Objekts aufgerufen, um drei relative Intensitäten mit drei relativen Positionen zuzuordnen. Wie in der obigen Tabelle ist eine relative Intensität von 0,5 mit einer relativen Position von 0,2 verknüpft. Der Code füllt eine Ellipse und ein Rechteck mit dem Farbverlaufs Pinsel.


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



In der folgenden Abbildung werden die resultierende Ellipse und das Rechteck gezeigt.

![die Abbildung zeigt einen horizontalen Farbverlauf, der eine Ellipse und ein Rechteck füllt, das länger als die Ellipse ist.](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>Diagonale lineare Farbverläufe

Die Farbverläufe in den vorangehenden Beispielen waren horizontal. Das heißt, die Farbe ändert sich allmählich, wenn Sie sich entlang einer horizontalen Linie bewegen. Sie können auch vertikale Farbverläufe und diagonale Farbverläufe definieren. Der folgende Code übergibt die Punkte (0,0) und (200, 100) an einen [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) -Konstruktor. Die Farbe blau ist (0,0) zugeordnet, und die Farbe grün ist zugeordnet (200, 100). Eine Linie (mit der Stift Breite 10) und eine Ellipse werden mit dem linearen Farbverlaufs Pinsel gefüllt.


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



Die folgende Abbildung zeigt die Zeile und die Ellipse. Beachten Sie, dass sich die Farbe in der Ellipse allmählich ändert, wenn Sie eine beliebige Zeile bewegen, die parallel zur Zeile, die durchläuft (0,0) und (200, 100).

![Abbildung mit einem diagonalen Farbverlauf, der eine Ellipse und eine diagonal Linie füllt](images/lineargradient3.png)

 

 



