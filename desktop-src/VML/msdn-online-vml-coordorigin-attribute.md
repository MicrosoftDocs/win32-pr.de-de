---
title: VML-Attribut "CoordOrigin"
description: VML-Attribut "CoordOrigin"
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf568f2c305108a651d56a891a96890154f9493cbadd80a9c5610414c88f4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601942"
---
# <a name="vml-coordorigin-attribute"></a>VML-Attribut "CoordOrigin"

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den Ursprung der Koordinateneinheit des Rechtecks an, das eine Form umgibt. Lese-/Schreibzugriff. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* coordorigin="-Ausdruck "> 

**Skriptsyntax**

*element* .coordorigin="*expression*"

*expression* = *Element*.coordorigin

**Anmerkungen**

Wenn kein Wert angegeben wird, befinden sich die Ursprungskoordinaten (0,0) in der oberen linken Ecke des Umrandungsfelds der Form.

Der x-Wert **von CoordSize** wird dem x-Wert von **CoordOrigin** hinzugefügt, um den Bereich der horizontalen Werte zu bestimmen. Wenn der x-Wert von **CoordOrigin** beispielsweise -100 und der x-Wert von **CoordSize** 200 beträgt, liegen die horizontalen Einheiten zwischen -100 und +100. Wenn der x-Wert von **CoordOrigin** 100 und der x-Wert von **CoordSize** 200 beträgt, liegen die horizontalen Einheiten zwischen 100 und 300 innerhalb des Begrenzungsfelds. Dasselbe gilt für die y-Werte.

Beachten Sie, dass dieses Attribut ein Vektor ist und dass die Einheiten denselben Typ von Einheit wie [CoordSize haben.](msdn-online-vml-coordsize-attribute.md)

Da es sich bei der Skripterstellung um einen 2D-Vektor handelt, können Sie separat auf die x- und y-Werte zugreifen und auch den erwarteten Einheitentyp bestimmen.

*VML-Standardattribut*

**Beispiel**

Die Mitte des Begrenzungsfelds ist der Ursprung (0,0) des Pfads für die Form. Da **CoordOrigin** "-500 -500" und **CoordSize** "1000 1000" ist, reichen die horizontalen und vertikalen Einheiten von -500 bis +500. Die linke und obere Ecke des Pfads befindet sich in der Mitte des Begrenzungsfelds, das durch den linken und oberen Punkt definiert wird, wie durch Format **definiert.**


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[CoordOrigin-Attribut – Beispiel.](/previous-versions/bb229664(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 