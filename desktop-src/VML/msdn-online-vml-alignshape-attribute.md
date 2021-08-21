---
title: VML AlignShape-Attribut
description: VML AlignShape-Attribut
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00e1fe8d07fb04c198ced2e2eb50d6ef0e6c020984d2d8cf12a3ca37cf09d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125313"
---
# <a name="vml-alignshape-attribute"></a>VML AlignShape-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Bild an einer Form ausgerichtet wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* alignshape=" *ausdruck* ">

**Skriptsyntax**

*element* .alignshape="*expression*"

*expression* = *Element*.alignshape

**Anmerkungen**

**True** gibt an, dass das zum Erstellen der Füllung verwendete Bild an der Form ausgerichtet ist. **False** gibt an, dass das zum Erstellen der Füllung verwendete Bild am Fenster ausgerichtet ist. Der Standardwert ist **true**.

*VML-Standardattribut*

**Beispiel**

Das aus myimage.gif erstellte kachelte Füllbild ist am Fenster ausgerichtet, nicht an der Form. obwohl die Form gedreht wird, ist das Bild nicht.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 