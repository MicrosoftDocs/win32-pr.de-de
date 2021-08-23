---
title: Commands-Objekteigenschaften
description: Commands-Objekteigenschaften
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b9e8f8e6e7b44697891cd567fce8ca0f5db13a0142936b5cf48bdb52721392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716540"
---
# <a name="commands-object-properties"></a>Commands-Objekteigenschaften

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Der Server unterstützt die folgenden Eigenschaften für die [**Commands-Sammlung:**](/windows/desktop/lwef/the-commands-collection-object)

-   [**Caption**](caption-property-cmds.md)
-   [**Anzahl**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**Fontsize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**Helpcontextid**](helpcontextid-property.md)
-   [**Sichtbar**](visible-property-cso.md)
-   [**Sprache**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

Ein Eintrag für die [**Sammlung Befehle**](/windows/desktop/lwef/the-commands-collection-object) kann sowohl im Popupmenü als auch im Sprachbefehlsfenster für ein Zeichen angezeigt werden. Damit dieser Eintrag im Popupmenü angezeigt wird, legen Sie dessen [**Caption-Eigenschaft**](caption-property-cmds.md) fest. Legen Sie die VoiceCaption-Eigenschaft fest, um den Eintrag in das [**Fenster "Sprachbefehle"**](voicecaption-property.md) ein-/aus. (Aus Gründen der Abwärtskompatibilität wird die Einstellung Caption verwendet, wenn **voiceCaption** **nicht** vorhanden ist.)

In der folgenden Tabelle wird zusammengefasst, wie sich die Eigenschaften eines [**Commands-Objekts**](/windows/desktop/lwef/the-commands-collection-object) auf die Darstellung des Eintrags auswirken:



| Caption-Eigenschaft                                                                                                                                                                                                                                            | Voice-Caption-Eigenschaft | Voice-Eigenschaft | Visible-Eigenschaft | Wird im Popupmenü des Zeichens angezeigt | Wird im Fenster "Sprachbefehle" angezeigt |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Ja                                                                                                                                                                                                                                                         | Ja                    | Ja            | Richtig             | Ja, verwenden von Caption                 | Ja, mit VoiceCaption          |
| Ja                                                                                                                                                                                                                                                         | Ja                    | Nein             | Richtig             | Ja, verwenden von Caption                 | Nein                               |
| Ja                                                                                                                                                                                                                                                         | Ja                    | Ja            | False            | Nein                                 | Ja, mit VoiceCaption          |
| Ja                                                                                                                                                                                                                                                         | Ja                    | Nein             | False            | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Ja            | True             | Nein                                 | Ja, mit VoiceCaption          |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Ja            | False            | Nein                                 | Ja, mit VoiceCaption          |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Nein             | True             | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Nein             | False            | Nein                                 | Nein                               |
| Ja                                                                                                                                                                                                                                                         | Nein                    | Ja            | Richtig             | Ja, verwenden von Caption                 | Ja, verwenden von Caption               |
| Ja                                                                                                                                                                                                                                                         | Nein                     | Nein             | True             | Ja                                | Nein                               |
| Ja                                                                                                                                                                                                                                                         | Nein                     | Ja            | False            | Nein                                 | Ja, verwenden von Caption               |
| Ja                                                                                                                                                                                                                                                         | Nein                     | Nein             | False            | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Ja            | True             | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Ja            | False            | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Nein             | True             | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Nein             | False            | Nein                                 | Nein                               |
|  Wenn die Eigenschafteneinstellung NULL ist. In einigen Programmiersprachen kann eine leere Zeichenfolge nicht als null-Zeichenfolge interpretiert werden.  Der Befehl ist weiterhin sprachbereit und wird im Fenster "Sprachbefehle" als "(command undefined)" angezeigt.<br/> |                        |                |                  |                                    |                                  |



 

 

