---
description: Die meisten CAD- und Zeichnungsanwendungen bieten Features, die die vom Benutzer erstellte Ausgabe skalieren.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf8cb7293be4083c08de1d104bb8349b3cd5003a0abddf77d41922cfb294cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965240"
---
# <a name="scaling"></a>Skalierung

Die meisten CAD- und Zeichnungsanwendungen bieten Features, die die vom Benutzer erstellte Ausgabe skalieren. Anwendungen, die Skalierungsfunktionen (oder Zoomfunktionen) enthalten, rufen die [**SetWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) auf, um die entsprechende Transformation für den Raum auf der Seite festzulegen. Diese Funktion empfängt einen Zeiger auf eine [**XFORM-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-xform) die die entsprechenden Werte enthält. Die Elemente eM11 und eM22 von XFORM geben die Komponenten für horizontale und vertikale Skalierung an.

Bei der *Skalierung* werden die vertikalen und horizontalen Linien (oder Vektoren), die ein Objekt bilden, in Bezug auf die x- oder y-Achse gestreckt oder komprimiert. Die folgende Abbildung zeigt ein 20-mal-20-Einheiten-Rechteck, das vertikal auf das Doppelte seiner ursprünglichen Höhe skaliert wird, wenn es aus dem Raum der Weltkoordinaten in den Seitenkoordinatenraum kopiert wird.

![Abbildung eines kleinen Rechtecks im Raum der Welt und eines höheren Rechtecks im Seitenbereich](images/cstrn-10.png)

In der obigen Abbildung messen die vertikalen Linien, die die Seite des ursprünglichen Rechtecks definieren, 20 Einheiten, während die vertikalen Linien, die die Seiten des skalierten Rechtecks definieren, 40 Einheiten messen.

Die vertikale Skalierung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
y' = y * Dy 
```

Dabei ist y' die neue Länge, y die ursprüngliche Länge und Dy der vertikale Skalierungsfaktor.

Die horizontale Skalierung kann durch den folgenden Algorithmus dargestellt werden.

``` syntax
x' = x * Dx 
```

Wobei x' die neue Länge, x die ursprüngliche Länge und Dx der horizontale Skalierungsfaktor ist.

Die vertikalen und horizontalen Skalierungstransformationen können mithilfe einer 2-mal-2-Matrix in einem einzelnen Vorgang kombiniert werden.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

Die 2:2-Matrix, die die Skalierungstransformation erzeugt hat, enthält die folgenden Werte.

``` syntax
|1    0| 
|0    2| 
```

 

 



