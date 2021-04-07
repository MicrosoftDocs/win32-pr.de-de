---
title: Type-Attribut (Fill) (VML)
description: Type-Attribut (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728808"
---
# <a name="type-attribute-fillvml"></a>Type-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt den Fülltyp. Lese-/Schreibzugriff. **Vgfilltype**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Elementtyp* = " *Ausdruck* " >

**Skript Syntax**

*Element* . Type = "*Ausdruck*"

*Ausdruck* = *Element*. Type

**Anmerkungen**

Mögliche Werte:



| type           | BESCHREIBUNG                                                             |
|----------------|-------------------------------------------------------------------------|
| festem          | Das Füllmuster ist vollständig. Standard.                                     |
| Farbverlauf       | Die Füll Farben vermischen sich in einem linearen Farbverlauf von unten nach oben. |
| gradientradiale | Die Füllfarben werden in einem radialen Farbverlauf miteinander verknüpft.                    |
| tile           | Das Füllbild wird gekachelt.                                                |
| pattern        | Das Bild wird zum Erstellen eines Musters mithilfe der Füllfarben verwendet.            |
| frame          | Das Bild wird gestreckt, um die Form auszufüllen.                               |



 

**VML-Standard Attribut**

**Beispiel**

Eine rote Vordergrund-und blaue Hintergrund Füllung wird mithilfe des Musters der Bild myimage.gif erstellt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 