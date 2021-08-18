---
title: VML-Font-Style-Attribut
description: VML-Font-Style-Attribut
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4571f9805b3a12f1c3c7b340780d0f3d9f6ce8644c2ec501e8c93aa58d378de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057858"
---
# <a name="vml-font-style-attribute"></a>VML-Font-Style-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Umfang der Sung für eine Schriftart. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="font-style: *expression* ">

**Skriptsyntax**

*element* .style.fontstyle="*expression*"

*expression* = *Element*.style.fontstyle

**Anmerkungen**

Die Werte sind:

-   normal (Standard)
-   Oblique
-   kursiv

Die meisten Browser rendern obkonszön als italisch. Die Werte sind identisch mit den Html-Standardformatattributen.

*VML-Standardattribut*

**Beispiel**

Die Schriftart ist italisch (schräg).


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 