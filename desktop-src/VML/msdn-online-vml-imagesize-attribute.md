---
title: VML-ImageSize-Attribut
description: VML-ImageSize-Attribut
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be63fb0adf39e2494ae2fa4d1037b96c7873a7c12524215de0d1ecfd016e116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600246"
---
# <a name="vml-imagesize-attribute"></a>VML-ImageSize-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Größe des Bilds für den Strich. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* imagesize=" *Ausdruck* ">

**Skriptsyntax**

*element* .imagesize="*expression*"

*expression* = *Element*.imagesize

**Anmerkungen**

Der Standardwert ist die Größe des Bilds.

*VML-Standardattribut*

**Beispiel**

Das Strichbild hat eine Größe von 10 by 10 Punkt.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 