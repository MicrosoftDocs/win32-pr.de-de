---
title: Vollständiger Code für simple skin
description: Vollständiger Code für simple skin
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Erstellen von Skins, Codebeispielen
- Windows Media Player Skins, Codebeispiele
- Skins, Codebeispiele
- Skindefinitionsdateien, Codebeispiele
- Erstellen von Skins, Beispielen
- Windows Media Player Skins, Beispiele
- Skins, Beispiele
- Skindefinitionsdateien, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b4d4380c6d7fb44290e8faff26bf5cb84dae552d09fe13594402dbe434ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135793"
---
# <a name="complete-code-for-simple-skin"></a>Vollständiger Code für simple skin

Hier ist der vollständige Code für die erste Beispielskin:


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

Erstellen Sie eine komprimierte Datei mit der Dateinamenerweiterung .zip. Diese komprimierte Datei enthält Ihre Skindefinitionsdatei, Bitmaps und alle digitalen Mediendateien, die Sie einschließen möchten. Benennen Sie die Datei so um, dass sie über die Dateinamenerweiterung .wmz verfügt. Wenn Sie dann auf die komprimierte Skin doppelklicken, wird die Wiedergabe gestartet.

Eine ähnliche funktionierende einfache Skin finden Sie im Abschnitt mit den Beispielen des SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen der Skindefinitionsdatei**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




