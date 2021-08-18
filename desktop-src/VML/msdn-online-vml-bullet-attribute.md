---
title: VML-Aufzählungsattribut
description: VML-Aufzählungsattribut
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f35fda917931567dcd2dc4cf823ed74e3b449e05fba6046f1390e3d6454fd45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755019"
---
# <a name="vml-bullet-attribute"></a>VML-Aufzählungsattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob eine Form ein grafischer Aufzählungszeichen ist. Lese-/Schreibzugriff **auf VgTriState**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:bullet=" *ausdruck* ">

**Anmerkungen**

Der Standardwert ist **False**. **True** gibt an, dass die Form ein grafischer Aufzählungszeichen ist.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form ist ein Aufzählungszeichen.


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 