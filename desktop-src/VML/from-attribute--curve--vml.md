---
title: From-Attribut (Kurve) (VML)
description: From-Attribut (Kurve) (VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d5f78dee46192efed48172a7d1f4d9cc77582f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390925"
---
# <a name="from-attribute-curvevml"></a>From-Attribut (Kurve) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Anfangspunkt einer Kurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[FF](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *Element* from = " *Expression* " >

**Skript Syntax**

*Element* . from = "*Ausdruck*"

*Ausdruck* = *Element*. from

**Anmerkungen**

Definiert den Anfangspunkt einer kubischen Bézier-Kurve im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden). Der Standardwert ist 0, 0.

*VML-Standard Attribut*

**Beispiel**

Die Kurve wird Lächeln. Sie beginnt auf der linken Seite und endet auf der rechten Seite. Die beiden Kontrollpunkte sind auf dem Weg, um die Kurve nach unten zu ziehen, um die Darstellung eines Lächelns zu gestalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 