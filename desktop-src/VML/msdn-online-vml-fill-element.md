---
title: VML Fill-Element
description: VML Fill-Element
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b314e2d735b8b7800321eacffbd63c686b17e870fd136e086c52231ad801456e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346624"
---
# <a name="vml-fill-element"></a>VML Fill-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Füllung für eine Form.

Die folgenden Attribute ändern eine Füllung.



| attribute                                                          | Beschreibung                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [AlignShape](msdn-online-vml-alignshape-attribute.md)             | Bestimmt, ob ein Bild an einer Form ausgerichtet wird.   |
| [ALTHRef](althref-attribute--fill--vml.md)                        | Gibt einen alternativen Verweis für ein Bild an.         |
| [Winkel](angle-attribute--fill--vml.md)                            | Definiert den Winkel einer Farbverlaufsfüllung.                  |
| [Aspekt](msdn-online-vml-aspect-attribute.md)                     | Gibt an, wie der Füllbildaspekt beibehalten wird. |
| [Farbe](color-attribute--fill--vml.md)                            | Definiert die Farbe einer Füllung.                           |
| [Color2](color2-attribute--fill--vml.md)                          | Definiert die zweite Farbe für eine Füllung.                   |
| [Farben](msdn-online-vml-colors-attribute.md)                     | Definiert mehrere Farben für eine Farbverlaufsfüllung.           |
| [DetectMouseClick](detectmouseclick-attribute--fill--vml.md)      | Bestimmt, ob ein Mausklick erkannt wird.          |
| [Fokus](msdn-online-vml-focus-attribute.md)                       | Definiert den Mittelpunkt einer linearen Farbverlaufsfüllung.          |
| [FocusPosition](msdn-online-vml-focusposition-attribute.md)       | Definiert den Mittelpunkt einer radialen Farbverlaufsfüllung.          |
| [FocusSize](msdn-online-vml-focussize-attribute.md)               | Definiert die Fokusgröße für eine radiale Füllung.              |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Definiert eine URL zur ursprünglichen Bilddatei.              |
| [ID](id-attribute--fill--vml.md)                                  | Definiert einen eindeutigen Bezeichner für die Füllung.              |
| [Methode](msdn-online-vml-method-attribute.md)                     | Definiert die Methode, die zum Generieren einer Farbverlaufsfüllung verwendet wird.   |
| [Ein](on-attribute--fill--vml.md)                                  | Bestimmt, ob die Füllung angezeigt wird.          |
| [Deckkraft](opacity-attribute--fill--vml.md)                        | Definiert die Transparenz einer Füllung.                    |
| [Deckkraft2](msdn-online-vml-opacity2-attribute.md)                 | Definiert die Transparenz der zweiten Füllfarbe.     |
| [Ursprung](origin-attribute--fill--vml.md)                          | Definiert die Mitte eines Bilds.                        |
| [Position](position-attribute--fill--vml.md)                      | Definiert die Position eines Bilds.                      |
| [Größe](size-attribute--fill--vml.md)                              | Definiert die Größe eines Bilds.                          |
| [Src](src-attribute--fill--vml.md)                                | Definiert das Bild, das für eine Füllung geladen werden soll.                  |
| [Titel](title-attribute--fill--vml.md)                            | Definiert den Titel einer Füllung.                           |
| [Typ](type-attribute--fill--vml.md)                              | Definiert den Typ der Füllung.                              |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape-Elements definiert](shape-element--vml.md) werden.

Der folgende Code zeigt eine einfache Farbverlaufsfüllung für eine Form.


```HTML
   <v:shape
   style="position:relative;top:1;left:1;width:400;height:400"
   path = "m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type=gradient color="blue" color2="yellow"/>
   </v:shape>
```



**Beispiele**

-   [Einfache Farbverlaufsfüllung](/previous-versions/bb229620(v=vs.85))
-   [Beispiel für dynamische Füllung](/previous-versions/bb229621(v=vs.85))

 

 