---
title: ID-Attribut (Pfad) (VML)
description: ID-Attribut (Pfad) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101666"
---
# <a name="id-attribute-pathvml"></a>ID-Attribut (Pfad) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Ein Name, der einen eindeutigen Bezeichner für einen Pfad bereitstellt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* -ID = " *Ausdruck* " >

**Skript Syntax**

*Element* . ID = "*Ausdruck*"

*Ausdruck* = *Element*. ID

**Anmerkungen**

Verwenden Sie **ID** , um auf einen bestimmten Pfad zu verweisen. Nachdem Sie einen Pfad erstellt und ihm eine ID zugewiesen haben, können Sie den ID-Namen verwenden, wenn Sie den Pfad bearbeiten möchten.

*VML-Standard Attribut*

**Beispiel**

Die Form hat eine Pfad-ID mit dem Namen "myPath".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 