---
title: AltHRef-Attribut (Fill)(VML)
description: AltHRef-Attribut (Fill)(VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181f98ace80403668f8f67c6f8412091271fdfcf2abcb5a1320d0685853d92bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603003"
---
# <a name="althref-attribute-fillvml"></a>AltHRef-Attribut (Fill)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert einen alternativen Verweis für ein Bild. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* o:althref=" *ausdruck* ">

**Skriptsyntax**

*element* .althref="*expression*"

*expression* = *.althref-Element*

**Anmerkungen**

Unterstützt die Beibehaltung von PICT-Daten durch HTML-Roundtripping. Beim HTML-Schreibvorgang wird die alternative Darstellung (die ursprünglichen PICT-Daten, wenn die Datei vom Apple Macintosh stammt) gespeichert. Bei HTML-Lese- wird **AltHRef** gegenüber **Src** bevorzugt.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Füllung der Form weist ein **AltHRef** auf, das auf eine Datei mit dem Namen myimage.gif zeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 