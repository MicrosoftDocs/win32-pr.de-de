---
title: VML-Masterattribut
description: VML-Masterattribut
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d126b9d02144bbc8831d7be9e73a3e5896c2ceccca71cfcbc8161d5ccc8112f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999110"
---
# <a name="vml-master-attribute"></a>VML-Masterattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein **ShapeType-Element** ein Masterelement ist. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[ShapeType](msdn-online-vml-shapetype-element.md)

**Tagsyntax**

<v: *element* o:master=" *ausdruck* ">

**Anmerkungen**

**True** gibt an, dass die **ShapeType-Form** von der Rendering-Engine gerendert wird. Der Standardwert ist **False**.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Das **ShapeType-Element** ist eine Masterform.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 