---
title: VML CropBottom-Attribut
description: VML CropBottom-Attribut
ms.assetid: 9548d0fa-1708-4206-90d8-1d90cb42de87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667e5501f43d55dcc6a489406e4b10397c1a39773fad2fce7dc6f8601bf45024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601953"
---
# <a name="vml-cropbottom-attribute"></a>VML CropBottom-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Prozentsatz der Entfernung des Bilds von der unteren Seite. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* cropbottom=" *ausdruck* ">

**Skriptsyntax**

*element* .cropbottom="*expression*"

*expression* = *.cropbottom-Element*

**Anmerkungen**

Die Zuschneidemenge kann zwischen -1,0 und 1,0 liegen. Der Standardwert ist 0. Beachten Sie, dass der Wert 1 überhaupt kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der zugeschnittenen Kante nach innen gezogen wird (der leere Bereich zwischen dem Bild und dem zugeschnittenen Rand wird durch die Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gestreckt wird, um die Form anzupassen.

VML-Standardattribut

**Beispiel**

Es wird kein Bild angezeigt, da das Bild zu 100 % vom unteren Rand zugeschnitten ist.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropbottom="1" src="kids.jpg"/>
   </v:shape>
```



 

 