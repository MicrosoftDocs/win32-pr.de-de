---
title: ID-Attribut (Pfad)(VML)
description: ID-Attribut (Pfad)(VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29fe87845616b0e93e47458cd5c96f25733edd3aea7b09af6088b057d8ce0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118845918"
---
# <a name="id-attribute-pathvml"></a>ID-Attribut (Pfad)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Ein Name, der einen eindeutigen Bezeichner für einen Pfad enthält. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *element* id=" *ausdruck* ">

**Skriptsyntax**

*element* .id="*expression*"

*expression* = *Element*.id

**Anmerkungen**

Verwenden **Sie ID,** um auf einen bestimmten Pfad zu verweisen. Nachdem Sie einen Pfad erstellt und ihm eine ID gegeben haben, können Sie den ID-Namen verwenden, wenn Sie den Pfad bearbeiten möchten.

*VML-Standardattribut*

**Beispiel**

Die Form verfügt über eine Pfad-ID namens "myPath".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 