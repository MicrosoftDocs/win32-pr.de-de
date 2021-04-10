---
title: VML-Z-Index-Attribut
description: VML-Z-Index-Attribut
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948806"
---
# <a name="vml-z-index-attribute"></a>VML-Z-Index-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt die Anzeigereihenfolge von überlappenden Formen. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "z-Index: *Expression* " >

**Skript Syntax**

*Element* . Style. ZIndex = "*Ausdruck*"

*Ausdruck* = *Element*. Style. ZIndex

**Anmerkungen**

Das **z-Index-** Attribut ähnelt dem standardmäßigen HTML **-z-Index-** Attribut für Stile.

Mögliche Werte:



| Wert | BESCHREIBUNG                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto  | Die Reihenfolge, in der die Formen auf der HTML-Seite angezeigt werden, wird von unten nach oben verwendet.                                                                                                                         |
| order | Eine Zahl, die die Stapel Rangfolge darstellt. Eine Form mit einer höheren Zahl wird so angezeigt, als ob Sie sich überlappen (im "Vordergrund") einer Form mit einer niedrigeren Zahl. Negative Zahlen können verwendet werden. |



 

*VML-Standard Attribut*

**Beispiel**

Die rote Form wird in "Front" der blauen Form angezeigt, da Sie einen höheren z-Index aufweist.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Beispiel für den Z-Index-Attribut](/previous-versions/ms530275(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 