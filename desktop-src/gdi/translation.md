---
description: Einige Anwendungen übersetzen (oder verschieben) Objekte, die im Client Bereich gezeichnet werden.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Sprachübersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988180"
---
# <a name="translation"></a>Sprachübersetzung

Einige Anwendungen übersetzen (oder verschieben) Objekte, die im Client Bereich gezeichnet werden. durch Aufrufen der [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion zum Festlegen der entsprechenden Welt Raum-und Seiten Raum Transformation. Die setworldtransform-Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält. Die EDX-und Edy-Member von XForm geben die horizontalen bzw. vertikalen Übersetzungs Komponenten an.

Wenn die *Übersetzung* auftritt, wird jeder Punkt in einem Objekt vertikal, horizontal oder beides um einen angegebenen Betrag verschoben. Die folgende Abbildung zeigt ein Rechteck mit 20 x 20 Einheiten, das beim Kopieren aus der weltweiten Koordinaten Fläche in den Bereich der Seiten Koordinate nach rechts um 10 Einheiten übersetzt wurde.

![Darstellung eines Rechtecks an einer Position im Raum der Welt und an einer anderen Position im Seitenbereich](images/cstrn-09.png)

In der obigen Abbildung ist die x-Koordinate der einzelnen Punkte im Rechteck 10 Einheiten größer als die ursprüngliche x-Koordinate.

Die horizontale Übersetzung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
x' = x + Dx 
```

Where x ' ist die neue x-Koordinate, x ist die ursprüngliche x-Koordinate, und DX ist die horizontale Entfernung, die verschoben wird.

Die vertikale Übersetzung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
y' = y + Dy 
```

Dabei ist y ' die neue y-Koordinate, y ist die ursprüngliche y-Koordinate, und dy ist der vertikale Abstand verschoben.

Die horizontalen und vertikalen Übersetzungs Transformationen können mithilfe einer 3 x 3-Matrix zu einem einzelnen Vorgang kombiniert werden.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(Die Regeln der Matrix Multiplikation geben an, dass die Anzahl der Zeilen in einer Matrix der Anzahl der Spalten im anderen entsprechen muss. Die Ganzzahl 1 in der Matrix \| x y 1 \| ist ein Platzhalter, der hinzugefügt wurde, um diese Anforderung zu erfüllen.)

Die 3-x-3-Matrix, die die veranschaulichte Übersetzungs Transformation erzeugt hat, enthält die folgenden Werte.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



