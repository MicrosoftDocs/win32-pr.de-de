---
title: VML-Attribut "strokeweight"
description: VML-Attribut "strokeweight"
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728072"
---
# <a name="vml-strokeweight-attribute"></a>VML-Attribut "strokeweight"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Pinsel Stärke, mit der der Pfad einer Form festgelegt wird. Lese-/Schreibzugriff. **Vglength**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* strokeweight = " *Expression* " >

**Skript Syntax**

*Element* . strokeweight = "*Ausdruck*"

*Ausdruck* = *Element*. strokeweight

**Anmerkungen**

Der Wert wird aus dem **Weight** -Attribut des **Stroke** -Elements dupliziert. Wenn eine Zahl angegeben, aber keine Einheiten hinzugefügt werden, ist die Standard Maßeinheit die EWU. Wenn kein Wert angegeben wird, ist der Standardwert 1 Pixel (1px).

Bei der Skripterstellung wird jedoch die Standard Maßeinheit in Punkten angezeigt.

*VML-Standard Attribut*

**Siehe auch**

[Strich](msdn-online-vml-stroke-element.md), [ivglength](msdn-online-vml-vglength.md), [Einheiten](msdn-online-vml-units.md)

**Beispiel**

Die Strich Gewichtung der Form ist 1 Punkt.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel für ein strokeweight-Attribut](/previous-versions/bb264095(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 