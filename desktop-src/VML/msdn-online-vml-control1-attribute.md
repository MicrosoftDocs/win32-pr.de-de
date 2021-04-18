---
title: VML Control1-Attribut
description: VML Control1-Attribut
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339274"
---
# <a name="vml-control1-attribute"></a>VML Control1-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den ersten Kontrollpunkt einer Bézier-Kurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[FF](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *Element* Control1 = " *Ausdruck* " >

**Skript Syntax**

*Element* . Control1 = "*Ausdruck*"

*Ausdruck* = *Element*. Control1

**Anmerkungen**

Definiert den ersten Kontrollpunkt einer kubischen Bézier-Kurve im Koordinatenraum des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden). Der Standardwert ist 10, 10.

*VML-Standard Attribut*

**Beispiel**

Die Kurve wird Lächeln. Sie beginnt auf der linken Seite und endet auf der rechten Seite. Die beiden Kontrollpunkte sind auf dem Weg, um die Kurve nach unten zu ziehen, um die Darstellung eines Lächelns zu gestalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 