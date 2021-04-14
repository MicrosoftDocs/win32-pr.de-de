---
title: Origin-Attribut (Fill) (VML)
description: Origin-Attribut (Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390969"
---
# <a name="origin-attribute-fillvml"></a>Origin-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Mittelpunkt eines Füllbilds. Lese-/Schreibzugriff. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Origin = " *Expression* " >

**Skript Syntax**

*Element* . Origin = "*Ausdruck*"

*Ausdruck* = *Element*. Origin

**Anmerkungen**

Gibt einen Punkt relativ zur oberen linken Ecke des Bilds an. Dieser Punkt wird als der Ursprung des Bilds behandelt. Der Standardwert ist der Mittelpunkt des Bilds. Der Vektor ist ein Bruchteil der Breite und Höhe des Bilds.

*VML-Standard Attribut*

**Beispiel**

Das Bild der Füllung wird nach Links zu einem Punkt 50% der Breite der Form verschoben.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 