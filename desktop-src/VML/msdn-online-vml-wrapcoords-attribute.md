---
title: VML-wrapcoords-Attribut
description: VML-wrapcoords-Attribut
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727961"
---
# <a name="vml-wrapcoords-attribute"></a>VML-wrapcoords-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert das Begrenzungs Polygon, das eine Form umgibt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:wrapcoords = " *Ausdruck* " >

**Anmerkungen**

Beschreibt eine durch Trennzeichen getrennte Liste von x und ykoordinaten; Das heißt, "x1, Y1, x2, Y2, X3, Y3,..." Diese wird verwendet, wenn Text eng um eine Form umschlossen ist. Der Standardwert ist **null** (eine leere Zeichenfolge), bis das **mso-Wrap-Mode-** Attribut auf ' **Tight** ' oder ' **through**' festgelegt ist.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form hat ein Begrenzungsfeld mit Text Umbruch, das 5 Einheiten überschreitet, die größer sind als der Pfad.


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 