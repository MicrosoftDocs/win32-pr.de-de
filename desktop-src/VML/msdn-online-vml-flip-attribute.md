---
title: VML-Attribut "Kippen"
description: VML-Attribut "Kippen"
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730145"
---
# <a name="vml-flip-attribute"></a>VML-Attribut "Kippen"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Schaltet die Ausrichtung einer Form um. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "Flip: *Expression* " >

**Skript Syntax**

*Element* . Style. Flip = "*Ausdruck*"

*Ausdruck* = *Element*. Style. Flip

**Anmerkungen**

Mögliche Werte:



| Wert | BESCHREIBUNG                                           |
|-------|-------------------------------------------------------|
| x     | Kippen Sie entlang der y-Achse, und umkehren Sie die *x*-Koordinaten. |
| Y     | Kippen Sie entlang der *x*-Achse, und umkehren Sie die y-Koordinaten. |
| xy    | Kippen Sie sowohl auf die y-als auch auf die *x*-Achse.                  |
| YX    | Kippen Sie entlang der *x*-und *y*-Achse.                |



 

*VML-Standard Attribut*

**Siehe auch**

[Vgfliporientation](msdn-online-vector-markup-language-object-model-reference.md)

**Beispiel**

Die Form wird entlang der *y* -Achse durch Umkehren der *x* -Koordinaten gekippt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Beispiel](/previous-versions/bb229670(v=vs.85))für das Flip-Attribut. (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 