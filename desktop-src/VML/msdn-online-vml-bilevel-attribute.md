---
title: VML Bilevel-Attribut
description: VML Bilevel-Attribut
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b84f77777cfa21a5bd5c80cb59e447c5a5ce1da78875cc9bd5ff07548690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602870"
---
# <a name="vml-bilevel-attribute"></a>VML Bilevel-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Bild in Schwarz/Weiß angezeigt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* bilevel="-Ausdruck "> 

**Skriptsyntax**

*element* .bilevel="*expression*"

*expression* = .bilevel-Element

**Anmerkungen**

True **gibt an,** dass das Bild mit zwei Farben (Schwarz und Weiß) angezeigt wird. Der Standardwert ist **False**. Dadurch entsteht ein Effekt, der der Nachpostisierung ähnelt.

*VML-Standardattribut*

**Beispiel**

Das Bild wird nur in Schwarz und Weiß angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 