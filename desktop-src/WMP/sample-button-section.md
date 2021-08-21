---
title: Abschnitt "Beispielschaltfläche"
description: Abschnitt "Beispielschaltfläche"
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Windows Media Player Mobile Skins, Abschnitt "Schaltfläche"
- Skins, Abschnitt "Schaltfläche"
- Referenz für Skins, Abschnitt "Schaltfläche"
- Schaltflächen in Skins, Abschnitt "Schaltfläche"
- Skindefinitionsdateien, Abschnitt "Schaltfläche"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c69d57248664808062c2f6e0d3f9d331edd7cd0f07085ec76fc51a1960817d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833384"
---
# <a name="sample-button-section"></a>Abschnitt "Beispielschaltfläche"

Die folgenden Zeilen zeigen einen typischen Schaltflächenabschnitt einer Skindefinitionsdatei:


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



Dieser Code definiert acht Schaltflächen, die verwendet werden, um alle folgenden Funktionen in einer Skin zur Verfügung zu stellen:

-   Wiedergabe, Pause und Beenden von Medienelementen.
-   Shuffle, Repeat und Move Through der Wiedergabeliste.
-   Stummschalten des Volumes.

Alle Schaltflächen außer der Stummschaltfläche sind Bereichschaltflächen. Die Stummschaltfläche ruft der Einfachheit halber die Bilder Pushed und Disabled aus der Super-Bitmap ab.

> [!Note]  
> Schaltflächentypen sind in Skins für Windows Media Player 10 Mobile oder höher veraltet. Geben Sie anstelle eines Schaltflächentyps, der in Ihrer Skindatei deklariert ist, "NA" für jeden Typ ein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




