---
title: VML-Attribut "V-Rotate Letters"
description: VML-Attribut "V-Rotate Letters"
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779f7878b01765416560dacaed5e3b81a1e00a25d4bf7c53e0071c8bb487d16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123780"
---
# <a name="vml-v-rotate-letters-attribute"></a>VML-Attribut "V-Rotate Letters"

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die Buchstaben des Texts gedreht werden. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="v-rotate-letters: *expression* ">

**Skriptsyntax**

*element* .style.v-rotate-letters="*expression*"

*expression* = *Element*.style.v-rotate-letters

**Anmerkungen**

True **gibt an,** dass die Buchstaben des Texts um 90 Grad gedreht werden. Der Standardwert ist **False**.

*VML-Standardattribut*

**Beispiel**

Die Buchstaben werden um 90 Grad gedreht.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 