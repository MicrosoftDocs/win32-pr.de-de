---
title: VML-Attribut "CropLeft"
description: VML-Attribut "CropLeft"
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff01af761e7177d866b46ed48e5d633506aa63fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209263"
---
# <a name="vml-cropleft-attribute"></a>VML-Attribut "CropLeft"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Prozentsatz der Bild Entfernung von der linken Seite. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* CropLeft = " *Expression* " >

**Skript Syntax**

*Element* . CropLeft = "*Ausdruck*"

*Ausdruck* = *Element*. CropLeft

**Anmerkungen**

Der Wert für das Zuschneiden kann zwischen-1,0 und 1,0 liegen. Der Standardwert ist 0. Beachten Sie, dass bei einem Wert von 1 überhaupt kein Bild angezeigt wird. Negative Werte führen dazu, dass das Bild von der Kante, die zugeschnitten wird, nach innen gedrückt wird (der leere Bereich zwischen dem Bild und dem Rand der Kante wird durch die Füllfarbe der Form aufgefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild so gestreckt wird, dass es der Form entspricht.

*VML-Standard Attribut*

**Beispiel**

20% des Bilds werden auf der linken Seite entfernt, und das verbleibende Bild wird gestreckt, damit es an die Form angepasst wird.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 