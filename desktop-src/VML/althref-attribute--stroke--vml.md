---
title: AltHRef-Attribut (Strich)(VML)
description: AltHRef-Attribut (Strich)(VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cbdbe82330d154675b135f7e9f35869c8f47e25715680d97df05e5511a01e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867441"
---
# <a name="althref-attribute-strokevml"></a>AltHRef-Attribut (Strich)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt einen alternativen Verweis für ein Bild an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* o:althref=" *ausdruck* ">

**Skriptsyntax**

*element* .althref="*expression*"

*expression* = *.althref-Element*

**Anmerkungen**

Unterstützt die Beibehaltung von PICT-Daten durch HTML-Roundtripping. Beim HTML-Schreibvorgang wird die alternative Darstellung (d. h. die ursprünglichen PICT-Daten, wenn die Datei vom Macintosh stammt) gespeichert. Bei HTML-Lese- wird **AltHRef** gegenüber **Src** bevorzugt.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Der Strich der Form weist ein **AltHRef** auf, das auf eine Datei mit dem Namen myimage.gif zeigt.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 