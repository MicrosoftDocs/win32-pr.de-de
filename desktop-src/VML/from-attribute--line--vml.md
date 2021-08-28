---
title: From-Attribut (Zeile)(VML)
description: From-Attribut (Zeile)(VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a8bf41462f698397b193835d08655f8d6acefb2df77b17e035ec170c3c4781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099310"
---
# <a name="from-attribute-linevml"></a>From-Attribut (Zeile)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Anfangspunkt einer Zeile. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Linie](msdn-online-vml-line-element.md)

**Tagsyntax**

<v: *element* from="-Ausdruck "> 

**Skriptsyntax**

*element* .from="*expression*"

*expression* = *Element*.from

**Anmerkungen**

Definiert den Anfangspunkt der Linie im Koordinatenbereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standardeinheit ein Pixel (in, cm, mm, pt, pc kann jedoch auch angegeben werden). [](msdn-online-vml-units.md) Der Standardwert ist 0,0.

*VML-Standardattribut*

**Beispiel**

Die Linie beginnt an einer Position, die 10 Punkte nach unten und 10 Punkte rechts von der oberen linken Ecke des übergeordneten Leerzeichens zeigt.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 