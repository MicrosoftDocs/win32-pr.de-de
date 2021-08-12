---
title: VML TextBox-Element
description: VML TextBox-Element
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b6ef160e975f00dd859e0f6db6f2821054a34815b3aef1ea19f520ad3d01a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597509"
---
# <a name="vml-textbox-element"></a>VML TextBox-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert ein Textfeld für eine Form.

Die folgenden Attribute ändern ein Textfeld.



| attribute                                                                    | BESCHREIBUNG                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Richtung](msdn-online-vml-direction-attribute.md)                         | Definiert die Richtung des Texts.                         |
| [ID](id-attribute--textbox--vml.md)                                         | Definiert einen eindeutigen Bezeichner für das Textfeld.               |
| [Inset](msdn-online-vml-inset-attribute.md)                                 | Gibt innere Randwerte für Textfeldtext an.            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | Definiert, wie eine Anwendung benutzerdefinierte Einsetwerte zulässt. |
| [Layout-Flow](msdn-online-vml-layout-flow-attribute.md)                     | Bestimmt den Fluss des Texts im Textfeld.            |
| [MSO-Direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Definiert alternative Anweisungen für Text in Textboxen.        |
| [MSO-Fit-Shape-to-Text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Bestimmt, ob eine Form an Text angepasst wird.       |
| [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Bestimmt, ob Text gestreckt wird, um an eine Form anzupassen.       |
| [MSO-Layout-Flow-ALT](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Definiert den alternativen Layoutflow für Text in einem Textfeld.   |
| [MSO-Next-Textbox](msdn-online-vml-mso-next-textbox-attribute.md)           | Gibt das nächste Textfeld in einer Reihe an.                    |
| [MSO-Rotate](msdn-online-vml-mso-rotate-attribute.md)                       | Bestimmt, ob Text mit einer gedrehten Form gedreht wird.      |
| [MSO-Textskala](msdn-online-vml-mso-text-scale-attribute.md)               | Definiert den Skalierungsfaktor für die Anpassung von Text an Formen.     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | Bestimmt, ob Text mit einem einzigen Klick ausgewählt werden kann. |
| [V-Textanker](msdn-online-vml-v-text-anchor-attribute.md)                 | Definiert die vertikale Ankerung von Text in einem Textfeld.       |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape-Elements](shape-element--vml.md) definiert werden.

Im Folgenden wird der mindest erforderliche Code zum Erstellen eines Textfelds angezeigt.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Beachten Sie, dass der im Textfeld angezeigte Text von den TextBox-Tags eingeschlossen wird. Der Text in den Tags kann durch normale HTML-Tags geändert werden.

**Beispiel**

-   [Einfaches TextBox-Beispiel](/previous-versions/bb264075(v=vs.85))

 

 