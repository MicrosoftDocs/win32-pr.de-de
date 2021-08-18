---
title: VML-EndArrow-Attribut
description: VML-EndArrow-Attribut
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f289342c8bfb67e9a0c2ccc6e418f42bd954e9826a18f07260a2891bf4b4284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007830"
---
# <a name="vml-endarrow-attribute"></a>VML-EndArrow-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Pfeilspitze für das Ende einer Zeile. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* endarrow=" *ausdruck* ">

**Skriptsyntax**

*element* .endarrow="*expression*"

*expression* = *.endarrow-Element*

**Anmerkungen**

Mögliche Werte:

-   Keine (Standard)
-   Blockieren
-   Klassisch
-   Diamond
-   Oval
-   Öffnen

*VML-Standardattribut*

**Beispiel**

Eine Linie wird mit einer klassischen Pfeilspitze am Ende des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 