---
title: VML Stroke-Element
description: VML Stroke-Element
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fa3b8293c8d540af47578ac522ff1cde179d8858c4f1e16aa95a0cd6e635e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513210"
---
# <a name="vml-stroke-element"></a>VML Stroke-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert einen Strich für eine Form.

Die folgenden Attribute ändern einen Strich.



| attribute                                                          | Beschreibung                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [ALTHRef](althref-attribute--stroke--vml.md)                      | Gibt einen alternativen Verweis für einen Strich an.                |
| [Farbe](color-attribute--stroke--vml.md)                          | Definiert die Farbe eines Strichs.                                |
| [Color2](color2-attribute--stroke--vml.md)                        | Definiert eine zweite Farbe für einen Strich.                          |
| [Dashstyle](msdn-online-vml-dashstyle-attribute.md)               | Gibt das Punkt- und Bindestrichmuster für einen Strich an.              |
| [EndArrow](msdn-online-vml-endarrow-attribute.md)                 | Definiert einen Pfeilspitzenstil für das Ende eines Strichs.           |
| [EndArrowLength](msdn-online-vml-endarrowlength-attribute.md)     | Definiert eine Pfeilspitzenlänge für das Ende eines Strichs.          |
| [EndArrowWidth](msdn-online-vml-endarrowwidth-attribute.md)       | Definiert eine Pfeilspitzenbreite für das Ende eines Strichs.           |
| [Endcap](msdn-online-vml-endcap-attribute.md)                     | Definiert die Strichobergrenze für das Ende eines Strichs.                |
| [FillType](msdn-online-vml-filltype-attribute.md)                 | Definiert den Typ der Füllung, die für den Hintergrund eines Strichs verwendet wird. |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Definiert die URL zum ursprünglichen Bild für den Strich.         |
| [ID](id-attribute--stroke--vml.md)                                | Definiert einen eindeutigen Bezeichner für den Strich.                   |
| [ImageAlignShape](msdn-online-vml-imagealignshape-attribute.md)   | Bestimmt die Ausrichtung eines Strichbilds.                   |
| [ImageAspect](msdn-online-vml-imageaspect-attribute.md)           | Definiert, wie das Seitenverhältnis des Strichbilds beibehalten wird.  |
| [Imagesize](msdn-online-vml-imagesize-attribute.md)               | Definiert die Größe des Bilds für den Strich.                 |
| [JoinStyle](msdn-online-vml-joinstyle-attribute.md)               | Definiert den Joinstil einer Polylinie.                         |
| [Linestyle](msdn-online-vml-linestyle-attribute.md)               | Definiert die Linienart eines Strichs.                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | Definiert die Glättung eines Miter-Fugens.                      |
| [Ein](on-attribute--stroke--vml.md)                                | Bestimmt, ob der Strich angezeigt wird.              |
| [Deckkraft](opacity-attribute--stroke--vml.md)                      | Definiert die Transparenz eines Strichs.               |
| [Src](src-attribute--stroke--vml.md)                              | Definiert das Quellbild, das für eine Strichfüllung geladen werden soll.           |
| [StartArrow](msdn-online-vml-startarrow-attribute.md)             | Definiert die Pfeilspitze für den Anfang eines Strichs.              |
| [StartArrowLength](msdn-online-vml-startarrowlength-attribute.md) | Definiert die Pfeilspitzenlänge für den Anfang eines Strichs.       |
| [StartArrowWidth](msdn-online-vml-startarrowwidth-attribute.md)   | Definiert die Pfeilspitzenbreite für den Anfang eines Strichs.        |
| [Titel](title-attribute--stroke--vml.md)                          | Definiert den Titel eines Strichs.                                |
| [Weight](msdn-online-vml-weight-attribute.md)                     | Definiert die Stärke eines Strichs.                            |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape-Elements definiert](shape-element--vml.md) werden.

Der folgende Code zeigt, wie das **Stroke-Element** verwendet werden kann, um eine Zeile zu ändern.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**Beispiele**

-   [Einfaches Strichbeispiel](/previous-versions/bb229466(v=vs.85))
-   [Beispiel für Strichbild](/previous-versions/bb229468(v=vs.85))

 

 