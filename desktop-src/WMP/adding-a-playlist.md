---
title: Hinzufügen einer Wiedergabeliste
description: Hinzufügen einer Wiedergabeliste
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- Erstellen von Skins, Wiedergabelisten
- Windows Media Player skins,playlists
- Skins, Wiedergabelisten
- Wiedergabelisten,Skins
- Metafile-Wiedergabelisten,Skins
- Windows Wiedergabelisten von Medienmetadateien, Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23d9198f1f913b83cef40cea9f6ec47976f9f1e08a5e54257ab16df63e538b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031590"
---
# <a name="adding-a-playlist"></a>Hinzufügen einer Wiedergabeliste

Sie können Wiedergabelisten verwenden, um aus Sammlungen Ihrer Audio- und Videodateien zu wählen.

Mithilfe der Grafik aus Ihrer ersten Skin können Sie einige Änderungen an der Skindefinitionsdatei vornehmen.

Der erste Schritt besteht in der Verwendung der Shell, die Sie für die meisten Skins verwenden:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



Fügen Sie nun eine zweite **VIEW hinzu,** die eine Wiedergabeliste enthält. Platzieren Sie den folgenden Code nach dem </VIEW> des Shellcodes.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



Sie müssen dieser zweiten Ansicht eine ID geben, damit Sie später darauf verweisen können. Fügen Sie ein PLAYELEMENT und ein STOPELEMENT hinzu. Diese vordefinierten Schaltflächen erleichtern das Leben.


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



Fügen Sie abschließend dem PLAYELEMENT ein onClick-Ereignis hinzu, um eine Wiedergabeliste in der zweiten Ansicht anzuzeigen:


```C++
            onClick = "JScript: theme.openView('playview');" />

```



Eine ähnliche Arbeitswiedergabelisten-Skin finden Sie im Beispielabschnitt des SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch zur Erstellung von Skins**](skin-creation-guide.md)
</dt> </dl>

 

 




