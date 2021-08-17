---
title: Size-Attribut (Fill)(VML)
description: Size-Attribut (Fill)(VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26568151961fb2186f8cf49ae25d9f2835665b8fd52a96a4d3a79e954c50ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754145"
---
# <a name="size-attribute-fillvml"></a>Size-Attribut (Fill)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Größe des Bilds für die Füllung. Lese-/Schreibzugriff. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* size="-Ausdruck "> 

**Skriptsyntax**

*element* .size="*expression**"**

*expression* = *Element*.size

**Anmerkungen**

Der Standardwert ist die Größe des ursprünglichen Bilds. Größen, die größer als die Form sind, zeigen eine vergrößerte, aber abgeschnittene Version des Bilds an.

*VML-Standardattribut*

**Beispiel**

Obwohl die ursprüngliche Größe des Bilds 50 mal 50 Punkte beträgt, wird das Bild als 10-mal-10-Bild in der Mitte der Füllung angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 