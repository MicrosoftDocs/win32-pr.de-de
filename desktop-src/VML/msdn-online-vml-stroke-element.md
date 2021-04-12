---
title: VML Stroke-Element
description: VML Stroke-Element
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62048227fca074276b825ceedb793eaa9a5d84dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473389"
---
# <a name="vml-stroke-element"></a>VML Stroke-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Strich für eine Form.

Die folgenden Attribute ändern einen Strich.



| Attribut                                                          | BESCHREIBUNG                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [Althref](althref-attribute--stroke--vml.md)                      | Gibt einen alternativen Verweis für einen Strich an.                |
| [Farbe](color-attribute--stroke--vml.md)                          | Definiert die Farbe eines Strichs.                                |
| [Color2](color2-attribute--stroke--vml.md)                        | Definiert eine zweite Farbe für einen Strich.                          |
| [DashStyle](msdn-online-vml-dashstyle-attribute.md)               | Gibt den Punkt und das Bindestrich Muster für einen Strich an.              |
| [Umdarrow](msdn-online-vml-endarrow-attribute.md)                 | Definiert einen Pfeilspitzen Stil für das Ende eines Strichs.           |
| ["Tdarrowlength"](msdn-online-vml-endarrowlength-attribute.md)     | Definiert eine Pfeilspitzen Länge für das Ende eines Strichs.          |
| ["-Rowwidth"](msdn-online-vml-endarrowwidth-attribute.md)       | Definiert eine Pfeilspitzen Breite für das Ende eines Strichs.           |
| [EndCap](msdn-online-vml-endcap-attribute.md)                     | Definiert den Stil für das Ende eines Strichs.                |
| [FillType](msdn-online-vml-filltype-attribute.md)                 | Definiert den Fülltyp, der für den Hintergrund eines Strichs verwendet wird. |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Definiert die URL zum ursprünglichen Bild für den Strich.         |
| [ID](id-attribute--stroke--vml.md)                                | Definiert einen eindeutigen Bezeichner für den Strich.                   |
| [Imagealignshape](msdn-online-vml-imagealignshape-attribute.md)   | Bestimmt die Ausrichtung eines Strich Bilds.                   |
| [Imageaspekt](msdn-online-vml-imageaspect-attribute.md)           | Definiert, wie das Seitenverhältnis des Strich Bilds beibehalten wird.  |
| [ImageSize](msdn-online-vml-imagesize-attribute.md)               | Definiert die Größe des Bilds für den Strich.                 |
| [JOINSTYLE](msdn-online-vml-joinstyle-attribute.md)               | Definiert die joinart einer Polylinie.                         |
| [LineStyle](msdn-online-vml-linestyle-attribute.md)               | Definiert die Linienart eines Strichs.                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | Definiert die Glätte eines Gehrungs-Joint.                      |
| [Ein](on-attribute--stroke--vml.md)                                | Bestimmt, ob der Strich angezeigt wird.              |
| [Deckkraft](opacity-attribute--stroke--vml.md)                      | Definiert den Umfang der Transparenz eines Strichs.               |
| [Src](src-attribute--stroke--vml.md)                              | Definiert das Quell Bild, das für einen Strich Füllvorgang geladen werden soll.           |
| [Startarrow](msdn-online-vml-startarrow-attribute.md)             | Definiert die Pfeilspitze für den Anfang eines Strichs.              |
| [Startarrowlength](msdn-online-vml-startarrowlength-attribute.md) | Definiert die Pfeilspitzen Länge für den Anfang eines Strichs.       |
| [Startarrowwidth](msdn-online-vml-startarrowwidth-attribute.md)   | Definiert die Pfeilspitzen Breite für den Anfang eines Strichs.        |
| [Titel](title-attribute--stroke--vml.md)                          | Definiert den Titel eines Strichs.                                |
| [Weight](msdn-online-vml-weight-attribute.md)                     | Definiert die Stärke eines Strichs.                            |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Der folgende Code zeigt, wie das **Stroke** -Element verwendet werden kann, um eine Zeile zu ändern.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**Beispiele**

-   [Einfaches Beispiel für einen Strich](/previous-versions/bb229466(v=vs.85))
-   [Beispiel für ein Strich Bild](/previous-versions/bb229468(v=vs.85))

 

 