---
title: VML CropRight-Attribut
description: VML CropRight-Attribut
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d695bb3fd9e88c3357343860dcbbff820e5a49a22100d59fe46c502b642e31d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796300"
---
# <a name="vml-cropright-attribute"></a>VML CropRight-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Prozentsatz der Entfernung des Bilds von der rechten Seite. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* cropright=" *ausdruck* ">

**Skriptsyntax**

*element* .cropright="*expression*"

*expression* = *.cropright-Element*

**Anmerkungen**

Die Zuschneidemenge kann zwischen -1,0 und 1,0 liegen. Der Standardwert ist 0. Beachten Sie, dass der Wert 1 überhaupt kein Bild anzeigt. Negative Werte führen dazu, dass das Bild von der zugeschnittenen Kante nach innen gezogen wird (der leere Bereich zwischen dem Bild und dem zugeschnittenen Rand wird durch die Füllfarbe der Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild gestreckt wird, um die Form anzupassen.

*VML-Standardattribut*

**Beispiel**

Das Bild wird von der rechten Seite um 20 % der Breite dargestellt. Der leere Bereich zwischen dem Bild und dem rechten Rand wird durch die Füllfarbe der Form gefüllt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 