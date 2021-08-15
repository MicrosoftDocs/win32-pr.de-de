---
title: VMLFont-Family Attribut
description: VMLFont-Family Attribut
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1254be6f7264e0d8f77d5881a11b9c2ec5085a931a0cad713813c059c60e5e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754737"
---
# <a name="vml-font-family-attribute"></a>VMLFont-Family Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Familie der Textpfadschriftart. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="font-family: *expression* ">

**Skriptsyntax**

*element* .style.fontfamily="*expression*"

*expression* = *Element*.style.fontfamily

**Anmerkungen**

Definiert den Schriftartnamen. Es können bestimmte Namen wie Arial oder generische Typen wie Serif, Sans-Serif, Cursive, Generic oder Monospace verwendet werden. Die Werte sind identisch mit den Standardattributen im HTML-Format.

*VML-Standardattribut*

**Beispiel**

Die Schriftfamilie des Texts ist Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 