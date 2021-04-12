---
title: VML FillType-Attribut
description: VML FillType-Attribut
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949092"
---
# <a name="vml-filltype-attribute"></a>VML FillType-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Fülltyp, der für den Hintergrund eines Strichs verwendet wird. Lese-/Schreibzugriff. **Vgfilltype**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* FillType = " *Expression* " >

**Skript Syntax**

*Element* . FillType = "*Ausdruck*"

*Ausdruck* = *Element*. FillType

**Anmerkungen**

Mögliche Werte:



| DashStyle | BESCHREIBUNG                                    |
|-----------|------------------------------------------------|
| Basis     | Das Füllmuster ist vollständig. Standardwert.      |
| Tile      | Das Füllbild wird gekachelt.                       |
| Muster   | Das Füllbild wird gestreckt, um ein Muster zu bilden. |
| Frame     | Das Füllbild wird zu einem Rahmen für die Form. |



 

*VML-Standard Attribut*

**Beispiel**

Der Strich der Form hat eine Kachel, die aus dem cylinder.gif Bild erstellt wurde.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 