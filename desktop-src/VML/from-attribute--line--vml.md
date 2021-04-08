---
title: From-Attribut (Zeile) (VML)
description: From-Attribut (Zeile) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730008"
---
# <a name="from-attribute-linevml"></a>From-Attribut (Zeile) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Anfangspunkt einer Linie. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Line](msdn-online-vml-line-element.md)

**Tagsyntax**

<v: *Element* from = " *Expression* " >

**Skript Syntax**

*Element* . from = "*Ausdruck*"

*Ausdruck* = *Element*. from

**Anmerkungen**

Definiert den Anfangspunkt der Linie im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden). Der Standardwert ist 0, 0.

*VML-Standard Attribut*

**Beispiel**

Die Zeile beginnt an einer Position, die 10 zeigt, und 10 zeigt rechts neben der oberen linken Ecke des übergeordneten Raums.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 