---
title: VML-alignshape-Attribut
description: VML-alignshape-Attribut
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316299"
---
# <a name="vml-alignshape-attribute"></a>VML-alignshape-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein Bild an einer Form ausgerichtet wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* alignshape = " *Expression* " >

**Skript Syntax**

*Element* . alignshape = "*Ausdruck*"

*Ausdruck* = *Element*. alignshape

**Anmerkungen**

**True** gibt an, dass das zum Erstellen der Füllung verwendete Bild an der Form ausgerichtet wird. Wenn der Wert **false** ist, wird das Bild, das zum Erstellen der Füllung verwendet wird, an dem Fenster ausgerichtet. Der Standardwert ist **true**.

*VML-Standard Attribut*

**Beispiel**

Das aus myimage.gif erstellte Kachel Füll Bild wird am Fenster ausgerichtet, nicht an der Form. Obwohl die Form gedreht wird, ist das Bild nicht.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 