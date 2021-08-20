---
title: Hinzufügen von BUTTONGROUP
description: Hinzufügen von BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Erstellen von Skins, BUTTONGROUP-Element
- Windows Media Player,BUTTONGROUP-Element
- skins,BUTTONGROUP-Element
- Skindefinitionsdateien,BUTTONGROUP-Element
- BUTTONGROUP-Element
- elements,BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6719bb3974b254f8d9446d45fd6d34385dbfcada4084c7bdd5c3a4e03bb06dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865189"
---
# <a name="adding-buttongroup"></a>Hinzufügen von BUTTONGROUP

In diesem Beispiel wird das **BUTTONGROUP-Element** für die Codierung in der Skindefinitionsdatei verwendet. **BUTTONGROUP** bietet eine einfache Möglichkeit, Mausereignisse zu verarbeiten, ohne genaue Positionen auf dem Bildschirm berechnen zu müssen, und verwendet Farben anstelle von x- und y-Koordinaten.

Zuerst müssen Sie die **BUTTONGROUP-Tags** der erstellten Skindefinitionsdatei hinzufügen. Legen Sie sie nach den **THEME-Tagattributen** ab.


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Lassen Sie einige leere Zeilen über dem schließenden **BUTTONGROUP-Tag** für die Schaltflächen, die Sie als Nächstes hinzufügen.

Die folgenden Attribute werden verwendet, um **BUTTONGROUP zu definieren:**

**mappingImage**

Dies ist der Dateiname der Zuordnungsartdatei, die Sie zuvor erstellt haben, der Dateiname mit den roten und grünen Kreisen. Dieses Attribut ist für jede **BUTTONGROUP erforderlich.**

**hoverImage**

Dies ist der Dateiname der zuvor erstellten Hoverartdatei, die mit den beiden gelben Schaltflächen "Play" und "Close" (Schließen) lautet. Dies ist nicht erforderlich, aber ein Bild mit dem Hover hilft, dem Benutzer Feedback zu geben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skindefinitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




