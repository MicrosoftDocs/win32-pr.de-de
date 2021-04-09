---
title: VML VMLFrame-Element
description: VML VMLFrame-Element
ms.assetid: a1582223-d6e2-42d1-95bb-97f6f1d453d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f53371afb0c2790ff6dd666f0121b30b586c51b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101747"
---
# <a name="vml-vmlframe-element"></a>VML VMLFrame-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Frame für eine externe Form.

Die folgenden Attribute ändern einen Frame.



| Attribut                                     | BESCHREIBUNG                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------|
| [Techno](msdn-online-vml-clip-attribute.md)    | Bestimmt, ob das Bild abgeschnitten wird.                         |
| [ID](id-attribute--vmlframe--vml.md)         | Definiert einen eindeutigen Bezeichner für den Frame.                            |
| [Ursprung](origin-attribute--vmlframe--vml.md) | Gibt den Ursprung des Frames an.                                    |
| [Größe](size-attribute--vmlframe.md)          | Gibt die Größe des Frames an.                                      |
| [Src](src-attribute--vmlframe--vml.md)       | Gibt die Quelle der Daten an, die im Frame angezeigt werden. |
| [Stil](msdn-online-vml-style-attribute.md)  | Definiert die normalen CSS-Stile, die verwendet werden können, um den Frame zu positionieren. |



 

**Anmerkungen**

Die Quelldaten, die im Frame angezeigt werden sollen, können sich auf derselben Webseite befinden oder Teil einer anderen Seite sein. Mithilfe der Skripterstellung kann die Quelle dynamisch geändert werden, und die Anzeigeeigenschaften können geändert werden.

Objekte innerhalb des **vmlframe** sind "Zoom skaliert". Das heißt, Sie skalieren wie Metafiles, wobei Zeilen Gewichtungen, Schatten Offsets und Textbereiche proportional skaliert werden. Dies unterscheidet sich von einer Gruppe, in der Objektgröße und-Position proportional skaliert werden, aber Zeile, Schatten usw. nicht.

Im folgenden finden Sie den minimalen Code, der zum Laden eines Bilds in einen Frame erforderlich ist.


```HTML
   <v:vmlframe
     style="top:1;left:1;width:50;height:50">
     src="external.vml#rect01"/>
   </v:vmlframe>
```



Wenn die Datei extern ist, muss Sie eine XML-Datei sein. Der folgende Code ist der minimale Code, der erforderlich ist, um eine externe Quelldatei anzugeben, die eine identifizierbare Form enthalten muss. Dieses Beispiel enthält eine Bildform, in der eine Bitmap angezeigt wird.


```HTML
   <xml xmlns:v = "urn:schemas-microsoft-com:vml">
   <v:image id="rect01"
     style="height:100;width:100;top:50;left:50">
     src="kids.jpg">
   </v:rect>
   </xml>
```



> [!Note]  
> In vorab Versionen von VML wurde dieses Element als **vmlcanvas** bezeichnet.

 

**Beispiele**

-   [Einfaches vmlframe-Beispiel](/previous-versions/bb263920(v=vs.85))
-   [Dynamisches vmlframe-Beispiel](/previous-versions/bb263902(v=vs.85))

 

 