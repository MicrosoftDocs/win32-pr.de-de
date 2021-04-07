---
title: To-Attribut (Zeile) (VML)
description: To-Attribut (Zeile) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730129"
---
# <a name="to-attribute-linevml"></a>To-Attribut (Zeile) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Endpunkt einer Linie. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Line](msdn-online-vml-line-element.md)

**Tagsyntax**

<v: *Element* to = " *Expression* " >

**Skript Syntax**

*Element* . to = "*Ausdruck*"

*Ausdruck* = *Element*. to

**Anmerkungen**

Definiert den Endpunkt der Zeile im Koordinaten Bereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden). Der Standardwert ist 10, 10.

**VML-Standard Attribut**

**Beispiel**

Die Zeile endet an einer Position von 100 Punkten nach unten, und 100 zeigt rechts neben der oberen linken Ecke des übergeordneten Raums.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 