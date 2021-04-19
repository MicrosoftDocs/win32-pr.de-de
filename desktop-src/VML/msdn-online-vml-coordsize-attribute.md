---
title: VML coordsize-Attribut
description: VML coordsize-Attribut
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341939"
---
# <a name="vml-coordsize-attribute"></a>VML coordsize-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt die horizontalen und vertikalen Einheiten des Rechtecks an, das eine Form umschließt. Lese-/Schreibzugriff. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* coordsize = " *Expression* " >

**Skript Syntax**

*Element* . coordsize = "*Ausdruck*"

*Ausdruck* = *Element*. coordsize

**Anmerkungen**

Wenn nicht angegeben, ist die Koordinaten Größe mit dem umgebenden Feld der Form identisch.

Beachten Sie, dass es sich bei diesem Attribut um einen Vektor handelt und dass die Einheiten relativ zur Länge und Breite des umgebenden Rechtecks sind.

Beachten Sie auch, dass die Zuordnung zwischen **coordsize** und dem umgebenden Feld zu einem anisotrope gemacht werden kann. Stellen Sie sicher, dass die **Breite** und die Höhe von **coordsize** mit der **Breite und** **Höhe** des Formats identisch sind, wenn Sie die Form nicht verzerren möchten.

Da es sich hierbei um einen 2-D-Vektor handelt, können Sie bei der Skripterstellung separat auf die x-und y-Werte zugreifen und auch den Typ der erwarteten Einheiten festlegen.

*VML-Standard Attribut*

**Beispiel**

Die Form ist 100 Punkte hoch und 100 Punkte breit, aber jede horizontale und vertikale Einheit im Koordinaten Bereich ist 1/10 eines Punkts.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel für das coordsize-Attribut](/previous-versions/bb229665(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 