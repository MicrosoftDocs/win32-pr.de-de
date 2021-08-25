---
title: VML Text-Decoration-Attribut
description: VML Text-Decoration-Attribut
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474d76b9e37cb363a8b2a28b84c30be77f857159767cc4db221fd7a684b4951e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796030"
---
# <a name="vml-text-decoration-attribute"></a>VML Text-Decoration-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Stil der Textdekoration. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="text-decoration: *expression* ">

**Skriptsyntax**

*element* .style.textdecoration="*expression*"

*expression* = *Element*.style.textdecoration

**Anmerkungen**

Mögliche Werte:

-   none (Standard)
-   Unterstrichen
-   Überstrich
-   Line-Through
-   blink

*VML-Standardattribut*

**Beispiel**

Der Text wird unterstrichen.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 