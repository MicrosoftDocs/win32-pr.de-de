---
title: VML-Attribut "CropTop"
description: VML-Attribut "CropTop"
ms.assetid: b54939b6-0505-43b0-bf82-c3df82dc2633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8b2606c7ac5835caeecc145a885de48eaeaf8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315320"
---
# <a name="vml-croptop-attribute"></a>VML-Attribut "CropTop"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Prozentsatz der Bild Entfernung von der oberen Seite aus. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* CropTop = " *Expression* " >

**Skript Syntax**

*Element* . CropTop = "*Ausdruck*"

*Ausdruck* = *Element*. CropTop

**Anmerkungen**

Der Wert für das Zuschneiden kann zwischen-1,0 und 1,0 liegen. Der Standardwert ist 0. Beachten Sie, dass bei einem Wert von 1 überhaupt kein Bild angezeigt wird. Negative Werte führen dazu, dass das Bild von der Kante, die zugeschnitten wird, nach innen gedrückt wird (der leere Bereich zwischen dem Bild und dem Rand der Kante wird durch die Füllfarbe der Form aufgefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild so gestreckt wird, dass es der Form entspricht.

*VML-Standard Attribut*

**Beispiel**

Das Bild wird am unteren Rand der Form in einen schmalen Farbname gedrückt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata croptop="-.8" src="kids.jpg"/>
   </v:shape>
```





 

 