---
title: Beispiel für Schaltflächen Bereich
description: Beispiel für Schaltflächen Bereich
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bereich
- Skins, Schaltflächen Abschnitt
- Verweis für Skins, Schaltflächen Abschnitt
- Schaltflächen in Skins, Schaltflächen Abschnitt
- Skin-Definitions Dateien, Schaltflächen Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037205"
---
# <a name="sample-button-section"></a>Beispiel für Schaltflächen Bereich

Die folgenden Zeilen zeigen einen typischen Schaltflächen Abschnitt einer Skin-Definitionsdatei:


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



Dieser Code definiert acht Schaltflächen, die für die Bereitstellung aller der folgenden Funktionen in einem Skin verwendet werden:

-   Wiedergeben, anhalten und stoppen von Medien Elementen.
-   Ummischen, wiederholen und durchlaufen der Wiedergabeliste.
-   Das Volume wird stumm geschaltet.

Alle Schaltflächen außer der Schaltfläche stumm Schaltung sind Regions Schaltflächen. Die Schaltfläche stumm Schaltung Ruft die per pushübertragung und deaktivierten Bilder aus dem Super Bitmap aus.

> [!Note]  
> Schaltflächen Typen sind in Skins für Windows Media Player 10 Mobile oder höher veraltet. Geben Sie anstelle eines in der Skin-Datei deklarierten Schaltflächen Typs für jeden Typ "na" ein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schaltflächen**](buttons.md)
</dt> </dl>

 

 




