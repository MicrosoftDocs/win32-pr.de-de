---
title: VML TextPath-Element
description: VML TextPath-Element
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08707ae79bf297e6094228b26ae118c57a03c736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339488"
---
# <a name="vml-textpath-element"></a>VML TextPath-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Textpfad für eine Form.

Die folgenden Attribute ändern einen Textpfad.



| Attribut                                                                    | BESCHREIBUNG                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Fitpath](msdn-online-vml-fitpath-attribute.md)                             | Definiert, ob der Text dem Pfad einer Form entspricht.                             |
| [Fitshape](msdn-online-vml-fitshape-attribute.md)                           | Definiert, ob der Text an die Form Begrenzungen passt.                            |
| [Schriftfamilie](msdn-online-vml-font-family-attribute.md)                     | Gibt die Schriftart Text Familie an.                                             |
| [Schrift Grad](msdn-online-vml-font-size-attribute.md)                         | Gibt die Schriftgröße von Text an.                                               |
| [Schriftart Stil](msdn-online-vml-font-style-attribute.md)                       | Gibt den Schriftart Stil von Text an.                                              |
| [Schriftart-Variant](msdn-online-vml-font-variant-attribute.md)                   | Gibt die Schriftart Variante von Text an.                                            |
| [Schrift Breite](msdn-online-vml-font-weight-attribute.md)                     | Gibt die Schrift Breite von Text an.                                             |
| [Schriftart](msdn-online-vml-font-attribute.md)                                   | Gibt den zusammengesetzten Schriftart Wert von Text an.                                     |
| [Mso-Text Schatten](msdn-online-vml-mso-text-shadow-attribute.md)             | Definiert, ob ein Schatten auf den Text angewendet wird.                               |
| [Ein](on-attribute--textpath--vml.md)                                        | Definiert, ob der Text angezeigt wird.                                         |
| [String](msdn-online-vml-string-attribute.md)                               | Definiert die Text Zeichenfolge.                                                       |
| [Text-Dekoration](msdn-online-vml-text-decoration-attribute.md)             | Definiert die Text Dekoration des Texts.                                       |
| [Trim](msdn-online-vml-trim-attribute.md)                                   | Definiert, ob zusätzlicher Leerraum oberhalb und unterhalb des Texts entfernt wird.               |
| [V-Rotation-Buchstaben](msdn-online-vml-v-rotate-letters-attribute.md)           | Bestimmt, ob die Buchstaben des Texts gedreht werden.                        |
| [V-Höhe-Buchstabe-Höhe](msdn-online-vml-v-same-letter-heights-attribute.md) | Bestimmt, ob alle Buchstaben dieselbe Höhe aufweisen.                      |
| [V-Text-align](msdn-online-vml-v-text-align-attribute.md)                   | Definiert die Ausrichtung des Texts.                                             |
| [V-Text-Kern](msdn-online-vml-v-text-kern-attribute.md)                     | Bestimmt, ob die kernung aktiviert ist.                                       |
| [V-Text-Reverse](msdn-online-vml-v-text-reverse-attribute.md)               | Bestimmt, ob die layoutreihenfolge der Zeilen umgekehrt wird.                       |
| [V-Text-Abstände-Modus](msdn-online-vml-v-text-spacing-mode-attribute.md)     | Definiert den Modus für Brief Abstände.                                            |
| [V-Text-Abstand](msdn-online-vml-v-text-spacing-attribute.md)               | Definiert die Größe des Abstands für Text.                                        |
| [XScale](msdn-online-vml-xscale-attribute.md)                               | Bestimmt, ob anstelle des Shape-Pfads ein geradliniger Textpfad verwendet wird. |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Zusätzlich zu den normalen Füll-, Zeichen folgen-und Format Attributen muss das [textpathok](msdn-online-vml-textpathok-attribute.md) -Attribut von [path](msdn-online-vml-path-element.md) auf **true** festgelegt werden, und das [on](on-attribute--textpath--vml.md) -Attribut von TextPath muss auf **true** festgelegt werden, um Text in einem Textpfad anzuzeigen.

Im folgenden finden Sie den minimalen Code, der zum Anzeigen von Text in einem Pfad erforderlich ist.


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**Beispiele**

-   [Einfaches TextPath-Beispiel](/previous-versions/bb264038(v=vs.85))
-   [Beispiel für dynamisches TextPath-Schriftart](/previous-versions/bb264042(v=vs.85))
-   [Beispiel für dynamische Textpfad-Kurve](/previous-versions/bb264041(v=vs.85))

 

 