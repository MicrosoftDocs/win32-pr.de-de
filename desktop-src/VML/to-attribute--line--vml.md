---
title: To-Attribut (Zeile)(VML)
description: To-Attribut (Zeile)(VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d1e47261daf76103717476a84eea3bed99ddb0b514192df8a74cd0b69572a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654450"
---
# <a name="to-attribute-linevml"></a>To-Attribut (Zeile)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Endpunkt einer Zeile. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Linie](msdn-online-vml-line-element.md)

**Tagsyntax**

<v: *element* to="-Ausdruck "> 

**Skriptsyntax**

*element* .to="-Ausdruck "

*expression* = *Element*.to

**Anmerkungen**

Definiert den Endpunkt der Linie im Koordinatenbereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standardeinheit ein Pixel (in, cm, mm, pt, pc kann jedoch auch angegeben werden). [](msdn-online-vml-units.md) Der Standardwert ist 10,10.

**VML-Standardattribut**

**Beispiel**

Die Linie endet an einer Position, die 100 Punkte nach unten und 100 Punkte rechts von der oberen linken Ecke des übergeordneten Raums ist.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 