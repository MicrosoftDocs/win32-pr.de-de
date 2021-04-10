---
title: Hinzufügen einer ButtonGroup
description: Hinzufügen einer ButtonGroup
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Erstellen von Skins, ButtonGroup-Element
- Windows Media Player Skins, ButtonGroup-Element
- Skins, ButtonGroup-Element
- Skin-Definitions Dateien, ButtonGroup-Element
- ButtonGroup-Element
- Elemente, ButtonGroup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309580"
---
# <a name="adding-buttongroup"></a>Hinzufügen einer ButtonGroup

In diesem Beispiel wird das **ButtonGroup** -Element für die Codierung in der Skin-Definitionsdatei verwendet. **ButtonGroup** stellt eine einfache Möglichkeit zum Verarbeiten von Mausereignissen dar, ohne dass exakte Positionen auf dem Bildschirm berechnet werden müssen und anstelle von x-und y-Koordinaten Farben verwendet werden.

Zuerst müssen Sie der von Ihnen erstellten Skin-Definitionsdatei die **ButtonGroup** -Tags hinzufügen. Fügen Sie Sie nach **den Design** -Tagattributen ein.


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Lassen Sie für die Schaltflächen, die Sie als nächstes hinzufügen, ein paar leere Zeilen oberhalb des schließenden **ButtonGroup** -Tags.

Die folgenden Attribute werden verwendet, um **ButtonGroup** zu definieren:

**mappingImage**

Dies ist der Dateiname der Datei, die Sie zuvor erstellt haben, die mit den roten und grünen Kreisen. Dieses Attribut ist für jede **ButtonGroup** erforderlich.

**hoverimage**

Dies ist der Dateiname der Hover-Art-Datei, die Sie zuvor erstellt haben, die mit den beiden gelben Schaltflächen "Play" und "Close". Dies ist nicht erforderlich, aber ein Hover-Bild hilft beim Bereitstellen von Feedback für den Benutzer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skin-Definitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




