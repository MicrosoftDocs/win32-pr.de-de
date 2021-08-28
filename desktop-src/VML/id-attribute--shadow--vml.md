---
title: ID-Attribut (Schatten)(VML)
description: ID-Attribut (Schatten)(VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44cc307bcdd381247a105cc447e920819d3e8877bf66a81088bc8eabc8fa87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057918"
---
# <a name="id-attribute-shadowvml"></a>ID-Attribut (Schatten)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt einen Namen an, der einen eindeutigen Bezeichner für einen Schatten angibt. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* id=" *ausdruck* ">

**Skriptsyntax**

*element* .id="*expression*"

*expression* = *Element*.id

**Anmerkungen**

Verwenden **Sie ID,** um auf einen bestimmten Schatten zu verweisen. Nachdem Sie einen Schatten erstellt und ihm eine ID gegeben haben, können Sie den ID-Namen verwenden, wenn Sie den Schatten bearbeiten möchten.

*VML-Standardattribut*

**Beispiel**

Die Form verfügt über eine Schatten-ID namens "myshadow".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 