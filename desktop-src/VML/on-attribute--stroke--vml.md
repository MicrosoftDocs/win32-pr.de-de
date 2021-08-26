---
title: On-Attribut (Strich)(VML)
description: On-Attribut (Strich)(VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5682200a44a98d2b4c074b11db172e2b94b812a196a404927a33b4d142289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007570"
---
# <a name="on-attribute-strokevml"></a>On-Attribut (Strich)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob der Strich angezeigt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* on=" *ausdruck* ">

**Skriptsyntax**

*element* .on="*expression*"

*expression* = *.on-Element*

**Anmerkungen**

False gibt an, dass der Strich nicht angezeigt wird. Der Standardwert ist **True**.

*VML-Standardattribut*

**Beispiel**

Der Strich wird nicht angezeigt.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 