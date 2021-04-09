---
title: Position-Attribut (Fill) (VML)
description: Position-Attribut (Fill) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102270"
---
# <a name="position-attribute-fillvml"></a>Position-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Position des Füllbilds. Lese-/Schreibzugriff. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Position = " *Ausdruck* " >

**Skript Syntax**

*Element* . Position = "*Ausdruck*"

*Ausdruck* = *Element*. Position

**Anmerkungen**

Gibt einen Punkt in der Form an, um den Ursprung des Bilds zu positionieren. Der Standardwert ist die Mitte des Container Rechtecks. Der Vektor ist ein Bruchteil der Breite und Höhe des Bilds.

*VML-Standard Attribut*

**Beispiel**

Das Bild der Füllung wird direkt auf einen Punkt 50% der Breite der Form verschoben.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 