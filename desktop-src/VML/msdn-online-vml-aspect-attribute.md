---
title: VML-Aspektattribut
description: VML-Aspektattribut
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669b0f93e740e6bc4d4fb94155f6ca0ab60d5e00cebfb1604d5272d45d4dd8ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602897"
---
# <a name="vml-aspect-attribute"></a>VML-Aspektattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt an, wie das Seitenverhältnis des Füllbilds beibehalten wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* aspect=" *ausdruck* ">

**Skriptsyntax**

*element* .aspect="*expression*"

*expression* = *Element*.aspect

**Anmerkungen**

Mögliche Werte:



| Wert   | Beschreibung                           |
|---------|---------------------------------------|
| ignore  | Ignorieren sie Aspektprobleme. Standard.        |
| Atleast | Image ist mindestens so groß wie **Größe.** |
| atmost  | Image ist nicht größer als **Größe**.     |



 

*VML-Standardattribut*

**Beispiel**

Das Bild, aus dem die Füllung besteht, ist größer oder gleich einer Größe von 10 Punkten um 10 Punkte.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 