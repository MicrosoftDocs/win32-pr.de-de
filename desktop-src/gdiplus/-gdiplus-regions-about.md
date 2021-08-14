---
description: Ein Bereich ist ein Teil der Anzeigeoberfläche.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Regionen (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd15a7a25b341556b312c540f6fa4caf870da75aa4973be1d7c1e8102511e6ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885017"
---
# <a name="regions-gdi"></a>Regionen (GDI+)

Ein Bereich ist ein Teil der Anzeigeoberfläche. Bereiche können einfach (ein einzelnes Rechteck) oder komplex (eine Kombination aus Polygonen und geschlossenen Kurven) sein. Die folgende Abbildung zeigt zwei Bereiche: einen, der aus einem Rechteck und der andere aus einem Pfad erstellt wurde.

![Abbildung eines transparenten rechteckigen Bereichs, der eine nicht transparente gekrümmte Form überschneiden](images/aboutgdip02-art27.png)

Regionen werden häufig für Clipping- und Treffertests verwendet. Das Clipping umfasst das Einschränken des Zeichnens auf einen bestimmten Bereich des Bildschirms, in der Regel auf den Teil des Bildschirms, der aktualisiert werden muss. Beim Treffertest wird überprüft, ob sich der Cursor in einem bestimmten Bereich des Bildschirms befindet, wenn eine Maustaste gedrückt wird.

Sie können einen Bereich aus einem Rechteck oder aus einem Pfad erstellen. Sie können auch komplexe Regionen erstellen, indem Sie vorhandene Regionen kombinieren. Die [**Region-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) bietet die folgenden Methoden zum Kombinieren von Regionen: [Überschneiden,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)) [Union,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)) [Xor,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))und [**Region::Complement**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).

Die Schnittmenge zweier Regionen ist die Gruppe aller Punkte, die zu beiden Regionen gehören. Die Union ist der Satz aller Punkte, die zu einer oder den anderen oder beiden Regionen gehören. Das Komplement einer Region ist der Satz aller Punkte, die sich nicht in der Region befinden. Die folgende Abbildung zeigt die Schnittmenge und Vereinigung der beiden Regionen in der vorherigen Abbildung.

![Abbildung, die die Schnittmenge der Bereiche in der vorherigen Abbildung und deren Schnittmenge zeigt](images/aboutgdip02-art28.png)

Die [Xor-Methode,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) die auf ein Regionspaar angewendet wird, erzeugt eine Region, die alle Punkte enthält, die zu einer Region oder der anderen gehören, aber nicht beide. Die [](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) Exclude-Methode, die auf ein Regionspaar angewendet wird, erzeugt eine Region, die alle Punkte in der ersten Region enthält, die sich nicht in der zweiten Region befinden. Die folgende Abbildung zeigt die Regionen, die sich aus der Anwendung der Xor- und Exclude-Methode auf die beiden am Anfang dieses Themas gezeigten Regionen ergeben.

![Abbildung, die die Teile in beiden Regionen, jedoch nicht in beiden, und den Teil des Rechtecks zeigt, der den gekrümmten Bereich nicht überlappt](images/aboutgdip02-art29.png)

Um einen Bereich zu füllen, benötigen Sie ein [**Grafikobjekt,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ein [**Brush-Objekt**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) und ein [**Region-Objekt.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) Das **Graphics-Objekt** stellt die [**Graphics::FillRegion-Methode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) zur Hand, und das **Brush-Objekt** speichert Attribute der Füllung, z. B. Farbe oder Muster. Im folgenden Beispiel wird ein Bereich mit einer Volltonfarbe auffüllt.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
