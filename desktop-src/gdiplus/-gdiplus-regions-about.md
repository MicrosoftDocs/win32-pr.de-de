---
description: Ein Bereich ist ein Teil der Anzeige Oberfläche.
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: Regionen (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d6a7f0a5a6d3df4b11a491111dbedf9e155c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566133"
---
# <a name="regions-gdi"></a>Regionen (GDI+)

Ein Bereich ist ein Teil der Anzeige Oberfläche. Bereiche können einfach (ein einzelnes Rechteck) oder komplex sein (eine Kombination aus Polygonen und geschlossenen Kurven). Die folgende Abbildung zeigt zwei Bereiche: eine, die aus einem Rechteck erstellt wurde, und die andere, die aus einem Pfad erstellt wurde.

![Darstellung eines transparenten rechteckigen Bereichs, der sich überschneidet](images/aboutgdip02-art27.png)

Regionen werden häufig für Clipping-und Treffer Tests verwendet. Das Clipping umfasst das Einschränken der Zeichnung auf einen bestimmten Bereich des Bildschirms, in der Regel auf den Teil des Bildschirms, der aktualisiert werden muss. Bei Treffer Tests muss überprüft werden, ob sich der Cursor in einem bestimmten Bereich des Bildschirms befindet, wenn eine Maustaste gedrückt wird.

Sie können einen Bereich aus einem Rechteck oder einem Pfad erstellen. Sie können auch komplexe Regionen erstellen, indem Sie vorhandene Regionen kombinieren. Die [**Regions**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) Klasse stellt die folgenden Methoden zum Kombinieren von Bereichen bereit: [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)), [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))und [**Region:: Komplement**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).

Die Schnittmenge zweier Regionen ist der Satz aller Punkte, die zu beiden Regionen gehören. Die Union ist der Satz aller Punkte, die zu einer oder den beiden Regionen gehören. Das Komplement einer Region ist der Satz aller Punkte, die sich nicht in der Region befinden. Die folgende Abbildung zeigt die Schnittmenge und die Gesamtmenge der beiden Regionen in der vorherigen Abbildung.

![Darstellung der Schnittmenge der Regionen in der vorherigen Abbildung und ihrer Schnittmenge](images/aboutgdip02-art28.png)

Die auf ein paar von Regionen angewendete [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) -Methode erzeugt einen Bereich, der alle Punkte enthält, die zu einem Bereich oder dem anderen gehören, aber nicht beides. Die auf ein paar von Regionen angewendete [Ausschluss](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) Methode erzeugt einen Bereich, der alle Punkte in der ersten Region enthält, die sich nicht in der zweiten Region befinden. Die folgende Abbildung zeigt die Bereiche, die sich aus der Anwendung der Xor-Methode und der Exclude-Methode auf die beiden Regionen am Anfang dieses Themas ergeben.

![Darstellung der Teile in einem Bereich, aber nicht beides und der Teil des Rechtecks, das sich nicht überschneidet](images/aboutgdip02-art29.png)

Um einen Bereich auszufüllen, benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pinsel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekt und ein [**Regions**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) Objekt. Das **graphics** -Objekt stellt die [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) -Methode bereit, und das **Brush** -Objekt speichert Attribute der Füllung, z. b. Farbe oder Muster. Im folgenden Beispiel wird ein Bereich mit einer voll Tonfarbe gefüllt.


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
