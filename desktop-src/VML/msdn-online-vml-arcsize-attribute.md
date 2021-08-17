---
title: VML ArcSize-Attribut
description: VML ArcSize-Attribut
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715440f56625d16ed5b4386120dbf50588ce861c1ba59772e3ec8f35a077dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755124"
---
# <a name="vml-arcsize-attribute"></a>VML ArcSize-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Rundungsmenge für ein abgerundetes Rechteck. Lese-/Schreibzugriff. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Gilt für**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Tagsyntax**

<v: *element* arcsize=" *ausdruck* ">

**Skriptsyntax**

*element* .arcSize="*expression*"

*expression* = *.arcSize-Element*

**Anmerkungen**

Definiert die abgerundeten Ecken eines abgerundeten Rechtecks als Prozentsatz der Hälfte der kleineren Dimension der Länge und Breite eines Rechtecks. 0 % verfügen über quadratische Ecken, und 100 % bilden kreisförmige Ecken. Ein Quadrat mit einem **ArcSize-Wert** von 1,0 wäre ein Kreis. Der Standardwert ist 0,2 (20 %).

*VML-Standardattribut*

**Beispiel**

Das abgerundete Rechteck wird mit engen, aber abgerundeten Ecken gezeichnet.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 