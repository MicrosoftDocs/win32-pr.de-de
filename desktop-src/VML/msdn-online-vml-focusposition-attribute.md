---
title: VML focusposition-Attribut
description: VML focusposition-Attribut
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102318"
---
# <a name="vml-focusposition-attribute"></a>VML focusposition-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Mittelpunkt eines radialen Farbverlaufs. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* focusposition = " *Ausdruck* " >

**Skript Syntax**

*Element* . focusposition = "*Ausdruck*"

*Ausdruck* = *Element*. focusposition

**Anmerkungen**

Gibt die Mittelpunkt Positionierung für radiale Farbverläufe an. Der Vektor ist ein Bruchteil der Breite und Höhe der Form. Der erste Wert ist ein Prozentsatz der Füllung am linken Rand. der zweite Wert ist ein Prozentsatz der Füllung im oberen Bereich. Der Standardwert ist 0,0. Um eine radiale Füllung in der Mitte einer Form zu positionieren, verwenden Sie den Wert von 50%, 50%.

*VML-Standard Attribut*

**Beispiel**

Die radiale Füllung wird so zentriert, dass blau in der Mitte beginnt und nach außen strahlt und sich allmählich zu rot ändert, wenn die äußeren Ränder und Ecken erreicht werden.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 