---
title: VML-Punkte Attribut
description: VML-Punkte Attribut
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039085"
---
# <a name="vml-points-attribute"></a>VML-Punkte Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Satz von Punkten, die eine Polylinie bilden. Lese-/Schreibzugriff. [Ivgpoints](msdn-online-vml-ivgpoints-data-type.md) .

**Gilt für**

[Polylinie](msdn-online-vml-polyline-element.md)

**Tagsyntax**

<v: *Element* Points = " *Ausdruck* " >

**Skript Syntax**

*Element* . Points = "*Ausdruck * * *"**

*Ausdruck* = *Element*. Points

**Anmerkungen**

Definiert einen Satz von geraden Liniensegmenten, die aus einer Reihe von Punkten bestehen. Wenn das übergeordnete Element kein VML-Element ist, ist die Standard [Einheit](msdn-online-vml-units.md) ein Pixel (in, cm, mm, PT, kann jedoch auch der PC angegeben werden). Der Standardwert ist "0, 0 10, 10". Beachten Sie, dass Kommas nicht erforderlich sind, aber für eine einfachere Lesbarkeit sorgen.

*VML-Standard Attribut*

**Beispiel**

Die Polylinie beginnt am Punkt 10, 10 und endet bei 100.100 mit den Bewertungs Punkten.


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 