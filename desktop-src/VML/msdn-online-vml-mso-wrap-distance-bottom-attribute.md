---
title: VML-Attribut "MSO-Wrap-Distance-Bottom"
description: VML-Attribut "MSO-Wrap-Distance-Bottom"
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e28ea0f2d84b9bf9f5981f9ebb22f15af75a2071f07dd9f3e006ac70b34256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007680"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a>VML-Attribut "MSO-Wrap-Distance-Bottom"

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Abstand zwischen der unteren Seite der Form und dem Text, der sie umschließt. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="mso-wrap-distance-bottom: *expression* ">

**Anmerkungen**

Beachten Sie, dass sich dieses Attribut vom CSS **Margin-Attribut** abt. **Der Rand** ändert den Ursprung der Form so, dass er die Randbereiche einnimmt, aber der Umbruchabstand in Microsoft Office ändert nicht den Ursprung der Form.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form hat einen unteren Umbruchabstand von 10 Punkten.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-bottom:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 