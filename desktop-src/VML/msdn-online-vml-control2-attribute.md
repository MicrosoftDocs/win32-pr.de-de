---
title: VML Control2-Attribut
description: VML Control2-Attribut
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7af3871981e26ff7eff471651de555483fd540
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101686"
---
# <a name="vml-control2-attribute"></a>VML Control2-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den zweiten Kontrollpunkt einer Bézier-Kurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[FF](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *Element* Control2 = " *Ausdruck* " >

**Skript Syntax**

*Element* . Control2 = "*Ausdruck*"

*Ausdruck* = *Element*. Control2

**Anmerkungen**

Definiert den zweiten Kontrollpunkt einer kubischen Bézier-Kurve im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden). Der Standardwert ist 20,0.

*VML-Standard Attribut*

**Beispiel**

Die Kurve wird Lächeln. Sie beginnt auf der linken Seite und endet auf der rechten Seite. Die beiden Kontrollpunkte sind auf dem Weg, um die Kurve nach unten zu ziehen, um die Darstellung eines Lächelns zu gestalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 