---
title: VML-ImageAlignShape-Attribut
description: VML-ImageAlignShape-Attribut
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86090936556ba8a4f022024f292293b396d953d46962423a222b172adc2a15f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600468"
---
# <a name="vml-imagealignshape-attribute"></a>VML-ImageAlignShape-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt die Ausrichtung des Strichbilds. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v:

element *imagealignshape="* ausdruck *">*

**Skriptsyntax**

element *.imagealignshape="* expression *"*

*=**Expression-Element .imagealignshape*

**Anmerkungen**

True **gibt an,** dass das Bild an der Form ausgerichtet ist, ander denn, das Bild wird am Fenster ausgerichtet. Der Standardwert ist **True**.

*VML-Standardattribut*

**Beispiel**

Das Bild wird am Fenster ausgerichtet.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 