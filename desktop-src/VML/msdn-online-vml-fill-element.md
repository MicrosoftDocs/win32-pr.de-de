---
title: VML Fill-Element
description: VML Fill-Element
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc7205baa9db0eaa7d84d4022057f81804ea790
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949093"
---
# <a name="vml-fill-element"></a>VML Fill-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine Füllung für eine Form.

Die folgenden Attribute ändern eine Füllung.



| Attribut                                                          | BESCHREIBUNG                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [Alignshape](msdn-online-vml-alignshape-attribute.md)             | Bestimmt, ob ein Bild an einer Form ausgerichtet wird.   |
| [Althref](althref-attribute--fill--vml.md)                        | Gibt einen alternativen Verweis für ein Bild an.         |
| [Ultra](angle-attribute--fill--vml.md)                            | Definiert den Winkel einer Farbverlaufsfüllung.                  |
| [Aspekt](msdn-online-vml-aspect-attribute.md)                     | Gibt an, wie der Aspekt des Füll Bilds beibehalten wird. |
| [Farbe](color-attribute--fill--vml.md)                            | Definiert die Farbe einer Füllung.                           |
| [Color2](color2-attribute--fill--vml.md)                          | Definiert die zweite Farbe für eine Füllung.                   |
| [Farben](msdn-online-vml-colors-attribute.md)                     | Definiert mehrere Farben für eine Farbverlaufsfüllung.           |
| [Detectmoukliklicke](detectmouseclick-attribute--fill--vml.md)      | Bestimmt, ob ein Mausklick erkannt wird.          |
| [Fokus](msdn-online-vml-focus-attribute.md)                       | Definiert den Mittelpunkt einer linearen Farbverlaufsfüllung.          |
| [Focusposition](msdn-online-vml-focusposition-attribute.md)       | Definiert den Mittelpunkt einer radialen Farbverlaufsfüllung.          |
| [Focussize](msdn-online-vml-focussize-attribute.md)               | Definiert die Fokus Größe für eine radiale Füllung.              |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Definiert eine URL zur ursprünglichen Bilddatei.              |
| [ID](id-attribute--fill--vml.md)                                  | Definiert einen eindeutigen Bezeichner für die Füllung.              |
| [Methode](msdn-online-vml-method-attribute.md)                     | Definiert die Methode, die zum Generieren einer Farbverlaufsfüllung verwendet wird.   |
| [Ein](on-attribute--fill--vml.md)                                  | Bestimmt, ob die Füllung angezeigt wird.          |
| [Deckkraft](opacity-attribute--fill--vml.md)                        | Definiert die Transparenz einer Füllung.                    |
| [Opacity2](msdn-online-vml-opacity2-attribute.md)                 | Definiert die Transparenz der zweiten Füllfarbe.     |
| [Ursprung](origin-attribute--fill--vml.md)                          | Definiert den Mittelpunkt eines Bilds.                        |
| [Position](position-attribute--fill--vml.md)                      | Definiert die Position eines Bilds.                      |
| [Größe](size-attribute--fill--vml.md)                              | Definiert die Größe eines Bilds.                          |
| [Src](src-attribute--fill--vml.md)                                | Definiert das Bild, das für eine Füllung geladen werden soll.                  |
| [Titel](title-attribute--fill--vml.md)                            | Definiert den Titel einer Füllung.                           |
| [Type](type-attribute--fill--vml.md)                              | Definiert den Fülltyp.                              |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

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
-   [Beispiel für dynamisches ausfüllen](/previous-versions/bb229621(v=vs.85))

 

 