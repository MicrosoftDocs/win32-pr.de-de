---
title: Vervollständigen von Code für einfache Skin
description: Vervollständigen von Code für einfache Skin
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Erstellen von Skins, Codebeispielen
- Windows Media Player Skins, Codebeispiele
- Skins, Codebeispiele
- Skin-Definitions Dateien, Codebeispiele
- Erstellen von Skins, Beispiele
- Windows Media Player Skins, Beispiele
- Skins, Beispiele
- Skin-Definitions Dateien, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856443"
---
# <a name="complete-code-for-simple-skin"></a>Vervollständigen von Code für einfache Skin

Im folgenden finden Sie den gesamten Code für die erste Beispiel Skin:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



Nun haben Sie alle Teile zusammengestellt.

Erstellen Sie eine komprimierte Datei mit der Dateinamenerweiterung ". zip". Diese komprimierte Datei enthält Ihre Skin-Definitionsdatei, Bitmaps und alle Digital Media-Dateien, die Sie einschließen möchten. Benennen Sie die Datei so um, dass Sie die Dateinamenerweiterung. WMZ enthält. Wenn Sie dann auf die komprimierte Skin doppelklicken, wird Sie gestartet.

Im Abschnitt mit den Beispielen des SDK sehen Sie eine ähnliche Arbeits einfache Skin.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skin-Definitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




