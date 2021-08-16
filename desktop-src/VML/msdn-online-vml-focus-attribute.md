---
title: VML-Fokusattribut
description: VML-Fokusattribut
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b60eeb9ff379c8006cbb9068b6b78c8f24490ecf2fd15573b5b224a9ee1208ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057868"
---
# <a name="vml-focus-attribute"></a>VML-Fokusattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Mittelpunkt einer linearen Farbverlaufsfüllung. Lese-/Schreibzugriff. **VgFraction**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* focus="-Ausdruck "> 

**Skriptsyntax**

*element* .focus="*expression*"

*expression* = *Element*.focus

**Anmerkungen**

Definiert die zentrierte Anfangsposition der Mischung. Die Werte liegen zwischen 100 % und -100 %. Der Standardwert ist 0. Ein Wert von 100 % (oder -100 %) verschiebt den Fokus so, dass die Richtung der Mischung umgekehrt wird (in der Folge wird **Color** und **Color2** umgekehrt). Ein Wert von 50 % ändert die Mischung, sodass **Sich Color** an beiden Enden und **Color2** in der Mitte befindet. Ein Wert von -50 % ändert die Mischung, sodass **Color2** an beiden Enden und **Color** sich in der Mitte befindet.

*VML-Standardattribut*

**Beispiel**

Der Farbverlaufsfokus der Füllung wird so verschoben, dass rot (**Farbe**) ein Band in der Mitte der Form ist und dass der obere und untere Rand blau ist (**Color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 