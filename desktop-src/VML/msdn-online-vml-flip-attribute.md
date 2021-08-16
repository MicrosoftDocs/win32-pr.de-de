---
title: VML Flip-Attribut
description: VML Flip-Attribut
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5293bdff5ab888b13fdc095038e74fdbcf725bbfb1948a04018fbf5a22c5677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346634"
---
# <a name="vml-flip-attribute"></a>VML Flip-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Schaltet die Ausrichtung einer Form um. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="flip: *ausdruck* ">

**Skriptsyntax**

*element* .style.flip="*expression*"

*expression* = *Element*.style.flip

**Anmerkungen**

Mögliche Werte:



| Wert | BESCHREIBUNG                                           |
|-------|-------------------------------------------------------|
| x     | Blättern Sie entlang der y-Achse, und drehen Sie die *x-Koordinaten* zurück. |
| y     | Drehen Sie die *x-Achse* entlang, und drehen Sie die y-Koordinaten zurück. |
| xy    | Blättern Sie auf der y- und x-Achse.                  |
| Yx    | Drehen Sie die *x-* und *y-Achse* entlang.                |



 

*VML-Standardattribut*

**Siehe auch**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Beispiel**

Die Form wird entlang der *y-Achse* gekippt, indem die *x-Koordinaten* umgekehrt werden.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Flip-Attribut – Beispiel.](/previous-versions/bb229670(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 