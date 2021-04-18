---
title: Hinzufügen einer Wiedergabeliste
description: Hinzufügen einer Wiedergabeliste
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- Erstellen von Skins, Wiedergabelisten
- Windows Media Player Skins, Wiedergabelisten
- Skins, Wiedergabelisten
- Wiedergabelisten, Skins
- Metadatei-Wiedergabelisten, Skins
- Windows Media Metadatei-Wiedergabelisten, Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340226"
---
# <a name="adding-a-playlist"></a>Hinzufügen einer Wiedergabeliste

Mithilfe von Wiedergabelisten können Sie aus den Sammlungen ihrer Audiodaten und Videos auswählen.

Wenn Sie die Grafik von ihrer ersten Skin verwenden, können Sie einige Änderungen an der Skin-Definitionsdatei vornehmen.

Der erste Schritt besteht darin, die Shell zu verwenden, die für die meisten Skins verwendet wird:


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



Fügen Sie nun eine zweite **Ansicht** hinzu, die eine Wiedergabeliste enthält. Platzieren Sie den folgenden Code nach dem </VIEW> des Shellcodes.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



Sie müssen dieser zweiten Ansicht eine ID zuordnen, damit Sie später darauf verweisen können. Fügen Sie ein playelement und ein stopelement hinzu. Diese vordefinierten Schaltflächen machen das Leben einfacher.


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



Fügen Sie schließlich dem playelement ein OnClick-Ereignis hinzu, um eine Wiedergabeliste in der zweiten Ansicht anzuzeigen:


```C++
            onClick = "JScript: theme.openView('playview');" />

```



Im Beispiel Abschnitt des SDK sehen Sie eine ähnliche funktionierende Wiedergabeliste.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Erstellen von Skin**](skin-creation-guide.md)
</dt> </dl>

 

 




