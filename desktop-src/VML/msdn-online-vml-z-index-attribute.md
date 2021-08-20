---
title: VML-Z-Index-Attribut
description: VML-Z-Index-Attribut
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07100b2ecdbda792ea3f7d5550759430539b95b86c5ef76ded2f9238785b1151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123770"
---
# <a name="vml-z-index-attribute"></a>VML-Z-Index-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt die Anzeige reihenfolge überlappender Formen. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="z-index: *expression* ">

**Skriptsyntax**

*element* .style.zindex="*expression*"

*expression* = *Element*.style.zindex

**Anmerkungen**

Das **Z-Index-Attribut** ähnelt dem STANDARDMÄßIGEN **HTML-Z-Index-Attribut** für Stile.

Mögliche Werte:



| Wert | Beschreibung                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch  | Die Reihenfolge, in der die Formen auf der HTML-Seite angezeigt werden, wird von unten nach oben verwendet.                                                                                                                         |
| order | Eine Zahl, die die Stapelreihenfolge darstellt. Eine Form mit einer höheren Zahl wird so angezeigt, als ob sie eine Form mit einer niedrigeren Zahl überschnappt (vorn). Negative Zahlen können verwendet werden. |



 

*VML-Standardattribut*

**Beispiel**

Die rote Form wird im "Front" der blauen Form angezeigt, da sie über einen höheren Z-Index verfügt.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Beispiel für das Z-Index-Attribut](/previous-versions/ms530275(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 