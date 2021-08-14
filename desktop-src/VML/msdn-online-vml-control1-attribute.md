---
title: VML Control1-Attribut
description: VML Control1-Attribut
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b4c57a936a2820e5189be78cab119b4455d20af22735a47a66c444f721723f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601933"
---
# <a name="vml-control1-attribute"></a>VML Control1-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den ersten Kontrollpunkt einer Bézierkurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Kurve](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *element* control1="-Ausdruck "> 

**Skriptsyntax**

*element* .control1="*expression*"

*expression* = *Element*.control1

**Anmerkungen**

Definiert den ersten Kontrollpunkt einer kubischen Bézierkurve im Koordinatenbereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die Standardeinheit ein Pixel (in, cm, mm, pt, pc kann jedoch auch angegeben werden). [](msdn-online-vml-units.md) Der Standardwert ist 10,10.

*VML-Standardattribut*

**Beispiel**

Die Kurve lächelt. Er beginnt links und endet auf der rechten Seite. Die beiden Kontrollpunkte werden entlang des Wegs entlang gezogen, um die Kurve nach unten zu ziehen, um das Aussehen eines Lächelns zu erhalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 