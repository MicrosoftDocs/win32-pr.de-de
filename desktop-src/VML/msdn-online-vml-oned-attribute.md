---
title: VML OnEd-Attribut
description: VML OnEd-Attribut
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ef444037a0cd05a7cfbed5a97bb93ed7e8236a9d9f66bf1f7bd77b92b82e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999150"
---
# <a name="vml-oned-attribute"></a>VML OnEd-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die zusätzlichen Handles einer Form ausgeblendet sind. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:oned=" *ausdruck* ">

**Anmerkungen**

Blendet alle Formhandles außer oben links und unten rechts aus. Das heißt, die gleichen Handles, die für ein gerades Liniensegment verwendet werden. Der Standardwert ist **False**.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Bis auf die oberen linken und unteren rechten Ziehpunkte der Form werden alle ausgeblendet.


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 