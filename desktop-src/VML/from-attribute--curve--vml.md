---
title: From-Attribut (Curve)(VML)
description: From-Attribut (Curve)(VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df431e9239f185ce83771f7822fe98e5bf491bd84a1deb7b869df7d3d2f235e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905497"
---
# <a name="from-attribute-curvevml"></a>From-Attribut (Curve)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Anfangspunkt einer Kurve. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Kurve](msdn-online-vml-curve-element.md)

**Tagsyntax**

<v: *element* from=" *ausdruck* ">

**Skriptsyntax**

*element* .from="*expression*"

*expression* = *Element*.from

**Anmerkungen**

Definiert den Anfangspunkt einer kubischen Bézierkurve im Koordinatenbereich des übergeordneten Elements. Wenn das übergeordnete Element kein VML-Element ist, ist die [Standardeinheit](msdn-online-vml-units.md) ein Pixel (aber in, cm, mm, pt, pc kann auch angegeben werden). Der Standardwert ist 0,0.

*VML-Standardattribut*

**Beispiel**

Die Kurve ist lächelnd. Er beginnt links und endet auf der rechten Seite. Die beiden Kontrollpunkte werden entlang des Wegs vererbt, um die Kurve nach unten zu ziehen, um ein Lächeln zu erhalten.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 