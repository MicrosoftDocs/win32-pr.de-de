---
title: VML Control2-Attribut
description: VML Control2-Attribut
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c0eee9ba861a73ec6d9f0fd07cca22a551c92c5add5498cd0e33522419fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999250"
---
# <a name="vml-control2-attribute"></a>VML Control2-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den zweiten Kontrollpunkt einer Bézierkurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Kurve](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *element* control2="-Ausdruck "> 

**Skriptsyntax**

*element* .control2="*expression*"

*expression* = *Element*.control2

**Anmerkungen**

Definiert den zweiten Kontrollpunkt einer kubischen Bézierkurve im Koordinatenraum des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standardeinheit ein Pixel (in, cm, mm, pt, pc kann jedoch auch angegeben werden). [](msdn-online-vml-units.md) Der Standardwert ist 20.0.

*VML-Standardattribut*

**Beispiel**

Die Kurve lächelt. Er beginnt links und endet auf der rechten Seite. Die beiden Kontrollpunkte werden entlang des Wegs entlang gezogen, um die Kurve nach unten zu ziehen, um das Aussehen eines Lächelns zu erhalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 