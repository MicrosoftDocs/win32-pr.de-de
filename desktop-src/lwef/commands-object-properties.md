---
title: Objekteigenschaften für Befehle
description: Objekteigenschaften für Befehle
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4493b1e146a011434f7a0324a4008031a575d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038826"
---
# <a name="commands-object-properties"></a>Objekteigenschaften für Befehle

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Der Server unterstützt die folgenden Eigenschaften für die [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung:

-   [**Caption**](caption-property-cmds.md)
-   [**Countdown**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**Globalvoicecommandsenabled**](globalvoicecommandsenabled-property.md)
-   [**HelpContextID**](helpcontextid-property.md)
-   [**Sichtbar**](visible-property-cso.md)
-   [**Sprache**](voice-property.md)
-   [**Voicecaption**](voicecaption-property.md)

Ein Eintrag für die [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung kann sowohl im Popup Menü als auch im Fenster "Sprachbefehle" für ein Zeichen angezeigt werden. Damit dieser Eintrag im Popupmenü angezeigt wird, legen Sie die [**Beschriftung**](caption-property-cmds.md) -Eigenschaft fest. Wenn Sie den Eintrag in das Fenster "Sprachbefehle" einschließen möchten, legen Sie seine [**voicecaption**](voicecaption-property.md) -Eigenschaft fest. (Aus Gründen der Abwärtskompatibilität wird die **Beschriftungs** Einstellung verwendet, wenn keine **voicecaption** vorhanden ist.)

In der folgenden Tabelle wird zusammengefasst, wie sich die Eigenschaften eines [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Objekts auf die Darstellung des Eintrags auswirken:



| Caption-Eigenschaft                                                                                                                                                                                                                                            | Voice-Caption-Eigenschaft | Voice-Eigenschaft | Visible-Eigenschaft | Wird im Popupmenü des Zeichens angezeigt. | Wird im Fenster "Sprachbefehle" angezeigt |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Ja                                                                                                                                                                                                                                                         | Ja                    | Ja            | Richtig             | Ja, mit Beschriftung                 | Ja, mit voicecaption          |
| Ja                                                                                                                                                                                                                                                         | Ja                    | Nein             | Richtig             | Ja, mit Beschriftung                 | Nein                               |
| Ja                                                                                                                                                                                                                                                         | Ja                    | Ja            | False            | Nein                                 | Ja, mit voicecaption          |
| Ja                                                                                                                                                                                                                                                         | Ja                    | Nein             | False            | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Ja            | True             | Nein                                 | Ja, mit voicecaption          |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Ja            | False            | Nein                                 | Ja, mit voicecaption          |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Nein             | True             | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Ja                    | Nein             | False            | Nein                                 | Nein                               |
| Ja                                                                                                                                                                                                                                                         | Nein                    | Ja            | Richtig             | Ja, mit Beschriftung                 | Ja, mit Beschriftung               |
| Ja                                                                                                                                                                                                                                                         | Nein                     | Nein             | True             | Ja                                | Nein                               |
| Ja                                                                                                                                                                                                                                                         | Nein                     | Ja            | False            | Nein                                 | Ja, mit Beschriftung               |
| Ja                                                                                                                                                                                                                                                         | Nein                     | Nein             | False            | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Ja            | True             | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Ja            | False            | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Nein             | True             | Nein                                 | Nein                               |
| Nein                                                                                                                                                                                                                                                          | Nein                     | Nein             | False            | Nein                                 | Nein                               |
|  , Wenn die Eigenschafts Einstellung NULL ist. In manchen Programmiersprachen kann eine leere Zeichenfolge nicht als identisch mit einer NULL-Zeichenfolge interpretiert werden.  Der Befehl ist weiterhin sprach zugänglich und wird im Fenster "Sprachbefehle" als "(Befehl nicht definiert)" angezeigt.<br/> |                        |                |                  |                                    |                                  |



 

 

