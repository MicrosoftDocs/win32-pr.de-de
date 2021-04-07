---
title: VML-TextBox-Element
description: VML-TextBox-Element
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a46ce8b6636b79099b7f7423fd8f746602a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727568"
---
# <a name="vml-textbox-element"></a>VML-TextBox-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert ein Textfeld für eine Form.

Mit den folgenden Attributen wird ein Textfeld geändert.



| Attribut                                                                    | BESCHREIBUNG                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Richtung](msdn-online-vml-direction-attribute.md)                         | Definiert die Richtung des Texts.                         |
| [ID](id-attribute--textbox--vml.md)                                         | Definiert einen eindeutigen Bezeichner für das Textfeld.               |
| [Einfügen](msdn-online-vml-inset-attribute.md)                                 | Gibt die inneren Rand Werte für Text Feld Text an.            |
| [Insetmode](msdn-online-vml-insetmode-attribute.md)                         | Definiert, wie eine Anwendung benutzerdefinierte insetwerte zulässt. |
| [Layoutfluss](msdn-online-vml-layout-flow-attribute.md)                     | Bestimmt den Text Fluss im Textfeld.            |
| [Mso-Richtung-alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Definiert Alternative Anweisungen für Text in Textfeldern.        |
| [Mso-fit-Shape-to-Text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Bestimmt, ob eine Form an Text angepasst wird.       |
| [Mso-fit-Text-in-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Bestimmt, ob Text für eine Form angepasst wird.       |
| [Mso-Layout-Flow-alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Definiert den alternativen layoutfluss für Text in einem Textfeld.   |
| [Mso-Next-TextBox](msdn-online-vml-mso-next-textbox-attribute.md)           | Gibt das nächste Textfeld in einer Reihe an.                    |
| [Mso-drehen](msdn-online-vml-mso-rotate-attribute.md)                       | Bestimmt, ob der Text mit einer gedrehten Form rotiert.      |
| [Mso-Text Skalieren](msdn-online-vml-mso-text-scale-attribute.md)               | Definiert den Skalierungsfaktor für die Anpassung von Text an Formen.     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | Bestimmt, ob der Text mit einem einzigen Mausklick auswählbar ist. |
| [V-Text-Anker](msdn-online-vml-v-text-anchor-attribute.md)                 | Definiert das vertikale Verankern von Text in einem Textfeld.       |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Im folgenden finden Sie den minimalen Code, der zum Entwickeln eines Textfelds erforderlich ist.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Beachten Sie, dass der Text, der im Textfeld angezeigt wird, von den Textfeld-Tags eingeschlossen wird. Der Text innerhalb der Tags kann durch normale HTML-Tags geändert werden.

**Beispiel**

-   [Einfaches Beispiel für ein Textfeld](/previous-versions/bb264075(v=vs.85))

 

 