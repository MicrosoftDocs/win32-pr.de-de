---
title: VML-Attribut "MiterLimit"
description: VML-Attribut "MiterLimit"
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473429"
---
# <a name="vml-miterlimit-attribute"></a>VML-Attribut "MiterLimit"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Glätte des Haupt Trennzeichens. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* MiterLimit = " *Ausdruck* " >

**Skript Syntax**

*Element* . MiterLimit = "*Ausdruck*"

*Ausdruck* = *Element*. miterLimit

**Anmerkungen**

Der maximale Abstand zwischen dem inneren und dem äußeren Punkt eines gemeinsamen Punkts. Diese Zahl ist ein Vielfaches der Linienstärke.

Der Standardwert ist 8.

*VML-Standard Attribut*

**Beispiel**

Die Gelenke auf der Polylinie werden mit einem Grenzwert von 10 gemessen, d. h. 5 mal 2 Punkten.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 