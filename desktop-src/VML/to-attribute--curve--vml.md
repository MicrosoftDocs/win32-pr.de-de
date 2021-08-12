---
title: To-Attribut (Curve)(VML)
description: To-Attribut (Curve)(VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1d2a4c7fd91652ca59707ff00b67a8215d754134bc150402d72e833f249f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596241"
---
# <a name="to-attribute-curvevml"></a>To-Attribut (Curve)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Endpunkt einer Kurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Kurve](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *element* to="-Ausdruck "> 

**Skriptsyntax**

*element* .to="*expression*"

*expression* = *Element*.to

**Anmerkungen**

Definiert den Endpunkt einer kubischen Bézierkurve im Koordinatenraum des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standardeinheit ein Pixel (in, cm, mm, pt, pc kann jedoch auch angegeben werden). [](msdn-online-vml-units.md) Der Standardwert ist 30,20.

**VML-Standardattribut**

**Beispiel**

Die Kurve lächelt. Er beginnt links und endet auf der rechten Seite. Die beiden Kontrollpunkte werden entlang des Wegs entlang gezogen, um die Kurve nach unten zu ziehen, um das Aussehen eines Lächelns zu erhalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 