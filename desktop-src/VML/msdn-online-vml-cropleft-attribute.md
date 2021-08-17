---
title: VML-CropLeft-Attribut
description: VML-CropLeft-Attribut
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26112aa969e95c6bfb1ec715024aca9eb17b2dbfc2d7d214fb3679cf7ab77447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754850"
---
# <a name="vml-cropleft-attribute"></a>VML-CropLeft-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Prozentsatz der Entfernung des Bilds von der linken Seite. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* cropleft=" *ausdruck* ">

**Skriptsyntax**

*element* .cropleft="*expression*"

*expression* = *.cropleft-Element*

**Anmerkungen**

Die Zuschneidemenge kann zwischen -1,0 und 1,0 liegen. Der Standardwert ist 0. Beachten Sie, dass der Wert 1 überhaupt kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der zugeschnittenen Kante nach innen gezogen wird (der leere Bereich zwischen dem Bild und dem zugeschnittenen Rand wird durch die Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gestreckt wird, um die Form anzupassen.

*VML-Standardattribut*

**Beispiel**

20 % des Bilds werden auf der linken Seite entfernt, und das verbleibende Bild wird gestreckt, um es an die Form anzupassen.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 