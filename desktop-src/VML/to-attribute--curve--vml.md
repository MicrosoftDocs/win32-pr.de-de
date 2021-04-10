---
title: To-Attribut (Kurve) (VML)
description: To-Attribut (Kurve) (VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858463"
---
# <a name="to-attribute-curvevml"></a>To-Attribut (Kurve) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Endpunkt einer Kurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[FF](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *Element* to = " *Expression* " >

**Skript Syntax**

*Element* . to = "*Ausdruck*"

*Ausdruck* = *Element*. to

**Anmerkungen**

Definiert den Endpunkt einer kubischen Bézier-Kurve im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden). Der Standardwert ist 30, 20.

**VML-Standard Attribut**

**Beispiel**

Die Kurve wird Lächeln. Sie beginnt auf der linken Seite und endet auf der rechten Seite. Die beiden Kontrollpunkte sind auf dem Weg, um die Kurve nach unten zu ziehen, um die Darstellung eines Lächelns zu gestalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 