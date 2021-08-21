---
title: VML-V-Textabstandsattribut
description: VML-V-Textabstandsattribut
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0b699e70cd235bf7d0f7530f75a8fc5eaef52974180cc8d36a10a69c9197f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057678"
---
# <a name="vml-v-text-spacing-attribute"></a>VML-V-Textabstandsattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Abstand für Text. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="v-text-spacing: *expression* ">

**Skriptsyntax**

*element* .style.v-text-spacing="*expression*"

*expression* = *Element*.style.v-text-spacing

**Anmerkungen**

Der Standardwert ist 100. Weitere Informationen zum Textabstand finden Sie unter [V-Text-Spacing-Mode-Attribut.](msdn-online-vml-v-text-spacing-mode-attribute.md)

*VML-Standardattribut*

**Beispiel**

Die Buchstabenpashierung zwischen den einzelnen Buchstaben wird um 200 Einheiten verstärkt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 