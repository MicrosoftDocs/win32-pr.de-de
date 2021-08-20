---
title: ID-Attribut (Stroke)(VML)
description: ID-Attribut (Stroke)(VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02fa8ad958315af58e2abfa6d374a6545cc1e3e171080ec29ac6a30600160184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125303"
---
# <a name="id-attribute-strokevml"></a>ID-Attribut (Stroke)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Ein Name, der einen eindeutigen Bezeichner für einen Strich enthält. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* id=" *ausdruck* ">

**Skriptsyntax**

*element* .id="*expression*"

*expression* = *Element*.id

**Anmerkungen**

Verwenden **Sie ID,** um auf einen bestimmten Strich zu verweisen. Nachdem Sie einen Strich erstellt und ihm eine ID gegeben haben, können Sie den ID-Namen verwenden, wenn Sie den Strich bearbeiten möchten.

*VML-Standardattribut*

**Beispiel**

Die Form hat eine Strich-ID namens "mystroke".


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 