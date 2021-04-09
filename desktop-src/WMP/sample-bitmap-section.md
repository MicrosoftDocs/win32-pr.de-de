---
title: Beispiel für einen bitmapabschnitt
description: Beispiel für einen bitmapabschnitt
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Verweis für Skins, Bitmaps
- Bitmaps in Skins, Bitmaps (Abschnitt)
- Skin-Definitions Dateien, Abschnitt "Bitmaps"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856568"
---
# <a name="sample-bitmap-section"></a>Beispiel für einen bitmapabschnitt

Die folgenden Zeilen zeigen einen typischen Bitmaps-Abschnitt einer Skin-Definitionsdatei:


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



Definiert fünf Bitmaps, die zum Erstellen eines Hintergrund Bilds, Bilder für die Schaltflächen deaktiviert und per pushübertragung, ein Regions Bild für Regions Schaltflächen und ein superbild für trackbars verwendet werden.

> [!Note]  
> Region und Super Bitmaps sind in Skins für Windows Media Player 10 Mobile oder höher veraltet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bitmaps**](bitmaps.md)
</dt> </dl>

 

 




