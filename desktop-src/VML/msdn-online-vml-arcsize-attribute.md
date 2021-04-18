---
title: VML-arcsize-Attribut
description: VML-arcsize-Attribut
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337658"
---
# <a name="vml-arcsize-attribute"></a>VML-arcsize-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Menge der roundness für ein abgerundetes Rechteck. Lese-/Schreibzugriff. [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md) .

**Gilt für**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Tagsyntax**

<v: *Element* arcsize = " *Ausdruck* " >

**Skript Syntax**

*Element* . arcsize = "*Ausdruck*"

*Ausdruck* = *Element*. arcsize

**Anmerkungen**

Definiert die abgerundeten Ecken eines gerundeten Rechtecks als Prozentsatz der Hälfte der kleineren Dimension der Länge und Breite eines Rechtecks. 0% hätte quadratische Ecken, und 100% würde kreisförmige Ecken bilden. Ein Quadrat mit einem **arcsize** -Wert von 1,0 wäre ein Kreis. Der Standardwert ist 0,2 (20%).

*VML-Standard Attribut*

**Beispiel**

Das abgerundete Rechteck wird mit engen, aber abgerundeten Ecken gezeichnet.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 