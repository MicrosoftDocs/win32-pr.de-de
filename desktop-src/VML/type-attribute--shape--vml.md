---
title: Typattribut (Shape)(VML)
description: Typattribut (Shape)(VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b20f663f8a403acca03ff8ab516a86dc91f7dd8d478eadedaa6be8b919ad48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513150"
---
# <a name="type-attribute-shapevml"></a>Typattribut (Shape)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert einen Verweis auf die ID eines [ShapeType-Elements.](msdn-online-vml-shapetype-element.md) Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

``` syntax
<v:
          element 
          type=" expression ">
```

**Skriptsyntax**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Anmerkungen**

Wenn das **Type-Attribut** auf die ID eines **ShapeType-Elements** verweist, werden die Füllungen, Pfade und Striche von **ShapeType** als Vorlagen zum Erstellen der Form verwendet. Von **ShapeType abgeleitete** Werte können durch einzelne Formwerte überschrieben werden.

Bei Verwendung in Tags muss der Zeichenfolgenwert mit einem Nummernzeichen \# () beginnen.

**VML-Standardattribut**

**Beispiel**

Eine **ShapeType-Form** wird mit dem "mytype" als ID erstellt.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



Wenn Sie dann eine Form mithilfe der **ShapeType-Werte** erstellen, enthält die Form die Attribute des ShapeType "mytype".  Das heißt, "shape01" hat eine rote Füllung mit einem blauen Strich.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



Sie können die geerbten Werte überschreiben, indem Sie beispielsweise die Farbe in Grün ändern.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Typattribut – Beispiel.](/previous-versions/bb264099(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 