---
title: On-Attribut (Fill)(VML)
description: On-Attribut (Fill)(VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee692bf1beb8c9a7c79b50ef8be3c115deea615f18ee6702d0817d4f81439555
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680640"
---
# <a name="on-attribute-fillvml"></a>On-Attribut (Fill)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die Füllung angezeigt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* on=" *ausdruck* ">

**Skriptsyntax**

*element* .on="*expression*"

*expression* = *Element*.on

**Anmerkungen**

**False** gibt an, dass die Füllung nicht angezeigt wird. Der Standardwert ist **True**.

*VML-Standardattribut*

**Beispiel**

Obwohl die Füllung als rot definiert ist, wird sie nicht angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 