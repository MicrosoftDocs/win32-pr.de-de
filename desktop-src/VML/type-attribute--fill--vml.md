---
title: Typattribut (Fill)(VML)
description: Typattribut (Fill)(VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883318c82758178ee9693a1199cb76c5798e351ec809aecb54fe7d0a266d85d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596141"
---
# <a name="type-attribute-fillvml"></a>Typattribut (Fill)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt den Typ der Füllung. Lese-/Schreibzugriff. **VgFillType**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* type="-Ausdruck "> 

**Skriptsyntax**

*element* .type="*expression*"

*expression* = *Element*.type

**Anmerkungen**

Mögliche Werte:



| Typ           | BESCHREIBUNG                                                             |
|----------------|-------------------------------------------------------------------------|
| Solide          | Das Füllmuster ist voll. Standard.                                     |
| Farbverlauf       | Die Füllfarben werden in einem linearen Farbverlauf von unten nach oben kombiniert. |
| gradientradial | Die Füllfarben werden in einem radialen Farbverlauf kombiniert.                    |
| tile           | Das Füllbild ist gekachelt.                                                |
| pattern        | Das Bild wird verwendet, um ein Muster mit den Füllfarben zu erstellen.            |
| frame          | Das Bild wird gestreckt, um die Form zu füllen.                               |



 

**VML-Standardattribut**

**Beispiel**

Eine rote Vordergrund- und blaue Hintergrundfüllung wird mithilfe des Musters des Bilds myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 