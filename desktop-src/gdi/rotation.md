---
description: Viele CAD-Anwendungen stellen Features zur Verfügung, die im Clientbereich gezeichnete Objekte drehen.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Drehung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa6552411e2e018d04ff55cbeeb430d185fe62d61dc59d421d08dbe6e0d7174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602700"
---
# <a name="rotation"></a>Drehung

Viele CAD-Anwendungen stellen Features zur Verfügung, die im Clientbereich gezeichnete Objekte drehen. Anwendungen, die Drehungsfunktionen enthalten, verwenden die [**SetWorldTransform-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) um die entsprechende Transformation für Den Raum auf Seitenbereich zu setzen. Diese Funktion empfängt einen Zeiger auf eine [**XFORM-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-xform) die die entsprechenden Werte enthält. Die Member eM11, eM12, eM21 und eM22 von XFORM geben jeweils den Kosinus, Sinus, negativen Sinus und Kosinus des Drehwinkels an.

Wenn *eine* Drehung auftritt, werden die Punkte, die ein Objekt bilden, in Bezug auf den Ursprung des Koordinatenraums gedreht. Die folgende Abbildung zeigt ein 20-by-20-Einheiten-Rechteck, das um 30 Grad gedreht wird, wenn es aus dem Weltkoordinatenraum in den Seitenkoordinatenraum kopiert wird.

![Abbildung, die zwei Koordinatenräume zeigt; Jede hat eine Rectange an einer anderen Position und mit einer anderen Drehung.](images/cstrn-11.png)

In der obigen Abbildung wurde jeder Punkt im Rechteck um 30 Grad im Hinblick auf den Ursprung des Koordinatenraums gedreht.

Der folgende Algorithmus berechnet die neue x-Koordinate (x ') für einen Punkt (x,y ), der im Hinblick auf den Ursprung des Koordinatenraums um Winkel A gedreht wird.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

Der folgende Algorithmus berechnet die y-Koordinate (y ') für einen Punkt (x,y ), der vom Winkel A in Bezug auf den Ursprung gedreht wird.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

Die beiden Rotationstransformationen können wie folgt in einer 2:2-Matrix kombiniert werden.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

Die 2 by 2-Matrix, die die Drehung erzeugt hat, enthält die folgenden Werte.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Rotationsalgorithmusableitung

Rotationsalgorithmen basieren auf dem Additionssatz der Trigonometrie, der besagt, dass die trigonometrische Funktion einer Summe von zwei Winkeln (A1 und A2 ) in Bezug auf die trigonometrischen Funktionen der beiden Winkel ausgedrückt werden kann.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

Die folgende Abbildung zeigt einen Punkt, der gegen den Uhrzeigersinn zu einer neuen Position p' gedreht wurde. Darüber hinaus werden zwei Dreiecke angezeigt, die aus einer Linie gebildet werden, die vom Ursprung des Koordinatenraums bis zu jedem Punkt gezeichnet wird, und einer Linie, die von jedem Punkt durch die X-Achse gezeichnet wird.

![Diagramm, das den Ursprung, p und p' und zwei Dreiecke zeigt](images/cstrn-12.png)

Mithilfe der Trigonometrie kann die x-Koordinate des Punkts p durch Multiplizieren der Länge der Hypotenuse h mit dem Kosinus von A1 ermittelt werden.

``` syntax
x = h * cos A1 
```

Die y-Koordinate des Punkts p kann durch Multiplizieren der Länge der Hypotenuse h mit dem Sinus von A1 ermittelt werden.

``` syntax
y = h * sin A1 
```

Ebenso kann die x-Koordinate des Punkts p' durch Multiplizieren der Länge der Hypotenuse h mit dem Kosinus von (A1 +A2 ) ermittelt werden.

``` syntax
x' = h * cos (A1 + A2) 
```

Schließlich kann die y-Koordinate des Punkts p' durch Multiplizieren der Länge der Hypotenuse h mit dem Sinus von (A1 +A2 ) ermittelt werden.

``` syntax
y' = h * sin (A1 + A2) 
```

Mit dem Additionssatz werden die obigen Algorithmen wie folgt:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Die Drehalgorithmen für einen bestimmten Punkt, der um Winkel A2 gedreht wird, können durch Dies erreichen, indem Sie x für jedes Vorkommen von (h cos A1 ) und durch y für jedes Vorkommen von \* (h \* sin A1) substituieren.

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



