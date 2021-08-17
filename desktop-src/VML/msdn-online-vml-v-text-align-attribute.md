---
title: VML-V-Text-Align-Attribut
description: VML-V-Text-Align-Attribut
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bf8ec2e781b04e7ababc0b30ea3996e569e5cf9066a4bac072806fd7329eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939129"
---
# <a name="vml-v-text-align-attribute"></a>VML-V-Text-Align-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Ausrichtung von Text. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="v-text-align: *expression* ">

**Skriptsyntax**

*element* .style.v-text-align="*expression*"

*expression* = *Element*.style.v-text-align

**Anmerkungen**

Mögliche Werte:

-   **left** (Standard)
-   **Richting**
-   **Center**
-   **Rechtfertigen**
-   **Letter-Justify**
-   **Stretch-Justify**

*VML-Standardattribut*

**Beispiel**

Der Text wird so gestreckt, dass er dem Pfad passt, aber der zusätzliche Leerzeichen wird zwischen jedem Buchstaben eingefügt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 