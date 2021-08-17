---
title: VML-Font-Size-Attribut
description: VML-Font-Size-Attribut
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401d66668b0a86b92e453ac2e4a8a9adb96411131cc90f7bf14bd22be67e6775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346577"
---
# <a name="vml-font-size-attribute"></a>VML-Font-Size-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Schriftgrad. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="font-size: *expression* ">

**Skriptsyntax**

*element* .style.fontsize="*expression*"

*expression* = *.style.fontsize-Element*

**Anmerkungen**

Der Schriftgrad ist in Punkten definiert. Die Werte sind identisch mit den Html-Standardformatattributen.

*VML-Standardattribut*

**Beispiel**

Der Schriftgrad beträgt 36 Punkte.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 