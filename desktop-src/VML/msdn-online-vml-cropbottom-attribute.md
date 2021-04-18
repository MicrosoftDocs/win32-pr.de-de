---
title: VML-Attribut "CropBottom"
description: VML-Attribut "CropBottom"
ms.assetid: 9548d0fa-1708-4206-90d8-1d90cb42de87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b847fcd061e13418efe04b6ea27795a19002abf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315326"
---
# <a name="vml-cropbottom-attribute"></a>VML-Attribut "CropBottom"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Prozentsatz der Bild Entfernung von der unteren Seite. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* CropBottom = " *Expression* " >

**Skript Syntax**

*Element* . CropBottom = "*Ausdruck*"

*Ausdruck* = *Element*. CropBottom

**Anmerkungen**

Der Wert für das Zuschneiden kann zwischen-1,0 und 1,0 liegen. Der Standardwert ist 0. Beachten Sie, dass bei einem Wert von 1 überhaupt kein Bild angezeigt wird. Negative Werte führen dazu, dass das Bild von der Kante, die zugeschnitten wird, nach innen gedrückt wird (der leere Bereich zwischen dem Bild und dem Rand der Kante wird durch die Füllfarbe der Form aufgefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild so gestreckt wird, dass es der Form entspricht.

VML-Standard Attribut

**Beispiel**

Es wird kein Bild angezeigt, da das Bild von unten nach 100% zugeschnitten ist.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropbottom="1" src="kids.jpg"/>
   </v:shape>
```



 

 