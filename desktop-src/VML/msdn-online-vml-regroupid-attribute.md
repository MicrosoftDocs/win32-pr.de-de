---
title: VML ReGroupID-Attribut
description: VML ReGroupID-Attribut
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c304bb0ecbe19c62e6fa5a204749b61fad4a700fe4222b6e1ef993384d53abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597643"
---
# <a name="vml-regroupid-attribute"></a>VML ReGroupID-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine vorherige Gruppe für eine Form. Lese-/Schreibzugriff. **VgInteger**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:regroupid=" *Ausdruck* ">

**Anmerkungen**

Eine ID-Nummer wird verwendet, um Gruppen von Formen zu identifizieren, die nicht mehr gruppiert sind. Ermöglicht das programmgesteuerte Neugruppieren von Formen.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form war Teil einer Gruppe, die durch den Gruppen-ID-040754.


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 