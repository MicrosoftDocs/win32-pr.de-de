---
title: Type-Attribut (Form) (VML)
description: Type-Attribut (Form) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039148"
---
# <a name="type-attribute-shapevml"></a>Type-Attribut (Form) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Verweis auf die ID eines [ShapeType](msdn-online-vml-shapetype-element.md) -Elements. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

``` syntax
<v:
          element 
          type=" expression ">
```

**Skript Syntax**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Anmerkungen**

Wenn das **Type** -Attribut auf die ID eines **ShapeType** -Elements verweist, werden die Füllungen, Pfade und Striche des **ShapeType** als Vorlagen verwendet, um die Form zu erstellen. Werte, die von **ShapeType** abgeleitet werden, können von einzelnen Form Werten überschrieben werden.

Bei Verwendung in Tags muss der Zeichen folgen Wert mit einem Nummern Zeichen ( \# ) beginnen.

**VML-Standard Attribut**

**Beispiel**

Eine **ShapeType** -Form wird mit dem "MyType" als ID erstellt.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



Wenn Sie dann eine Form mithilfe der **ShapeType** -Werte erstellen, weist die Form die Attribute des **ShapeType**"MyType" auf. Das heißt, "shape01" hat eine rote Füllung mit einem blauen Strich.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



Sie können die geerbten Werte überschreiben, indem Sie z. b. die Farbe in grün ändern.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Beispiel für Typattribut](/previous-versions/bb264099(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 