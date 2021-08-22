---
title: VML-Attribut "StartArrowLength"
description: VML-Attribut "StartArrowLength"
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25446737118c546727d769d54d98e4503faaadd063102fa98a417ebea13c976d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395830"
---
# <a name="vml-startarrowlength-attribute"></a>VML-Attribut "StartArrowLength"

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Pfeilspitzenlänge für den Anfang einer Linie. Lese-/Schreibzugriff. **VgArrowheadLength**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* startwlwlength="-Ausdruck "> 

**Skriptsyntax**

*element* .startwlength="*expression*"

*expression* = *Element*.startwlwlength

**Anmerkungen**

Mögliche Werte:

-   Short
-   Mittel (Standard)
-   Long

VML-Standardattribut

**Beispiel**

Eine Linie wird mit einer kurzen klassischen Pfeilspitze am Anfang des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 