---
description: Die meisten CAD-und Zeichnungs Anwendungen bieten Features, mit denen die vom Benutzer erstellte Ausgabe skaliert wird.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980304"
---
# <a name="scaling"></a>Skalierung

Die meisten CAD-und Zeichnungs Anwendungen bieten Features, mit denen die vom Benutzer erstellte Ausgabe skaliert wird. Anwendungen, die Skalierungs-(oder Zoom-) Funktionen enthalten, setzen die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion ein, um die entsprechende Welt Raum-und Seiten Raum Transformation festzulegen. Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält. Die eM11-und eM22-Member von XForm geben die horizontalen bzw. vertikalen Skalierungs Komponenten an.

Wenn die *Skalierung* erfolgt, werden die vertikalen und horizontalen Linien (oder Vektoren), die ein Objekt bilden, in Bezug auf die x-oder y-Achse gestreckt oder komprimiert. In der folgenden Abbildung wird ein Rechteck mit einer Breite von 20 und 20 Einheiten dargestellt, das vertikal auf die ursprüngliche Höhe skaliert wird, wenn es aus dem weltweiten Koordinatenraum in den Seiten Koordinaten Bereich kopiert wurde.

![Darstellung eines kleinen Rechtecks im Raum der Welt und eines größeren Rechtecks im Seitenbereich](images/cstrn-10.png)

In der obigen Abbildung sind die vertikalen Linien, die die Seite des ursprünglichen Rechtecks definieren, 20 Einheiten, während die vertikalen Linien, die die Seiten des skalierten Rechtecks definieren, 40 Einheiten messen.

Die vertikale Skalierung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
y' = y * Dy 
```

Dabei ist y ' die neue Länge, y ist die ursprüngliche Länge, und dy ist der vertikale Skalierungsfaktor.

Die horizontale Skalierung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
x' = x * Dx 
```

Wobei x ' die neue Länge, x die ursprüngliche Länge und DX der Faktor für die horizontale Skalierung ist.

Die vertikalen und horizontalen Skalierungs Transformationen können mithilfe einer 2-x-2-Matrix zu einem einzelnen Vorgang kombiniert werden.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

Die 2 x 2-Matrix, die die Skalierungs Transformation erzeugt hat, enthält die folgenden Werte.

``` syntax
|1    0| 
|0    2| 
```

 

 



