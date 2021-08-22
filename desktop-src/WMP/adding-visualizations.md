---
title: Hinzufügen von Visualisierungen
description: Hinzufügen von Visualisierungen
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Erstellen von Skins, Visualisierungen
- Windows Media Player Skins,Visualisierungen
- Skins, Visualisierungen
- Visualisierungen,Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d236990d3e29cf4e51dbb46e8e1269b0c8a50ccaf205940a6f34b97c89fa6e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619150"
---
# <a name="adding-visualizations"></a>Hinzufügen von Visualisierungen

Sie können ein Visualisierungsfenster auf die gleiche Weise hinzufügen, wie Sie ein Videofenster hinzugefügt haben. Die gleiche Skin kann verwendet werden, es wird jedoch **ein EFFECTS-Element** verwendet.

Zuerst müssen Sie das **EFFECTS-Element** hinzufügen und ihm eine ID und Größe geben:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



Anschließend können Sie den beiden Schaltflächen eine vorherige und eine nächste Visualisierungscodezeichenfolge zuweisen:


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



Die Ebenen und Bitmaps waren die gleichen, die im Videobeispiel verwendet wurden, mit der Ausnahme, dass der Wiedergabepfeil kopiert und horizontal gekippt wurde.

Schließlich wurde ein einfaches **PLAYER-Element** mit dem **URL-Attribut** hinzugefügt, um einen zu spielenden Titel zu wählen.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



Eine ähnliche funktionierende Visualisierungss skin finden Sie im Beispielabschnitt des SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch zur Erstellung von Skins**](skin-creation-guide.md)
</dt> </dl>

 

 




