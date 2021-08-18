---
title: VML-Gewichtungsattribut
description: VML-Gewichtungsattribut
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1a4dc7e33a4a1bf8421350bed9df374f7edd31a1c1a48a2b3e1549dc63084d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999090"
---
# <a name="vml-weight-attribute"></a>VML-Gewichtungsattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Stärke eines Strichs. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* weight="-Ausdruck "> 

**Skriptsyntax**

*element* .weight="*expression*"

*expression* = *Element*.weight

**Anmerkungen**

Dieses Attribut ist mit dem **StrokeWeight-Attribut** von **Shape identisch und** überschreibt es. Der Standardwert ist 1 Punkt.

*VML-Standardattribut*

**Beispiel**

Der Strich hat eine Stärke von 5 Punkten, nicht von 2 Punkten.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 