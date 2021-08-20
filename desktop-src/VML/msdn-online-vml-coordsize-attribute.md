---
title: VML CoordSize-Attribut
description: VML CoordSize-Attribut
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9ce79507e789c38512e775100aa27eda25dc61d5f2af56f9a677daf04d238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999190"
---
# <a name="vml-coordsize-attribute"></a>VML CoordSize-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt die horizontalen und vertikalen Einheiten des Rechtecks an, das eine Form umgibt. Lese-/Schreibzugriff. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* coordsize=" *ausdruck* ">

**Skriptsyntax**

*element* .coordsize="*expression*"

*expression* = *.coordsize-Element*

**Anmerkungen**

Wenn keine Angabe erfolgt, entspricht die Koordinatengröße dem begrenzungsfeld der Form.

Beachten Sie, dass dieses Attribut ein Vektor ist und dass die Einheiten relativ zur Länge und Breite des umgrenzenden Rechtecks sind.

Beachten Sie auch, dass die Zuordnung zwischen **coordsize** und dem Begrenzungsfeld als Anisotrope erfolgen kann. Stellen Sie sicher, dass die **Coordsize-Breite** und **coordsize-Höhe** mit der **Stilbreite** und **-höhe** identisch sind, wenn Sie die Form nicht verzerren möchten.

Da es sich bei der Skripterstellung um einen 2D-Vektor handelt, können Sie separat auf die x- und y-Werte zugreifen und auch den erwarteten Einheitentyp bestimmen.

*VML-Standardattribut*

**Beispiel**

Die Form ist 100 Punkte hoch und 100 Punkte breit, aber jede horizontale und vertikale Einheit im Koordinatenbereich beträgt 1/10 eines Punkts.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[CoordSize-Attribut – Beispiel.](/previous-versions/bb229665(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 