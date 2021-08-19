---
title: VML-Attribut "Key"
description: VML-Attribut "Key"
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d279f31ff4910ceb121242f587aac88585dba2cfc8278320c0d86680f4f330b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999310"
---
# <a name="vml-chromakey-attribute"></a>VML-Attribut "Key"

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Farbwert des Bilds, das als transparent behandelt wird. Lese-/Schreibzugriff. **VgColor**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *elementkey="* *ausdruck* ">

**Skriptsyntax**

*element* .key="*expression*"

*expression* = *element*.key

**Anmerkungen**

Verwenden Sie dieses Attribut, um Teile eines Bilds transparent zu machen, indem Sie die Transparenz auf eine bestimmte Farbe setzen. Wenn Sie z. **B. den Wert "Key"** **in Schwarz** setzen, ist jeder Teil des Bilds, der schwarz ist, transparent, und die Füllfarbe wird diesen Teil des Bilds "durchzeigen".

*VML-Standardattribut*

**Beispiel**

Die Bereiche des Bilds, die einfarbig schwarz sind, werden transparent, sodass die grüne Füllfarbe stattdessen durch diese Bereiche angezeigt werden kann.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 