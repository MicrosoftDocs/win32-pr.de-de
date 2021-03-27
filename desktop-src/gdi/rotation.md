---
description: Viele CAD-Anwendungen stellen Funktionen bereit, die Objekte drehen, die im Client Bereich gezeichnet werden.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Drehung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980680"
---
# <a name="rotation"></a>Drehung

Viele CAD-Anwendungen stellen Funktionen bereit, die Objekte drehen, die im Client Bereich gezeichnet werden. Anwendungen, die rotationsfunktionen enthalten, verwenden die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion, um die entsprechende Welt Raum-und Seiten Raum Transformation festzulegen. Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält. Die eM11-, eM12-, eM21-und eM22-Member von XForm geben jeweils, den Kosinus, den Sinus, den negativen Sinus und Kosinus des Drehwinkels an.

Wenn die *Drehung* erfolgt, werden die Punkte, die ein Objekt bilden, in Bezug auf den Ursprung des Koordinaten Raums gedreht. Die folgende Abbildung zeigt ein Rechteck von 20 bis 20 Einheiten, das 30 Grad gedreht wurde, wenn es aus dem weltweiten Koordinatenraum in den Bereich der Seiten Koordinate kopiert wurde.

![Abbildung, die zwei Koordinaten Bereiche anzeigt. Jeder hat eine rechge an einem anderen Speicherort und mit einer anderen Drehung.](images/cstrn-11.png)

In der obigen Abbildung wurde jeder Punkt im Rechteck in Bezug auf den Koordinatenraum Ursprung um 30 Grad gedreht.

Der folgende Algorithmus berechnet die neue x-Koordinate (x ") für einen Punkt (x, y), der in Bezug auf den Koordinatenraum Ursprung von Winkel a gedreht wird.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

Der folgende Algorithmus berechnet die y-Koordinate (y ") für einen Punkt (x, y), der durch den Winkel a in Bezug auf den Ursprung gedreht wird.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

Die beiden Drehungs Transformationen können wie folgt in einer 2 x 2-Matrix kombiniert werden.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

Die 2 x 2-Matrix, die die Drehung erzeugt hat, enthält die folgenden Werte.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Ableitung von Rotations Algorithmen

Rotations Algorithmen basieren auf dem Additions Theorem von Trigonometry, das besagt, dass die trigonometrische Funktion einer Summe von zwei Winkeln (a1 und a2) in Form der trigonometrischen Funktionen der beiden Winkel ausgedrückt werden kann.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

In der folgenden Abbildung wird eine Punkt-p-Drehung gegen den Uhrzeigersinn zu einer neuen Position p "gezeigt. Darüber hinaus werden zwei Dreiecke angezeigt, die durch eine Linie gebildet werden, die vom Koordinatenraum Ursprung bis zu jedem Punkt gezeichnet wird, und eine Linie, die von jedem Punkt durch die x-Achse gezeichnet wird.

![das Diagramm zeigt den Ursprung, p und p "und zwei Dreiecke](images/cstrn-12.png)

Bei Verwendung von Trigonometry kann die x-Koordinate von Punkt p durch Multiplizieren der Länge der Hypotenuse h durch den Kosinus von a1 abgerufen werden.

``` syntax
x = h * cos A1 
```

Die y-Koordinate von Punkt p kann abgerufen werden, indem die Länge der Hypotenuse h mit dem Sinus von a1 multipliziert wird.

``` syntax
y = h * sin A1 
```

Ebenso kann die x-Koordinate des Punkts p ' abgerufen werden, indem die Länge der Hypotenuse h durch den Kosinus von (a1 + a2) multipliziert wird.

``` syntax
x' = h * cos (A1 + A2) 
```

Schließlich kann die y-Koordinate von Punkt p ' abgerufen werden, indem die Länge der Hypotenuse h mit dem Sinus von (a1 + a2) multipliziert wird.

``` syntax
y' = h * sin (A1 + A2) 
```

Mit dem Additions-Theorem werden die vorangehenden Algorithmen wie folgt verwendet:

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Die Rotations Algorithmen für einen bestimmten Punkt, der durch den Winkel a2 gedreht wird, können durch die Ersetzung von x für jedes Vorkommen von (h \* cos a1) und durch Ersetzen von y für jedes Vorkommen von (h \* Sin a1) abgerufen werden.

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



