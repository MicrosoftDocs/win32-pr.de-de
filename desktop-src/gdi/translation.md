---
description: Einige Anwendungen übersetzen (oder verschieben) Objekte, die im Clientbereich gezeichnet werden.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Sprachübersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115af82d1e5b80fa4c50d081e6d042d2f2c9c8950f3b4b8f6ed09108df4c52bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613340"
---
# <a name="translation"></a>Sprachübersetzung

Einige Anwendungen übersetzen (oder verschieben) Objekte, die im Clientbereich gezeichnet werden. durch Aufrufen der [**SetWorldTransform-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) um die entsprechende Transformation für Den Raum auf Seitenbereich zu setzen. Die SetWorldTransform-Funktion empfängt einen Zeiger auf eine [**XFORM-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-xform) die die entsprechenden Werte enthält. Die eDx- und eDy-Member von XFORM geben die horizontalen bzw. vertikalen Übersetzungskomponenten an.

Bei *einer* Übersetzung wird jeder Punkt in einem Objekt um einen angegebenen Betrag vertikal, horizontal oder beides verschoben. Die folgende Abbildung zeigt ein Rechteck mit 20 bis 20 Einheiten, das beim Kopieren aus dem Weltkoordinatenraum in den Seitenkoordinatenraum um 10 Einheiten nach rechts übersetzt wurde.

![Abbildung eines Rechtecks an einer Position im Weltraum und an einer anderen Position im Seitenbereich](images/cstrn-09.png)

In der obigen Abbildung ist die x-Koordinate jedes Punkts im Rechteck 10 Einheiten größer als die ursprüngliche x-Koordinate.

Die horizontale Übersetzung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
x' = x + Dx 
```

Wobei x' die neue x-Koordinate, x die ursprüngliche x-Koordinate und Dx der horizontale Abstand ist.

Die vertikale Übersetzung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
y' = y + Dy 
```

Wobei y' die neue y-Koordinate, y die ursprüngliche y-Koordinate und Dy der vertikale Abstand ist.

Die horizontalen und vertikalen Übersetzungstransformationen können mithilfe einer 3 by 3-Matrix zu einem einzelnen Vorgang kombiniert werden.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(Die Regeln der Matrixmultiplikation geben an, dass die Anzahl der Zeilen in einer Matrix der Anzahl der Spalten in der anderen Matrix entsprechen muss. Die ganze Zahl 1 in der Matrix x y 1 ist ein Platzhalter, der hinzugefügt wurde, \| um diese Anforderung zu \| erfüllen.)

Die 3:3-Matrix, die die dargestellte Übersetzungstransformation erzeugt hat, enthält die folgenden Werte.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



