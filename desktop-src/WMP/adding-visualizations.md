---
title: Hinzufügen von Visualisierungen
description: Hinzufügen von Visualisierungen
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Erstellen von Skins, Visualisierungen
- Windows Media Player Skins, Visualisierungen
- Skins, Visualisierungen
- Visualisierungen, Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710787"
---
# <a name="adding-visualizations"></a>Hinzufügen von Visualisierungen

Sie können ein Visualisierungs Fenster auf die gleiche Weise hinzufügen, wie Sie ein Videofenster hinzugefügt haben. Dieselbe Skin kann verwendet werden, es wird jedoch ein **Effects** -Element verwendet.

Zuerst müssen Sie das **Effects** -Element hinzufügen und ihm eine ID und eine Größe geben:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



Anschließend können Sie die beiden Schaltflächen als vorherige und nächste Visualisierungs Code Zeichenfolge zuweisen:


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



Die Ebenen und Bitmaps waren dieselben, die im Video Beispiel verwendet wurden, mit dem Unterschied, dass der Wiedergabe Pfeil horizontal kopiert und gekippt wurde.

Schließlich wurde ein einfaches **Player** -Element mit dem **URL** -Attribut hinzugefügt, um einen zu Wiedergabe enden Song auszuwählen.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



Im Beispiel Abschnitt des SDK sehen Sie eine ähnliche Funktionsweise für die Visualisierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Erstellen von Skin**](skin-creation-guide.md)
</dt> </dl>

 

 




