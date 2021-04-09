---
title: VML coordorigin-Attribut
description: VML coordorigin-Attribut
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858280"
---
# <a name="vml-coordorigin-attribute"></a>VML coordorigin-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt den Koordinaten Einheits Ursprung des Rechtecks an, das eine Form umschließt. Lese-/Schreibzugriff. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* coordorigin = " *Expression* " >

**Skript Syntax**

*Element* . coordorigin = "*Ausdruck*"

*Ausdruck* = *Element*. coordorigin

**Anmerkungen**

Wenn kein Wert angegeben wird, sind die Ursprungs Koordinaten (0,0) in der oberen linken Ecke des umgebenden Felds der Form.

Der x-Wert von **coordsize** wird dem x-Wert von **coordorigin** hinzugefügt, um den Bereich der horizontalen Werte zu bestimmen. Wenn der x-Wert von **coordorigin** z. b.-100 und der x-Wert von **coordsize** 200 beträgt, liegen die horizontalen Einheiten zwischen-100 und + 100. Wenn der x-Wert von **coordorigin** 100 und der x-Wert von **coordsize** 200 ist, reichen die horizontalen Einheiten zwischen 100 und 300, alle innerhalb des umgebenden Felds. Das gleiche gilt für die y-Werte.

Beachten Sie, dass es sich bei diesem Attribut um einen Vektor handelt und dass die Einheiten denselben Typ von Einheit wie [coordsize](msdn-online-vml-coordsize-attribute.md) haben.

Da es sich hierbei um einen 2-D-Vektor handelt, können Sie bei der Skripterstellung separat auf die x-und y-Werte zugreifen und auch den Typ der erwarteten Einheiten festlegen.

*VML-Standard Attribut*

**Beispiel**

Der Mittelpunkt des umgebenden Felds ist der Ursprung (0,0) des Pfads für die Form. Da **coordorigin** den Wert "-500-500" und **coordsize** den Wert "1000 1000" hat, reichen die horizontalen und vertikalen Einheiten zwischen-500 und + 500. Die linke und obere Ecke des Pfads befinden sich in der Mitte des umgebenden Felds, das durch den linken und den oberen Punkt definiert wird, wie durch **Style** definiert.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel für das coordorigin-Attribut](/previous-versions/bb229664(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 